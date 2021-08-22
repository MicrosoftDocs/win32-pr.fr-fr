---
title: Élément SKIN (déconseillé)
description: cette page documente une fonctionnalité qui peut ne pas être disponible dans les futures versions de Lecteur Windows Media et le kit de développement logiciel (SDK) Lecteur Windows Media.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- élément SKIN (déconseillé) Lecteur Windows Media
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b868b756ed190301c66987b6e26249762bac71842f4a5425d6d7c6d4b16816a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507909"
---
# <a name="skin-element-deprecated"></a>Élément SKIN (déconseillé)

cette page documente une fonctionnalité qui peut ne pas être disponible dans les futures versions de Lecteur Windows Media et le kit de développement logiciel (SDK) Lecteur Windows Media.

L’élément **Skin** spécifie une URL vers une bordure.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

URL d’un fichier de bordure compressé avec l’extension de nom de fichier. WMZ. pour Lecteur Windows Media série 9 ou version ultérieure, cette valeur peut faire référence uniquement aux fichiers de bordure sur le disque dur de l’utilisateur situé dans le même répertoire que la sélection de métafichiers. Consultez l’exemple de code.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments |
|-----------------|----------|
| Éléments parents | **ASX**  |
| Éléments enfants  | None     |



 

## <a name="remarks"></a>Remarques

l’élément **SKIN** est utilisé pour créer une bordure, qui est similaire à une apparence, mais qui est affichée dans la zone de **jeu à présent** du Lecteur Windows Media en mode complet. l’élément **SKIN** est utilisé uniquement pour les bordures, qui apparaissent à l’intérieur du Lecteur Windows Media en mode complet, et non pour les apparences régulières, qui remplacent entièrement le mode compact Lecteur Windows Media.

dans un Package Windows Media Download (avec l’extension de nom de fichier. wmd), l’élément **SKIN** permet à une bordure d’avoir du contenu et d’établir un lien vers d’autres sites. le Package de téléchargement Windows Media est un fichier compressé qui contient un fichier de bordure et un métafichier Windows media. Le fichier de bordure (avec l’extension de nom de fichier. WMZ) est compressé et comprend un fichier de définition d’apparence (avec l’extension de nom de fichier. WMS).

Un élément **Skin** a trois composants :

-   Une apparence
-   Du contenu
-   Un métafichier

les habillages fournis avec Windows Packages de téléchargement de médias doivent être de forme rectangulaire. La création de bordures avec des apparences qui ne sont pas rectangulaires peut produire des résultats inattendus.

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

[**bordures pour la Lecteur Windows Media (déconseillée)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





