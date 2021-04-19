---
title: Élément REF
description: L’élément REF spécifie une URL pour le contenu multimédia numérique.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Élément REF lecteur Windows Media
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528098"
---
# <a name="ref-element"></a>Élément REF

L’élément **ref** spécifie une URL pour le contenu multimédia numérique.

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

URL d’un contenu multimédia pris en charge par le lecteur Windows Media.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Éléments parents | **MENTION**                                                                        |
| Éléments enfants  | **Duration**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **StartTime** |



 

## <a name="remarks"></a>Notes

Cet élément spécifie une URL pour un élément de contenu multimédia. L’URL peut pointer vers n’importe quel type de média pris en charge, à l’aide de n’importe quel protocole pris en charge par le lecteur Windows Media.

Les types de médias pris en charge incluent des images fixes, telles que des images. gif et. jpg et des fichiers Flash, avec l’extension de nom de fichier. swf. Ces types de médias sont utiles pour inclure du contenu publicitaire dans une sélection. Avec les fichiers image et les fichiers Flash qui s’exécutent dans une boucle, vous devez également spécifier la durée d’affichage de l’élément multimédia en incluant un élément **Duration** dans l’élément **ref** . Si vous souhaitez qu’une image continue à s’afficher pendant que l’entrée suivante dans la playlist est mise en mémoire tampon, incluez un élément **param** dans l’élément **entry** , affectez à son attribut **Name** la valeur ShowWhileBuffering et affectez à son attribut **value la valeur** true.

Pour référencer du contenu sur un CD ou un DVD qui l’autorise, les protocoles wmpcd et wmpdvd sont fournis. Par exemple, si vous affectez à l’attribut **href** la valeur « wmpdvd://f/5/3 », le chapitre 3 du titre 5 est lu sur un DVD, mais uniquement si le DVD a été créé pour l’autoriser.

Les applications qui ouvrent des médias numériques derrière un pare-feu bénéficient de meilleures performances lors de l’ouverture des éléments multimédias si l’adresse est spécifiée à l’aide du nom DNS (Domain Name Server) au lieu de l’adresse IP.

L’utilisation la plus courante de cet élément est la substitution d’URL. Si le lecteur Windows Media ne parvient pas à ouvrir un élément multimédia défini dans un élément **ref** , il essaie l’URL dans l’élément **ref** suivant. Une fois que le lecteur Windows Media a ouvert le contenu multimédia à partir d’une URL définie dans l’étendue d’un élément d' **entrée** , il ignore les balises **ref** suivantes dans cet élément d' **entrée** . À la fin de la lecture de la partie de contenu, le lecteur Windows Media passe à l’élément d' **entrée** suivant, le cas échéant.

-   **Important** Une fois que le lecteur Windows Media a établi une connexion à un élément de contenu référencé, il ignore tous les autres éléments **ref** de cette **entrée**, que la connexion se termine normalement ou anormalement.

Si l’élément multimédia référencé est un fichier image, l’élément **Duration** doit être utilisé pour spécifier l’heure d’affichage de l’image.

**Remarque**

Toute tentative de lecture d’un média Flash qui comprend du son avec le premier frame peut produire des résultats inattendus. Vous devez créer un contenu Flash pour qu’il émette un son commençant à ne pas être antérieur à la deuxième image.

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Protocoles et types de fichiers pris en charge**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





