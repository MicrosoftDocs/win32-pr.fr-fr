---
title: Modification de l’affichage
description: Modification de l’affichage
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows Sélections de métafichiers multimédia, modification des affichages
- sélections, modification d’affichages
- sélections de métafichiers, modification des affichages
- Windows Sélections du métafichier multimédia, modification de l’affichage
- sélections, modification de l’affichage
- sélections de métafichiers, modification d’affichage
- Lecteur Windows Media, modification de l’affichage
- Lecteur Windows Media, modification des affichages
- Lecteur Windows Media, propriétés de texte
- Lecteur Windows Media, propriétés de l’image
- Lecteur Windows Media, propriétés MOREINFO
- Lecteur Windows Media, texte abstrait
- Propriétés MOREINFO
- Texte abstrait
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919135"
---
# <a name="modifying-the-display"></a>Modification de l’affichage

les sélections peuvent modifier la Lecteur Windows Media interface utilisateur de quatre manières principales :

-   Propriétés du texte
-   Propriétés de l’image
-   Propriétés MOREINFO
-   Texte abstrait

## <a name="text-properties"></a>Propriétés du texte

Lecteur Windows Media permet d’afficher le titre, l’auteur, le Copyright et le texte des métadonnées de Description. Les métadonnées de clip peuvent provenir du flux ou du fichier multimédia, ou elles peuvent provenir d’une sélection. Afficher les métadonnées proviennent de la playlist. en général, les sélections sont une meilleure méthode de transmission des propriétés de texte à Lecteur Windows Media, en particulier si les éléments de texte sont susceptibles d’être modifiés. Il est plus facile de modifier le texte d’une sélection que de recréer un fichier multimédia. Et étant donné que les propriétés lues à partir d’une sélection remplacent celles contenues dans le fichier multimédia, vous pouvez facilement mettre à jour le texte affiché en ajoutant le nouveau texte à la propriété correspondante dans une sélection. Dans l’exemple suivant, le texte du titre et les métadonnées de l’auteur de la sélection remplace le titre et le texte de l’auteur contenu dans le fichier multimédia, Sample. WMA.

le texte de **DESCRIPTION** est récupéré à partir d’un fichier multimédia Windows référencé dans un élément **entry** , sauf s’il existe un élément **ABSTRACT** dans une sélection de métafichiers. S’il y a du texte **abstrait** , il est affiché, remplaçant le texte de **Description** .


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a>Propriétés de l’image

les images de bannière peuvent être ajoutées à l’interface utilisateur de Lecteur Windows Media. Le graphique peut être utilisé pour la publicité, fournir des informations et fournir un accès à des sites Web, pour nommer quelques possibilités.

utilisez l’élément **bannière** pour spécifier une image graphique (32 pixels de haut en 194 pixels de large) à afficher par Lecteur Windows Media. Le graphique est affiché sous tout le contenu de la vidéo. Un lien hypertexte peut être ajouté à la bannière à l’aide de l’élément enfant **moreinfo** .

Une info-bulle peut être définie par un élément **abstrait** au sein de la portée de l’élément **Banner** . Tout texte d’info-bulle défini peut être affiché en plaçant le pointeur de la souris sur le graphique de la bannière. Si vous sélectionnez le graphique de bannière avec le pointeur de la souris, tout lien hypertexte défini avec l’élément **moreinfo** est activé.

Le format de la **bannière** graphique par défaut est le format GIF. Le format JPG peut être utilisé si le graphique est correctement dimensionné.

L’exemple précédent illustre l’utilisation de l’élément **Banner** .

> [!Note]  
> les images de **bannière** ne sont pas prises en charge avec les fichiers DRM ou lorsque Lecteur Windows Media est incorporée dans une page web.

 

pour plus d’informations sur les bannières, consultez [graphiques personnalisés dans Lecteur Windows Media](custom-graphics-in-windows-media-player.md).

## <a name="moreinfo-properties"></a>Propriétés MOREINFO

Les zones de texte et d’image de l’interface utilisateur peuvent être associées à des URL. Pendant la lecture, les utilisateurs peuvent sélectionner l’une de ces sections pour se connecter à l’URL qui leur est associée dans leur navigateur Web. Par exemple, vous pouvez associer le site Web d’un annonceur à une image de bannière ad, comme illustré dans l’extrait de code suivant.


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>Texte abstrait

Le texte **abstrait** est utilisé pour afficher une brève description du texte ou des zones d’image de l’interface utilisateur à laquelle il est associé. Pendant la lecture, si le pointeur de la souris se trouve au-dessus de l’une de ces zones, une info-bulle s’affiche à côté du pointeur de la souris qui affiche le texte **abstrait** associé à la zone. Le texte **abstrait** est récupéré à partir d’un métafichier et est défini avec l’élément **abstrait** . L’élément **abstract** peut être un élément enfant d’un élément d' **entrée** ou de **bannière** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guide du métafichier multimédia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




