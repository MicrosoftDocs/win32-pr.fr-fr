---
title: Élément REF
description: L’élément REF spécifie une URL pour le contenu multimédia numérique.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- élément REF Lecteur Windows Media
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9195eb1fc3ca1f13e64376c0200cbb2e6ec4589e6740a74b1ff7670c0951df25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118333276"
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

URL de tout contenu multimédia pris en charge par Lecteur Windows Media.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Éléments parents | **MENTION**                                                                        |
| Éléments enfants  | **Duration**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **StartTime** |



 

## <a name="remarks"></a>Remarques

Cet élément spécifie une URL pour un élément de contenu multimédia. l’URL peut pointer vers n’importe quel type de média pris en charge, à l’aide de n’importe quel protocole pris en charge par Lecteur Windows Media.

Les types de médias pris en charge incluent les images fixes, telles que .gif et les images .jpg et les fichiers Flash avec une extension de nom de fichier. swf. Ces types de médias sont utiles pour inclure du contenu publicitaire dans une sélection. Avec les fichiers image et les fichiers Flash qui s’exécutent dans une boucle, vous devez également spécifier la durée d’affichage de l’élément multimédia en incluant un élément **Duration** dans l’élément **ref** . Si vous souhaitez qu’une image continue à s’afficher pendant que l’entrée suivante dans la playlist est mise en mémoire tampon, incluez un élément **param** dans l’élément **entry** , affectez à son attribut **Name** la valeur ShowWhileBuffering et affectez à son attribut **value la valeur** true.

Pour référencer du contenu sur un CD ou un DVD qui l’autorise, les protocoles wmpcd et wmpdvd sont fournis. Par exemple, si vous affectez à l’attribut **href** la valeur « wmpdvd://f/5/3 », le chapitre 3 du titre 5 est lu sur un DVD, mais uniquement si le DVD a été créé pour l’autoriser.

Les applications qui ouvrent des médias numériques derrière un pare-feu bénéficient de meilleures performances lors de l’ouverture des éléments multimédias si l’adresse est spécifiée à l’aide du nom DNS (Domain Name Server) au lieu de l’adresse IP.

L’utilisation la plus courante de cet élément est la substitution d’URL. si Lecteur Windows Media ne parvient pas à ouvrir un élément multimédia défini dans un élément **ref** , il essaie l’URL dans l’élément **ref** suivant. une fois que Lecteur Windows Media ouvre le contenu multimédia à partir d’une URL définie dans l’étendue d’un élément d' **entrée** , il ignore les balises **REF** suivantes dans cet élément d' **entrée** . une fois la partie de contenu terminée, Lecteur Windows Media passe à l’élément d' **entrée** suivant, le cas échéant.

-   **Important** une fois que Lecteur Windows Media établit une connexion à un élément de contenu référencé, il ignore tous les autres éléments **REF** de cette **entrée**, que la connexion se termine normalement ou anormalement.

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

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





