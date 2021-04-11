---
title: Utilisation du basculement de flux d’événements en temps réel
description: Utilisation du basculement de flux d’événements en temps réel
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
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
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190961"
---
# <a name="using-live-event-stream-switching"></a><span data-ttu-id="28af8-118">Utilisation du basculement de flux d’événements en temps réel</span><span class="sxs-lookup"><span data-stu-id="28af8-118">Using Live Event Stream Switching</span></span>

<span data-ttu-id="28af8-119">La diffusion multimédia en continu peut également être contrôlée par l’interaction des commandes de script incorporées dans un flux de média avec des éléments de métafichier Windows Media dans une sélection de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="28af8-119">Streaming media can also be controlled by the interaction of script commands embedded in a media stream with Windows Media metafile elements in a metafile playlist.</span></span>

<span data-ttu-id="28af8-120">Un événement est un type particulier de commande de script incorporé dans un flux multimédia ou un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="28af8-120">An event is a particular type of script command embedded in a media stream or media file.</span></span> <span data-ttu-id="28af8-121">Lorsque le contrôle du lecteur Windows Media reçoit la commande de script, il traite l’événement comme défini par l’élément d' **événement** dans la sélection du métafichier.</span><span class="sxs-lookup"><span data-stu-id="28af8-121">When the Windows Media Player control receives the script command, it processes the event as defined by the **EVENT** element in the metafile playlist.</span></span> <span data-ttu-id="28af8-122">Le lecteur Windows Media passe du flux actuel qu’il affiche et génère le rendu du contenu référencé dans l’élément d' **événement** de sélection de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="28af8-122">Windows Media Player switches from the current stream it is rendering and renders the content referenced in the metafile playlist **EVENT** element.</span></span> <span data-ttu-id="28af8-123">L’élément **Event** est généralement utilisé dans la production en direct.</span><span class="sxs-lookup"><span data-stu-id="28af8-123">The **EVENT** element is usually used in live production.</span></span>

<span data-ttu-id="28af8-124">Un élément d' **événement** ressemble à un élément d' **entrée** , mais chacun gère la lecture des flux et des fichiers multimédias différemment.</span><span class="sxs-lookup"><span data-stu-id="28af8-124">An **EVENT** element looks similar to an **ENTRY** element, but each handles the playback of streams and media files differently.</span></span> <span data-ttu-id="28af8-125">L’élément **entry** est utilisé pour créer des sélections.</span><span class="sxs-lookup"><span data-stu-id="28af8-125">The **ENTRY** element is used to create playlists.</span></span> <span data-ttu-id="28af8-126">Un fichier de flux ou de média référencé dans un élément d' **entrée** commence à être lu lorsque le flux ou le fichier multimédia référencé dans l' **entrée** précédente se termine.</span><span class="sxs-lookup"><span data-stu-id="28af8-126">A stream or media file referenced in an **ENTRY** element starts playing when the stream or media file referenced in the previous **ENTRY** finishes.</span></span> <span data-ttu-id="28af8-127">Un flux référencé dans un **événement** est lu uniquement lorsqu’une commande de script spécifique est reçue.</span><span class="sxs-lookup"><span data-stu-id="28af8-127">A stream referenced in an **EVENT** plays only when a specific script command is received.</span></span> <span data-ttu-id="28af8-128">Par exemple, lorsque le lecteur Windows Media reçoit une commande de script de type chaîne « EVENT » et la chaîne de commande « AdLINK », il recherche les éléments suivants dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="28af8-128">For example, when Windows Media Player receives a script command with type string "EVENT" and the command string "Adlink", it searches the playlist for the following elements.</span></span>


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



<span data-ttu-id="28af8-129">Le lecteur Windows Media passe alors du flux en direct pour lire le fichier de flux ou de média contenu dans l' **événement**, dans ce cas Adlink. WMA.</span><span class="sxs-lookup"><span data-stu-id="28af8-129">Windows Media Player then switches from the live stream to play the stream or media file contained in the **EVENT**, in this case Adlink.wma.</span></span> <span data-ttu-id="28af8-130">Le code `WHENDONE="RESUME"` indique au lecteur Windows Media de reprendre la lecture du flux précédent quand Adlink. WMA est terminé.</span><span class="sxs-lookup"><span data-stu-id="28af8-130">The code `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous stream when Adlink.wma is finished.</span></span>

