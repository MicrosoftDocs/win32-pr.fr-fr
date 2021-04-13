---
title: Exemple de sélection de station de radio
description: Exemple de sélection de station de radio
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Sélections de métafichiers Windows Media, exemples de sélection
- sélections, exemples de sélection
- sélections de métafichiers, exemples de sélection
- Sélections de métafichiers Windows Media, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Sélections de métafichiers Windows Media, exemples de sélections
- sélections, exemples de sélections
- sélections de métafichiers, exemples de sélections
- Sélections de métafichiers Windows Media, exemple de code
- sélections, exemple de code
- sélections de métafichiers, exemple de code
- Sélections de métafichiers Windows Media, exemple de sélection de station de radio
- sélections, exemple de sélection de station de radio
- sélections de métafichiers, exemple de sélection de station de radio
- Windows Media Player, exemples de sélection
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemples de sélections
- Lecteur Windows Media, exemple de sélection de station de radio
- exemples de sélection
- exemples de sélections
- exemples de sélections
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379820"
---
# <a name="an-example-radio-station-playlist"></a><span data-ttu-id="9aa23-125">Exemple de sélection de station de radio</span><span class="sxs-lookup"><span data-stu-id="9aa23-125">An Example Radio Station Playlist</span></span>

<span data-ttu-id="9aa23-126">L’exemple de code suivant montre comment créer une sélection pour analyser trois stations de radio Rock.</span><span class="sxs-lookup"><span data-stu-id="9aa23-126">The following example code illustrates how to create a playlist to scan three rock radio stations.</span></span> <span data-ttu-id="9aa23-127">La société fictive Adventure Works radio figure sur la sélection et sur tous les flux individuels de la playlist.</span><span class="sxs-lookup"><span data-stu-id="9aa23-127">The fictitious company Adventure Works Radio brand is on the playlist and on all of the individual streams within the playlist.</span></span> <span data-ttu-id="9aa23-128">Lorsque vous écrivez votre code, remplacez toutes les URL et tous les noms de fichiers par des noms de fichiers valides accessibles à votre lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9aa23-128">When you write your code, change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="9aa23-129">Une sélection est créée pour chacune des stations.</span><span class="sxs-lookup"><span data-stu-id="9aa23-129">A playlist is created for each of the stations.</span></span> <span data-ttu-id="9aa23-130">Une quatrième playlist balaie les trois premières.</span><span class="sxs-lookup"><span data-stu-id="9aa23-130">A fourth playlist scans through the first three.</span></span> <span data-ttu-id="9aa23-131">Les sélections sont créées pour référencer des publications générées de manière dynamique et avoir la personnalisation radio d’Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="9aa23-131">The playlists are created to reference dynamically generated advertisements and have Adventure Works Radio branding.</span></span>

<span data-ttu-id="9aa23-132">L’une des sélections représentant une station de radio peut se présenter comme suit.</span><span class="sxs-lookup"><span data-stu-id="9aa23-132">One of the playlists representing a radio station might look like this.</span></span>


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="9aa23-133">La sélection peut ensuite être constituée de références à des sélections individuelles.</span><span class="sxs-lookup"><span data-stu-id="9aa23-133">The playlist can then be constructed of references to the individual playlists.</span></span>

<span data-ttu-id="9aa23-134">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="9aa23-134">Example Code</span></span>


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



<span data-ttu-id="9aa23-135">Dans cet exemple, une publicité est suivie de 30 secondes de chacune des trois stations référencées, l’une après l’autre.</span><span class="sxs-lookup"><span data-stu-id="9aa23-135">This example would play an ad followed by 30 seconds of each of the three stations referenced, one after the other.</span></span> <span data-ttu-id="9aa23-136">Ce cycle se répète indéfiniment, car l’attribut **Count** de l’élément **REPEAT** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="9aa23-136">This cycle will repeat indefinitely because the **COUNT** attribute of the **REPEAT** element is not defined.</span></span>

-   <span data-ttu-id="9aa23-137">Les exemples de sociétés, organisations, produits, personnes et événements utilisés dans les exemples sont fictifs.</span><span class="sxs-lookup"><span data-stu-id="9aa23-137">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="9aa23-138">Toute ressemblance avec des noms ou des événements réels est purement fortuite et involontaire.</span><span class="sxs-lookup"><span data-stu-id="9aa23-138">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9aa23-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9aa23-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aa23-140">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="9aa23-140">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="9aa23-141">**Exemples de sélections**</span><span class="sxs-lookup"><span data-stu-id="9aa23-141">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="9aa23-142">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="9aa23-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="9aa23-143">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9aa23-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="9aa23-144">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9aa23-144">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




