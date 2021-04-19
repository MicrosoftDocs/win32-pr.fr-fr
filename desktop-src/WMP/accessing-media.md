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
# <a name="accessing-media"></a><span data-ttu-id="fea79-123">Accès au média</span><span class="sxs-lookup"><span data-stu-id="fea79-123">Accessing Media</span></span>

<span data-ttu-id="fea79-124">Utilisez des sélections pour spécifier et contrôler la diffusion multimédia en continu ou les fichiers multimédias lus par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fea79-124">Use playlists to specify and to control the streaming media or media files that Windows Media Player plays.</span></span>

<span data-ttu-id="fea79-125">Utilisez l’élément **entry** pour spécifier un élément Media unique (un fichier multimédia ou un flux en direct) et tous les éléments enfants (tels que des images, des liens **moreinfo** et du texte **abstrait** ).</span><span class="sxs-lookup"><span data-stu-id="fea79-125">Use the **ENTRY** element to specify a single media element (a media file or a live stream) and any child elements (such as images, **MOREINFO** links, and **ABSTRACT** text).</span></span> <span data-ttu-id="fea79-126">Utilisez un élément **ENTRYREF** pour spécifier une sélection.</span><span class="sxs-lookup"><span data-stu-id="fea79-126">Use an **ENTRYREF** element to specify a playlist.</span></span> <span data-ttu-id="fea79-127">Une sélection peut contenir un ou plusieurs éléments d' **entrée** ou de **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="fea79-127">A playlist can contain one or more **ENTRY** or **ENTRYREF** elements.</span></span> <span data-ttu-id="fea79-128">Le lecteur Windows Media exécute une sélection en commençant par la première entrée, puis en lisant chaque entrée jusqu’à ce que la liste soit terminée.</span><span class="sxs-lookup"><span data-stu-id="fea79-128">Windows Media Player executes a playlist by starting with the first entry and then playing each entry in turn until the list is finished.</span></span>

<span data-ttu-id="fea79-129">Un élément d' **entrée** peut pointer vers n’importe quel type de média que le lecteur Windows Media peut lire.</span><span class="sxs-lookup"><span data-stu-id="fea79-129">An **ENTRY** element can point to any type of media that Windows Media Player can play.</span></span> <span data-ttu-id="fea79-130">Cela comprend non seulement les fichiers. WMA,. wmv,. ASF et. avi, mais également des flux en direct.</span><span class="sxs-lookup"><span data-stu-id="fea79-130">This includes not only .wma, .wmv, .asf, and .avi files, to name a few, but live streams as well.</span></span> <span data-ttu-id="fea79-131">En utilisant une série d’éléments d' **entrée** ou de **ENTRYREF** pour référencer du contenu multimédia, vous pouvez utiliser une sélection pour envoyer un flux unique constitué de plusieurs sources.</span><span class="sxs-lookup"><span data-stu-id="fea79-131">By using a series of **ENTRY** or **ENTRYREF** elements to reference media content, you can use a playlist to send a single stream that consists of multiple sources.</span></span> <span data-ttu-id="fea79-132">Les flux référencés sont lus de manière séquentielle et considérés comme un flux continu par la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="fea79-132">The referenced streams will play sequentially and be seen as one continuous stream by the viewer.</span></span> <span data-ttu-id="fea79-133">Par exemple, la sélection peut contenir deux éléments d' **entrée** : une présentation standard d’un fichier Windows Media avec une extension. WMA et un flux Windows Media en direct.</span><span class="sxs-lookup"><span data-stu-id="fea79-133">For example, the playlist can contain two **ENTRY** elements: a standard introduction from a Windows Media file with a .wma extension, and a live Windows Media stream.</span></span>

