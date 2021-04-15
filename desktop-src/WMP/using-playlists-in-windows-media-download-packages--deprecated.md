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
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="50057-113">Utilisation des sélections dans les packages de téléchargement Windows Media (déconseillés)</span><span class="sxs-lookup"><span data-stu-id="50057-113">Using Playlists in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="50057-114">Cette page décrit une fonctionnalité qui peut ne pas être disponible dans les versions ultérieures du lecteur Windows Media et du kit de développement logiciel (SDK) du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50057-114">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="50057-115">Les sélections sont des sous-fichiers Windows Media avec une extension de nom de fichier. asx qui fournissent des informations qui indiquent au lecteur Windows Media comment lire le contenu empaqueté.</span><span class="sxs-lookup"><span data-stu-id="50057-115">Playlists are Windows Media metafiles with an .asx file name extension that provide information that tells Windows Media Player how to play the packaged content.</span></span> <span data-ttu-id="50057-116">En combinant plusieurs fichiers de contenu dans un package de téléchargement Windows Media unique, vous pouvez contrôler et personnaliser votre package de téléchargement Windows Media à l’aide de la sélection.</span><span class="sxs-lookup"><span data-stu-id="50057-116">By combining multiple content files into a single Windows Media Download package, you can control and customize your Windows Media Download package by using the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="50057-117">En général, les sélections de métafichiers sont utilisées par les packages de téléchargement Windows Media pour référencer le contenu multimédia du package plutôt qu’un flux à partir d’un serveur sur un intranet ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="50057-117">In general, metafile playlists are used by Windows Media Download packages to reference the multimedia content in the package rather than a stream from a server on an intranet or the Internet.</span></span> <span data-ttu-id="50057-118">Toutefois, les références d’URL dans le fichier. asx sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="50057-118">However, URL references within the .asx file are supported.</span></span>

 

<span data-ttu-id="50057-119">À l’aide de XML, le métafichier fournit les informations utilisées par le lecteur Windows Media pour lire et afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="50057-119">Using XML, the metafile provides the information Windows Media Player uses to play and display content.</span></span> <span data-ttu-id="50057-120">Les sélections sont composées de différents éléments de code XML avec leurs balises et attributs associés.</span><span class="sxs-lookup"><span data-stu-id="50057-120">Playlists are made up of various XML code elements with their associated tags and attributes.</span></span> <span data-ttu-id="50057-121">Chaque élément d’une sélection de métafichier Windows Media définit un paramètre ou une action spécifique dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50057-121">Each element in a Windows Media metafile playlist defines a particular setting or action in Windows Media Player.</span></span>

<span data-ttu-id="50057-122">L’ordinateur de l’utilisateur associe un métafichier Windows Media ayant une extension de nom de fichier. asx au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="50057-122">The user's computer associates a Windows Media metafile that has an .asx file name extension with Windows Media Player.</span></span> <span data-ttu-id="50057-123">Le lecteur Windows Media ouvre et analyse le code XML dans le métafichier, qui contient le chemin d’accès pour localiser les fichiers audio ou vidéo empaquetés.</span><span class="sxs-lookup"><span data-stu-id="50057-123">Windows Media Player opens and parses the XML code in the metafile, which contains the path for locating the packaged audio or video files.</span></span> <span data-ttu-id="50057-124">Le script Metafile contrôle ensuite l’expérience audio, vidéo et graphique.</span><span class="sxs-lookup"><span data-stu-id="50057-124">The metafile script then controls the audio, video, and graphical experience.</span></span> <span data-ttu-id="50057-125">Le métafichier contient également des informations que le lecteur Windows Media traite et affiche dans la zone de liste déroulante playlist.</span><span class="sxs-lookup"><span data-stu-id="50057-125">The metafile also contains information that Windows Media Player processes and displays in the playlist drop-down box.</span></span> <span data-ttu-id="50057-126">Immédiatement après l’affichage de la liste, le premier élément de la liste est lu.</span><span class="sxs-lookup"><span data-stu-id="50057-126">Immediately after the list is displayed, the first item in the list is played.</span></span>

<span data-ttu-id="50057-127">Une sélection de métafichiers est un raccourci vers les fichiers qui contiennent votre contenu empaqueté.</span><span class="sxs-lookup"><span data-stu-id="50057-127">A metafile playlist is a shortcut to the files that contain your packaged content.</span></span> <span data-ttu-id="50057-128">Le code suivant est un exemple de métafichier qui spécifie la bordure à afficher à l’aide de l’élément **Skin** , de deux chansons à lire et des informations de sélection pour chaque chanson.</span><span class="sxs-lookup"><span data-stu-id="50057-128">The following code is an example of a metafile that specifies the border to display by using the **SKIN** element, two songs to be played, and the playlist information for each song.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="50057-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50057-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50057-130">**Bordures du lecteur Windows Media (déconseillée)**</span><span class="sxs-lookup"><span data-stu-id="50057-130">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="50057-131">**Packages de téléchargement Windows Media (déconseillés)**</span><span class="sxs-lookup"><span data-stu-id="50057-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="50057-132">**Fichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="50057-132">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




