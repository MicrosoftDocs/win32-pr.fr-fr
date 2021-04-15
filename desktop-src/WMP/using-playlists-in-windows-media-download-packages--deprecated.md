---
title: Utilisation des sélections dans les packages de téléchargement Windows Media (déconseillés)
description: Utilisation des sélections dans les packages de téléchargement Windows Media (déconseillés)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Fichiers Windows Media, packages de téléchargement Windows Media
- Windows Media Player, packages de téléchargement Windows Media
- sous-fichiers, packages de téléchargement Windows Media
- Windows Media, packages de téléchargement Windows Media
- sélections, packages de téléchargement Windows Media
- sélections de métafichiers, packages de téléchargement Windows Media
- Sélections de métafichiers Windows Media, packages de téléchargement Windows Media
- Packages de téléchargement Windows Media, sélections
- Packages de téléchargement Windows Media, sélections de métafichiers
- Packages de téléchargement Windows Media, sélections de métafichiers Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380200"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>Utilisation des sélections dans les packages de téléchargement Windows Media (déconseillés)

Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.

Les sélections sont des sous-fichiers Windows Media avec une extension de nom de fichier. asx qui fournissent des informations qui indiquent au lecteur Windows Media comment lire le contenu empaqueté. En combinant plusieurs fichiers de contenu dans un package de téléchargement Windows Media unique, vous pouvez contrôler et personnaliser votre package de téléchargement Windows Media à l’aide de la sélection.

> [!Note]  
> En général, les sélections de métafichiers sont utilisées par les packages de téléchargement Windows Media pour référencer le contenu multimédia du package plutôt qu’un flux à partir d’un serveur sur un intranet ou sur Internet. Toutefois, les références d’URL dans le fichier. asx sont prises en charge.

 

À l’aide de XML, le métafichier fournit les informations utilisées par le lecteur Windows Media pour lire et afficher le contenu. Les sélections sont composées de différents éléments de code XML avec leurs balises et attributs associés. Chaque élément d’une sélection de métafichier Windows Media définit un paramètre ou une action spécifique dans le lecteur Windows Media.

L’ordinateur de l’utilisateur associe un métafichier Windows Media ayant une extension de nom de fichier. asx au lecteur Windows Media. Le lecteur Windows Media ouvre et analyse le code XML dans le métafichier, qui contient le chemin d’accès pour localiser les fichiers audio ou vidéo empaquetés. Le script Metafile contrôle ensuite l’expérience audio, vidéo et graphique. Le métafichier contient également des informations que le lecteur Windows Media traite et affiche dans la zone de liste déroulante playlist. Immédiatement après l’affichage de la liste, le premier élément de la liste est lu.

Une sélection de métafichiers est un raccourci vers les fichiers qui contiennent votre contenu empaqueté. Le code suivant est un exemple de métafichier qui spécifie la bordure à afficher à l’aide de l’élément **Skin** , de deux chansons à lire et des informations de sélection pour chaque chanson.


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Bordures du lecteur Windows Media (déconseillée)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Packages de téléchargement Windows Media (déconseillés)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Fichiers Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