> [!Note]  
> <span data-ttu-id="fea79-134">Une sélection ne doit pas contenir de liens vers des fichiers multimédias dont le contenu est créé avec des versions différentes de la Rights Management numérique (DRM).</span><span class="sxs-lookup"><span data-stu-id="fea79-134">A playlist must not contain links to media files that have content created with different versions of Digital Rights Management (DRM).</span></span> <span data-ttu-id="fea79-135">Dans une sélection de métafichiers, s’il existe des liens vers des fichiers multimédias avec un contenu DRM version 1 et des fichiers multimédias créés avec des versions DRM ultérieures, le lecteur Windows Media ne lira que le contenu DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="fea79-135">In a metafile playlist, if there are links for media files with DRM version 1 content and for media files created with later DRM versions, Windows Media Player will only play the DRM version 1 content.</span></span>

 

## <a name="controlling-playback"></a><span data-ttu-id="fea79-136">Contrôle de la lecture</span><span class="sxs-lookup"><span data-stu-id="fea79-136">Controlling Playback</span></span>

<span data-ttu-id="fea79-137">Utilisez des sélections pour contrôler non seulement quel clip multimédia est lu, mais également quelles parties du clip sont lues et comment.</span><span class="sxs-lookup"><span data-stu-id="fea79-137">Use playlists to control not only which media clip is played, but also which portions of the clip are played and how.</span></span> <span data-ttu-id="fea79-138">Vous pouvez utiliser des sélections pour définir un ensemble de clips à boucler ou à répéter, pour définir la durée de lecture et pour affecter des heures de début et des marqueurs de début et de fin pour chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="fea79-138">You can use playlists to define a set of clips to be looped or repeated, to set the duration of play, and to assign start times, and start and end markers for each entry.</span></span> <span data-ttu-id="fea79-139">Les éléments **StartTime**, **STARTMARKER** et **ENDMARKER** fonctionnent conjointement avec les marqueurs dans le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="fea79-139">The **STARTTIME**, **STARTMARKER**, and **ENDMARKER** elements work in conjunction with markers in the media file.</span></span>

<span data-ttu-id="fea79-140">Par exemple, la sélection suivante utilise une bannière ad et le lien **moreinfo** associé dans une **entrée**, et fait référence à un **STARTMARKER** et à **ENDMARKER**.</span><span class="sxs-lookup"><span data-stu-id="fea79-140">For example, the following playlist uses an ad banner and the associated **MOREINFO** link in one **ENTRY**, and references a **STARTMARKER** and **ENDMARKER**.</span></span>


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



## <a name="setting-duration"></a><span data-ttu-id="fea79-141">Définition de la durée</span><span class="sxs-lookup"><span data-stu-id="fea79-141">Setting Duration</span></span>

<span data-ttu-id="fea79-142">Utilisez l’élément **Duration** pour spécifier la durée de lecture d’un clip ou d’un ensemble de clips.</span><span class="sxs-lookup"><span data-stu-id="fea79-142">Use the **DURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="fea79-143">Vous pouvez également utiliser l’attribut **PREVIEWMODE** de l’élément **ASX** conjointement avec l’élément **PREVIEWDURATION** pour spécifier la durée de lecture d’un clip ou d’un ensemble de clips.</span><span class="sxs-lookup"><span data-stu-id="fea79-143">You can also use the **PREVIEWMODE** attribute of the **ASX** element in conjunction with the **PREVIEWDURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="fea79-144">Définissez l’attribut **PREVIEWMODE** sur Oui pour utiliser l’élément **PREVIEWDURATION** pour spécifier la durée pendant laquelle le clip associé doit être lu.</span><span class="sxs-lookup"><span data-stu-id="fea79-144">Set the **PREVIEWMODE** attribute to YES to use the **PREVIEWDURATION** element to specify how long to play the associated clip.</span></span> <span data-ttu-id="fea79-145">Les éléments **PREVIEWDURATION** et **Duration** ont le même comportement.</span><span class="sxs-lookup"><span data-stu-id="fea79-145">The **PREVIEWDURATION** and **DURATION** elements have the same behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fea79-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fea79-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fea79-147">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="fea79-147">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="fea79-148">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="fea79-148">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="fea79-149">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fea79-149">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="fea79-150">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fea79-150">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




