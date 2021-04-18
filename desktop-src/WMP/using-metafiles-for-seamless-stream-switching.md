---
title: Utilisation de safiles pour basculer en continu
description: Utilisation de safiles pour basculer en continu
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Sélections de métafichiers Windows Media, basculement de flux d’événements en direct
- sélections, basculement de flux d’événements en direct
- sélections de métafichiers, basculement de flux d’événements en direct
- Sélections de métafichiers Windows Media, basculement de flux d’événements
- sélections, basculement de flux d’événements
- sélections de métafichiers, basculement de flux d’événements
- Sélections de métafichiers Windows Media, insertion de publicités
- sélections, insertion de publicités
- sélections de métafichiers, insertion de publicités
- Windows Media Player, basculement de flux d’événements en direct
- Lecteur Windows Media, basculement de flux d’événements
- Windows Media Player, insertion de publicités
- basculement de flux d’événements en direct
- basculement de flux d’événements
- insertion de publicité
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512028"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a><span data-ttu-id="22904-118">Utilisation de safiles pour basculer en continu</span><span class="sxs-lookup"><span data-stu-id="22904-118">Using Metafiles for Seamless Stream Switching</span></span>

<span data-ttu-id="22904-119">Vous pouvez faciliter le basculement continu de flux à l’aide de sélections de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="22904-119">You can facilitate seamless stream switching using metafile playlists.</span></span> <span data-ttu-id="22904-120">En général, lorsqu’une partie du contenu se termine, la mise en mémoire tampon se produit pour le clip ou le flux suivant avant son ouverture (s’il s’agit d’un contenu reçu à partir d’un serveur multimédia de diffusion en continu).</span><span class="sxs-lookup"><span data-stu-id="22904-120">Usually, when a piece of content ends, buffering occurs for the next clip or stream before it opens (if it is content received from a streaming media server).</span></span> <span data-ttu-id="22904-121">Microsoft Windows Media Services vous permet d’éliminer ou de réduire au minimum le temps de mise en mémoire tampon et de faire en sorte qu’une autre partie du contenu diffusé en continu commence à s’exécuter presque immédiatement.</span><span class="sxs-lookup"><span data-stu-id="22904-121">Microsoft Windows Media Services enables you to eliminate, or at least minimize, this buffering time and have another piece of streamed content begin playing nearly immediately.</span></span> <span data-ttu-id="22904-122">Le mode de fonctionnement normal pour le lecteur Windows Media est d’ouvrir le flux multimédia suivant référencé par la sélection 20 secondes avant la fin du flux actuellement affiché.</span><span class="sxs-lookup"><span data-stu-id="22904-122">The normal mode of operation for Windows Media Player is to open the next media stream referenced by the playlist 20 seconds before the end of the currently rendered stream.</span></span> <span data-ttu-id="22904-123">Cela fournit généralement une transition transparente entre les flux multimédias, en fonction d’autres facteurs tels que les temps d’accès au Web.</span><span class="sxs-lookup"><span data-stu-id="22904-123">This generally provides a seamless transition between media streams, depending on other factors such as Web access times.</span></span>

<span data-ttu-id="22904-124">Utilisez l’élément **Event** dans une sélection conjointement avec les commandes OPENEVENT de l’encodeur pour faciliter le basculement transparent entre les flux ou les fichiers.</span><span class="sxs-lookup"><span data-stu-id="22904-124">Use the **EVENT** element in a playlist in conjunction with OPENEVENT commands from the encoder to facilitate seamless switching between streams or files.</span></span> <span data-ttu-id="22904-125">L’envoi d’une commande OPENEVENT 20 secondes ou plus avant la commande EVENT peut réduire les retards dans le basculement de flux.</span><span class="sxs-lookup"><span data-stu-id="22904-125">Sending an OPENEVENT command 20 seconds or more prior to the EVENT command can minimize delays in stream switching.</span></span> <span data-ttu-id="22904-126">Le lecteur Windows Media est ensuite en mesure de précharger une partie du contenu de diffusion en continu à venir dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="22904-126">Then Windows Media Player is able to preload a portion of the upcoming streaming content into a buffer.</span></span>

<span data-ttu-id="22904-127">Utilisez l’encodeur Windows Media pour envoyer une commande de script dans le flux en utilisant le format suivant :</span><span class="sxs-lookup"><span data-stu-id="22904-127">Use Windows Media Encoder to send a script command in the stream using the following format:</span></span>


```XML
OPENEVENT eventname 

```



<span data-ttu-id="22904-128">Le nom de l’événement doit être celui défini dans l’élément **événement** de la sélection.</span><span class="sxs-lookup"><span data-stu-id="22904-128">The event name must be the one defined in the **EVENT** element in the playlist.</span></span> <span data-ttu-id="22904-129">Lorsque le lecteur Windows Media reçoit une commande de script OPENEVENT à partir de l’encodeur, il recherche l’élément d' **événement** dans la sélection et commence la mise en mémoire tampon du clip ou du flux défini dans l’élément **Event** .</span><span class="sxs-lookup"><span data-stu-id="22904-129">When Windows Media Player receives an OPENEVENT script command from the encoder, it looks to the **EVENT** element in the playlist and begins buffering the clip or stream defined in the **EVENT** element.</span></span> <span data-ttu-id="22904-130">Le lecteur Windows Media contient ensuite ces informations jusqu’à l’événement réel du même nom.</span><span class="sxs-lookup"><span data-stu-id="22904-130">Windows Media Player then holds this information until the actual event of the same name.</span></span> <span data-ttu-id="22904-131">Lorsque l’événement nommé est reçu, le lecteur Windows Media bascule vers ce contenu précédemment mis en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="22904-131">When the named event is received, Windows Media Player switches to that previously buffered content.</span></span>

> [!Note]  
> <span data-ttu-id="22904-132">Vous ne pouvez pas utiliser de caractères Unicode pour la commande de script OPENEVENT dans le fichier multimédia ou l’élément d' **événement** dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="22904-132">You cannot use Unicode characters for the OPENEVENT script command in the media file or the **EVENT** element in the playlist.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="22904-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22904-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22904-134">**Création de sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="22904-134">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="22904-135">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="22904-135">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="22904-136">**Événement Player. commande**</span><span class="sxs-lookup"><span data-stu-id="22904-136">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="22904-137">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="22904-137">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="22904-138">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="22904-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="22904-139">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="22904-139">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