> [!Note]  
> <span data-ttu-id="28af8-131">Si vous ne gérez pas chaque événement incorporé dans un flux multimédia ou un fichier multimédia, vous risquez d’obtenir des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="28af8-131">Failure to handle every event embedded in a media stream or media file may yield unexpected results.</span></span>

 

<span data-ttu-id="28af8-132">Si vous souhaitez utiliser le basculement de flux d’événements en temps réel, vous devez inclure un élément d' **événement** dans votre sélection pour gérer chaque commande de script d’événement incorporée dans les flux de média ou les fichiers multimédias de votre sélection.</span><span class="sxs-lookup"><span data-stu-id="28af8-132">If you want to use live event stream switching, you must include one **EVENT** element in your playlist to handle each event script command embedded in the media streams or media files in your playlist.</span></span> <span data-ttu-id="28af8-133">Avant de créer votre sélection, vous devez connaître les détails sur les commandes de script incorporées dans votre contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="28af8-133">Before you create your playlist, you must know the details about which script commands are embedded in your digital media content.</span></span> <span data-ttu-id="28af8-134">S’il existe une commande de script d’événement que vous souhaitez que le lecteur Windows Media ignore, incluez un élément d' **événement** dans votre sélection pour gérer l’événement, mais faites référence à une URL factice dans le gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="28af8-134">If there is an event script command that you want Windows Media Player to ignore, include an **EVENT** element in your playlist to handle the event, but reference a dummy URL in the event handler.</span></span>

## <a name="ad-insertion"></a><span data-ttu-id="28af8-135">Insertion de publicité</span><span class="sxs-lookup"><span data-stu-id="28af8-135">Ad Insertion</span></span>

<span data-ttu-id="28af8-136">Cette technique peut être utilisée pour l’insertion d’AD.</span><span class="sxs-lookup"><span data-stu-id="28af8-136">This technique can be used for ad insertion.</span></span> <span data-ttu-id="28af8-137">Par exemple, lors d’une diffusion en direct sur Internet d’un jeu de billes, une commande peut être envoyée au début de chaque pause commerciale qui indique à chaque client (lecteur Windows Media) de lire les commerciaux figurant dans sa playlist.</span><span class="sxs-lookup"><span data-stu-id="28af8-137">For example, during a live Internet broadcast of a ball game, a command can be sent at the beginning of every commercial break that instructs each client (Windows Media Player) to play commercials listed in its playlist.</span></span> <span data-ttu-id="28af8-138">Lorsque les clients terminent la lecture des publicités, la playlist demande à chaque client de repasser à la diffusion en direct.</span><span class="sxs-lookup"><span data-stu-id="28af8-138">When clients finish playing the commercials, the playlist instructs each client to cut back to the live broadcast.</span></span> <span data-ttu-id="28af8-139">Le contenu du support d' **événement** est rendu uniquement lorsque le média de diffusion en continu qui est accédé diffuse des scripts incorporés avec le nom d' **événement** correspondant.</span><span class="sxs-lookup"><span data-stu-id="28af8-139">The **EVENT** media content will be rendered only when the streaming media being accessed broadcasts embedded scripting with the matching **EVENT** name.</span></span>

<span data-ttu-id="28af8-140">Les possibilités inhérentes au basculement d' **événements** sont plus appréciées en comparant la façon dont les publicités atteignent les visionneuses par le biais d’une diffusion standard, par voie hertzienne, avec la manière dont les publicités peuvent atteindre les spectateurs à l’aide des technologies Windows Media.</span><span class="sxs-lookup"><span data-stu-id="28af8-140">The possibilities inherent in **EVENT** switching are best appreciated by contrasting how ads reach viewers through standard, over-the-air broadcasting with how ads can reach viewers using Windows Media Technologies.</span></span> <span data-ttu-id="28af8-141">Historiquement, les annonces Broadcast pouvaient uniquement être ciblées à peu près sur les spectateurs, en utilisant les données de classement comme critère principal.</span><span class="sxs-lookup"><span data-stu-id="28af8-141">Historically, broadcast ads could only be roughly targeted at viewers, using ratings data as the primary criteria.</span></span> <span data-ttu-id="28af8-142">Les publicités envoyées à l’aide des technologies Windows Media peuvent être destinées directement à l’utilisateur cible, car les **événements** et les sélections peuvent être créés à la volée en fonction de l’entrée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="28af8-142">Ads sent using Windows Media Technologies can be aimed directly at the target user because **EVENTs** and playlists can be built on the fly based on user input.</span></span> <span data-ttu-id="28af8-143">Pour plus d’informations, consultez Personnalisation de la [distribution des médias](personalizing-media-delivery.md).</span><span class="sxs-lookup"><span data-stu-id="28af8-143">For more information, see [Personalizing Media Delivery](personalizing-media-delivery.md).</span></span>

