---
description: cet article décrit comment le gestionnaire de Graph de filtre localise un filtre source, en fonction d’un nom de fichier.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Inscription d’un type de fichier personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195384"
---
# <a name="registering-a-custom-file-type"></a>Inscription d’un type de fichier personnalisé

cet article décrit comment le gestionnaire de Graph de filtre localise un filtre source, en fonction d’un nom de fichier. Vous pouvez utiliser ce mécanisme pour inscrire vos propres types de fichiers personnalisés. une fois le type de fichier inscrit, DirectShow charge automatiquement le filtre source approprié chaque fois qu’une application appelle [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

-   [Vue d'ensemble](#overview)
-   [Protocoles](#protocols)
-   [Extensions de fichier](#file-extensions)
-   [Vérifier les octets](#check-bytes)
-   [Chargement du filtre source](#loading-the-source-filter)
-   [Types de fichiers personnalisés dans Lecteur Windows Media](#custom-file-types-in-windows-media-player)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

pour localiser un filtre source à partir d’un nom de fichier donné, le gestionnaire de Graph de filtre tente d’effectuer les opérations suivantes, dans l’ordre :

1.  Correspond au protocole, le cas échéant.
2.  Correspond à l’extension de fichier.
3.  Correspond aux modèles d’octets dans le fichier, appelés *octets de vérification*.

## <a name="protocols"></a>Protocoles

Les noms de protocole tels que « FTP » ou « http » sont inscrits sous le

**\_racine des classes HKEY \_**

clé, avec la structure suivante :


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



si le nom ou l’URL du fichier contient un signe deux-points («  : »), le gestionnaire de Graph de filtre tente d’utiliser la partie avant le «  : » comme nom de protocole. Par exemple, si le nom est « myprot://myfile.ext », il recherche une clé de Registre nommée **myprot**. si cette clé existe et contient une sous-clé nommée « Extensions », le gestionnaire de Graph de filtre recherche dans cette sous-clé les entrées qui correspondent à l’extension de fichier. La valeur de la clé doit être un GUID sous forme de chaîne ; par exemple, « {00000000-0000-0000-0000-000000000000} ». si le gestionnaire de Graph de filtre ne peut pas trouver de correspondance dans la sous-clé **Extensions** , il recherche une sous-clé nommée **filtre Source**, qui doit également être un GUID sous forme de chaîne.

si le gestionnaire de Graph de filtre trouve un GUID correspondant, il l’utilise comme CLSID du filtre source et tente de charger le filtre. S’il ne trouve pas de correspondance, il utilise le filtre de [source de fichier (URL)](file-source--url--filter.md) , qui traite le nom de fichier comme une URL.

Il existe deux exceptions à cet algorithme :

-   Pour exclure des lettres de pilotes, les chaînes à un seul caractère ne sont pas considérées comme des protocoles.
-   Si la chaîne est « file : » ou « file:// », elle n’est pas traitée comme un protocole.

## <a name="file-extensions"></a>Extensions de fichier

s’il n’existe aucun protocole dans le nom de fichier, le gestionnaire de Graph de filtre recherche dans le registre les entrées avec les **\_ \_ \\ \\ Extensions \\ clé HKEY de Type média racine**.*ext* \\ , où.*ext* est l’extension de fichier. Si cette clé existe, le filtre de la **source** de valeur contient le CLSID du filtre source, sous forme de chaîne. Éventuellement, la clé peut avoir des valeurs pour le type et le sous- **type** de **média** , qui fournissent les GUID de type et de sous-type principaux.

## <a name="check-bytes"></a>Vérifier les octets

Certains types de fichiers peuvent être identifiés par des modèles spécifiques de bits se produisant à des décalages d’octets spécifiques dans le fichier. le gestionnaire de Graph de filtre recherche les clés dans le registre au format suivant :

**HKEY \_ CLASSES \_ racine \\ MediaType \\**{ *major type* } \\ { *SubType* }

où le type et le sous- *type* *principaux* sont des GUID qui définissent le type de média pour le flux d’octets. Chaque clé contient une ou plusieurs sous-clés, généralement nommées 1, 2, etc., qui définissent les octets de vérification ; et une sous-clé nommée **source Filter** qui donne le CLSID du filtre source, sous forme de chaîne. Les sous-clés de vérification d’octet sont des chaînes qui contiennent un ou plusieurs Quad de nombres appelés :

*offset*, *CB*, *Mask*, *Val*

pour correspondre au fichier, le gestionnaire de Graph de filtre lit les octets cb, en commençant par le décalage de nombre d’octets. Il effectue ensuite une opération and au niveau du bit sur la valeur du masque. Si le résultat est égal à Val, le fichier est une correspondance pour ce Quad. Les valeurs Mask et Val sont données au format hexadécimal. Une entrée vide pour Mask est traitée comme une chaîne de 1 de longueur CB. Une valeur négative pour offset indique un décalage à partir de la fin du fichier. Pour correspondre à la clé, le fichier doit correspondre à tous les Quad de l’une des sous-clés.

Par exemple, supposons que le registre contient les clés suivantes sous **\\ type de média HKCR**:


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



La première clé correspond au flux du MEDIATYPE de type principal \_ . La sous-clé ci-dessous qui correspond au sous-type de MEDIATYPE \_ midi. La valeur de la sous-clé de filtre source est CLSID \_ AsyncReader, CLSID du filtre de [source de fichier (Async)](file-source--async--filter.md) .

Chaque entrée peut avoir plusieurs quadruples ; tous doivent correspondre. Dans l’exemple suivant, les 4 premiers octets du fichier doivent être 0xAB, 0xCD, 0x12, 0x34 ; et les 4 derniers octets du fichier doivent être 0xAB, 0xAB, 0x00, 0xAB :


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



En outre, il peut y avoir plusieurs entrées listées sous un seul type de média. Une correspondance avec l’une d’entre elles est suffisante. Ce schéma autorise un ensemble de masques alternatifs. par exemple, les fichiers. wav qui peuvent avoir ou non un en-tête RIFF.

> [!Note]  
> Ce schéma est similaire à celui utilisé par la fonction [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) .

 

## <a name="loading-the-source-filter"></a>Chargement du filtre source

en supposant que le gestionnaire de Graph de filtre trouve un filtre de source correspondant pour le fichier, il ajoute ce filtre au graphique, interroge le filtre de l’interface [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) et appelle [**IFileSourceFilter :: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load). Les arguments de la méthode **Load** sont le nom de fichier et le type de média, tel que déterminé à partir du Registre.

si le gestionnaire de Graph de filtre ne trouve rien dans le registre, il utilise par défaut le filtre de Source de fichier asynchrone. Dans ce cas, il définit le type de média sur le **\_ flux de MediaType**, **MEDIASUBTYPE \_ aucun**.

## <a name="custom-file-types-in-windows-media-player"></a>Types de fichiers personnalisés dans Lecteur Windows Media

Lecteur Windows Media utilise un ensemble supplémentaire d’entrées de registre. pour plus d’informations, consultez [Paramètres du registre](../wmp/file-name-extension-registry-settings.md) de l’Extension de nom de fichier dans le kit de développement logiciel Lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 
