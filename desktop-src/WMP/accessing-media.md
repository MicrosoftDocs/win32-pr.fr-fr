---
title: Accès au média
description: Accès au média
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Sélections de métafichiers Windows Media, accès aux médias
- sélections, accès aux médias
- sélections de métafichiers, accès aux médias
- Sélections de métafichiers Windows Media, accès aux médias
- sélections, accès multimédia
- sélections de métafichiers, accès aux médias
- Sélections de métafichiers Windows Media, contrôle de la lecture
- sélections, contrôle de la lecture
- sélections de métafichiers, contrôle de la lecture
- Sélections de métafichiers Windows Media, définition de la durée
- sélections, définition de la durée
- sélections de métafichiers, définition de la durée
- Lecteur Windows Media, accès aux médias
- Lecteur Windows Media, accès aux médias
- Lecteur Windows Media, contrôle de la lecture
- Lecteur Windows Media, définition de la durée
- accès au média
- accès au média
- contrôle de la lecture
- définition de la durée
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510419"
---
# <a name="accessing-media"></a>Accès au média

Utilisez des sélections pour spécifier et contrôler la diffusion multimédia en continu ou les fichiers multimédias lus par le lecteur Windows Media.

Utilisez l’élément **entry** pour spécifier un élément Media unique (un fichier multimédia ou un flux en direct) et tous les éléments enfants (tels que des images, des liens **moreinfo** et du texte **abstrait** ). Utilisez un élément **ENTRYREF** pour spécifier une sélection. Une sélection peut contenir un ou plusieurs éléments d' **entrée** ou de **ENTRYREF** . Le lecteur Windows Media exécute une sélection en commençant par la première entrée, puis en lisant chaque entrée jusqu’à ce que la liste soit terminée.

Un élément d' **entrée** peut pointer vers n’importe quel type de média que le lecteur Windows Media peut lire. Cela comprend non seulement les fichiers. WMA,. wmv,. ASF et. avi, mais également des flux en direct. En utilisant une série d’éléments d' **entrée** ou de **ENTRYREF** pour référencer du contenu multimédia, vous pouvez utiliser une sélection pour envoyer un flux unique constitué de plusieurs sources. Les flux référencés sont lus de manière séquentielle et considérés comme un flux continu par la visionneuse. Par exemple, la sélection peut contenir deux éléments d' **entrée** : une présentation standard d’un fichier Windows Media avec une extension. WMA et un flux Windows Media en direct.

> [!Note]  
> Une sélection ne doit pas contenir de liens vers des fichiers multimédias dont le contenu est créé avec des versions différentes de la Rights Management numérique (DRM). Dans une sélection de métafichiers, s’il existe des liens vers des fichiers multimédias avec un contenu DRM version 1 et des fichiers multimédias créés avec des versions DRM ultérieures, le lecteur Windows Media ne lira que le contenu DRM version 1.

 

## <a name="controlling-playback"></a>Contrôle de la lecture

Utilisez des sélections pour contrôler non seulement quel clip multimédia est lu, mais également quelles parties du clip sont lues et comment. Vous pouvez utiliser des sélections pour définir un ensemble de clips à boucler ou à répéter, pour définir la durée de lecture et pour affecter des heures de début et des marqueurs de début et de fin pour chaque entrée. Les éléments **StartTime**, **STARTMARKER** et **ENDMARKER** fonctionnent conjointement avec les marqueurs dans le fichier multimédia.

Par exemple, la sélection suivante utilise une bannière ad et le lien **moreinfo** associé dans une **entrée**, et fait référence à un **STARTMARKER** et à **ENDMARKER**.


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a>Définition de la durée

Utilisez l’élément **Duration** pour spécifier la durée de lecture d’un clip ou d’un ensemble de clips. Vous pouvez également utiliser l’attribut **PREVIEWMODE** de l’élément **ASX** conjointement avec l’élément **PREVIEWDURATION** pour spécifier la durée de lecture d’un clip ou d’un ensemble de clips. Définissez l’attribut **PREVIEWMODE** sur Oui pour utiliser l’élément **PREVIEWDURATION** pour spécifier la durée pendant laquelle le clip associé doit être lu. Les éléments **PREVIEWDURATION** et **Duration** ont le même comportement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