<span data-ttu-id="28af8-144">Vous pouvez également utiliser des sélections de métafichiers pour afficher des graphiques, du son et du texte personnalisés pour la publicité.</span><span class="sxs-lookup"><span data-stu-id="28af8-144">You can also use metafile playlists to display customized graphics, audio and text for advertising.</span></span> <span data-ttu-id="28af8-145">Vous pouvez utiliser l’élément **bannière** comme élément enfant d’un **événement** pour afficher un graphique de message publicitaire.</span><span class="sxs-lookup"><span data-stu-id="28af8-145">You can use the **BANNER** element as a child element of an **EVENT** to display an advertising message graphic.</span></span> <span data-ttu-id="28af8-146">L’élément **Banner** fournit le chemin d’accès et le fichier contenant les graphiques de votre bannière publicitaire.</span><span class="sxs-lookup"><span data-stu-id="28af8-146">The **BANNER** element provides the path and file containing the graphics for your advertising banner.</span></span> <span data-ttu-id="28af8-147">Vous pouvez également fournir un lien vers un site ou un fichier à l’aide de l’élément enfant **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="28af8-147">You can also provide a link to a site or file using the **MOREINFO** child element.</span></span> <span data-ttu-id="28af8-148">L’URL de l’élément **moreinfo** peut fournir un lien vers d’autres publications sur le Web.</span><span class="sxs-lookup"><span data-stu-id="28af8-148">The URL in the **MOREINFO** element can provide a link to even more advertisements on the Web.</span></span> <span data-ttu-id="28af8-149">L’exemple suivant illustre l’utilisation de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="28af8-149">The following example demonstrates using these elements.</span></span>

<span data-ttu-id="28af8-150">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="28af8-150">Example Code</span></span>


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



<span data-ttu-id="28af8-151">L’exemple suivant insère le. WMA ad dans le flux de diffusion en continu de diffusion BallGame lorsqu’un client reçoit un **événement** de commande de script avec l’attribut de **nom** défini sur « délai d’attente ».</span><span class="sxs-lookup"><span data-stu-id="28af8-151">The following example inserts the ad Advert.wma into the broadcast unicast stream BallGame when a client receives a script command **EVENT** with the **NAME** attribute set to "Time-Out".</span></span> <span data-ttu-id="28af8-152">**CLIENTSKIP** est défini sur non pour empêcher la publicité diffusée en continu d’être ignorée.</span><span class="sxs-lookup"><span data-stu-id="28af8-152">**CLIENTSKIP** is set to NO to prevent the streamed ad from being skipped.</span></span> <span data-ttu-id="28af8-153">Dans cet exemple, la publicité diffusée en continu doit être lue avant de retourner au flux d’origine.</span><span class="sxs-lookup"><span data-stu-id="28af8-153">In this example, the streamed ad must be played before returning to the original stream.</span></span> <span data-ttu-id="28af8-154">Une fois la publicité terminée, le client reprend le flux d’origine.</span><span class="sxs-lookup"><span data-stu-id="28af8-154">When the ad is finished, the client resumes playing the original stream.</span></span>

<span data-ttu-id="28af8-155">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="28af8-155">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="28af8-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28af8-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28af8-157">**Sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="28af8-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="28af8-158">**Utilisation des sélections de métafichiers**</span><span class="sxs-lookup"><span data-stu-id="28af8-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="28af8-159">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="28af8-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="28af8-160">**Guide des métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="28af8-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




