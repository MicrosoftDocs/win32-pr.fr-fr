---
title: Élément SKIN (déconseillé)
description: Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Élément SKIN (déconseillé) lecteur Windows Media
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537772"
---
# <a name="skin-element-deprecated"></a>Élément SKIN (déconseillé)

Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.

L’élément **Skin** spécifie une URL vers une bordure.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

URL d’un fichier de bordure compressé avec l’extension de nom de fichier. WMZ. Pour le lecteur Windows Media série 9 ou version ultérieure, cette valeur peut référencer uniquement les fichiers de bordure sur le disque dur de l’utilisateur situé dans le même répertoire que la sélection de métafichiers. Consultez l’exemple de code.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments |
|-----------------|----------|
| Éléments parents | **ASX**  |
| Éléments enfants  | Aucune     |



 

## <a name="remarks"></a>Notes

L’élément **Skin** est utilisé pour créer une bordure, qui est similaire à une apparence, mais qui est affichée dans la zone de **lecture à présent** du lecteur Windows Media en mode complet. L’élément **Skin** est utilisé uniquement pour les bordures, qui apparaissent dans le lecteur Windows Media en mode complet, et non pour les skins standard, qui remplacent entièrement le mode compact du lecteur Windows Media.

Dans un package de téléchargement Windows Media (avec l’extension de nom de fichier. WMD), l’élément **Skin** permet à une bordure d’avoir du contenu et d’établir un lien vers d’autres sites. Le package de téléchargement Windows Media est un fichier compressé qui contient un fichier de bordure et un métafichier Windows Media. Le fichier de bordure (avec l’extension de nom de fichier. WMZ) est compressé et comprend un fichier de définition d’apparence (avec l’extension de nom de fichier. WMS).

Un élément **Skin** a trois composants :

-   Une apparence
-   Du contenu
-   Un métafichier

Les habillages fournis avec les packages de téléchargement Windows Media doivent être de forme rectangulaire. La création de bordures avec des apparences qui ne sont pas rectangulaires peut produire des résultats inattendus.

## <a name="examples"></a>Exemples


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Bordures du lecteur Windows Media (déconseillée)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





