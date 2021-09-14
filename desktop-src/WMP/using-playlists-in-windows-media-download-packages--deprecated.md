---
title: utilisation des sélections dans les Packages de téléchargement de médias Windows (déconseillés)
description: utilisation des sélections dans les Packages de téléchargement de médias Windows (déconseillés)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Windows fichiers multimédias, Windows les packages de téléchargement de média
- Lecteur Windows Media, Windows les packages de téléchargement de médias
- sous-fichiers, packages de téléchargement de médias Windows
- Windows médias, Windows les packages de téléchargement de média
- sélections, Windows les packages de téléchargement de médias
- sélections de métafichiers, packages de téléchargement de médias Windows
- Windows sélections de métafichiers multimédia, packages de téléchargement de médias Windows
- Windows Packages de téléchargement de médias, sélections
- Windows Packages de téléchargement de médias, playlists de métafichiers
- Windows packages de téléchargement de médias, Windows les sélections de métafichiers multimédia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311086"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>utilisation des sélections dans les Packages de téléchargement de médias Windows (déconseillés)

cette page documente une fonctionnalité qui peut ne pas être disponible dans les futures versions de Lecteur Windows Media et le kit de développement logiciel (SDK) Lecteur Windows Media.

les sélections sont Windows les sous-fichiers multimédias avec une extension de nom de fichier. asx fournissant des informations qui indiquent Lecteur Windows Media comment lire le contenu empaqueté. en combinant plusieurs fichiers de contenu dans un seul Windows package de téléchargement multimédia, vous pouvez contrôler et personnaliser votre package de téléchargement Windows media à l’aide de la sélection.

> [!Note]  
> en général, les sélections de métafichiers sont utilisées par les packages de téléchargement de médias Windows pour référencer le contenu multimédia du package plutôt qu’un flux à partir d’un serveur sur un intranet ou sur Internet. Toutefois, les références d’URL dans le fichier. asx sont prises en charge.

 

à l’aide de XML, le métafichier fournit les informations que Lecteur Windows Media utilise pour lire et afficher le contenu. Les sélections sont composées de différents éléments de code XML avec leurs balises et attributs associés. chaque élément d’une sélection Windows métafichier multimédia définit un paramètre ou une action spécifique dans Lecteur Windows Media.

l’ordinateur de l’utilisateur associe un métafichier Windows Media ayant une extension de nom de fichier. asx à Lecteur Windows Media. Lecteur Windows Media ouvre et analyse le code XML dans le métafichier, qui contient le chemin d’accès pour localiser les fichiers audio ou vidéo empaquetés. Le script Metafile contrôle ensuite l’expérience audio, vidéo et graphique. le métafichier contient également des informations qui Lecteur Windows Media processus et s’affichent dans la zone de liste déroulante playlist. Immédiatement après l’affichage de la liste, le premier élément de la liste est lu.

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

[**bordures pour la Lecteur Windows Media (déconseillée)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Packages de téléchargement de médias (déconseillés)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Fichiers multimédias**](windows-media-metafiles.md)
</dt> </dl>

 

 




