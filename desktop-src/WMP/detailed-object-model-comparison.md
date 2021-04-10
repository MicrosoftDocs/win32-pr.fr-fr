---
title: Comparaison du modèle d’objet détaillé
description: Comparaison du modèle d’objet détaillé
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Lecteur Windows Media, modèle objet
- Modèle d’objet du lecteur Windows Media, différences entre les versions
- modèle objet, différences de version
- Contrôle ActiveX du lecteur Windows Media, différences entre les versions
- Contrôle ActiveX, différences de version
- Windows Media Player Mobile contrôle ActiveX, différences de version
- Windows Media Player Mobile, modèle objet
- Guide de migration, différences de version
- versions du lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104030749"
---
# <a name="detailed-object-model-comparison"></a><span data-ttu-id="66d89-112">Comparaison du modèle d’objet détaillé</span><span class="sxs-lookup"><span data-stu-id="66d89-112">Detailed Object Model Comparison</span></span>

<span data-ttu-id="66d89-113">Le tableau suivant compare les propriétés du modèle d’objet du lecteur Windows Media 6,4 au modèle objet Windows Media Player 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="66d89-113">The following table compares the Windows Media Player 6.4 object model properties with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66d89-114">Windows Media Player 6,4, propriété</span><span class="sxs-lookup"><span data-stu-id="66d89-114">Windows Media Player 6.4 property</span></span></th>
<th><span data-ttu-id="66d89-115">Windows Media Player 7 ou une version ultérieure équivalente</span><span class="sxs-lookup"><span data-stu-id="66d89-115">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66d89-116"><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-116"><em>Player6</em>.<strong>AllowChangeDisplaySize</strong></span></span></td>
<td><span data-ttu-id="66d89-117">L’affichage du lecteur Windows Media 7 ou ultérieur est automatiquement redimensionné pour s’adapter au média.</span><span class="sxs-lookup"><span data-stu-id="66d89-117">The display of Windows Media Player 7 or later automatically resizes to fit the media.</span></span> <span data-ttu-id="66d89-118">Vous pouvez définir les propriétés de hauteur et de largeur dans la <OBJECT> balise ou dans le script.</span><span class="sxs-lookup"><span data-stu-id="66d89-118">You can set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-119"><em>Player6</em>. <strong>AllowScan</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-119"><em>Player6</em>.<strong>AllowScan</strong></span></span></td>
<td><span data-ttu-id="66d89-120"><em>Contrôles</em>.</span><span class="sxs-lookup"><span data-stu-id="66d89-120"><em>Controls</em>.</span></span> <span data-ttu-id="66d89-121"><strong>fastForward</strong> et <em>contrôles</em>. les <strong>fastReverse</strong> sont automatiquement activés pour les types de fichiers qui prennent en charge ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="66d89-121"><strong>fastForward</strong> and <em>Controls</em>.<strong>fastReverse</strong> are automatically enabled for file types that support these methods.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-122"><em>Player6</em>. <strong>AnglesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-122"><em>Player6</em>.<strong>AnglesAvailable</strong></span></span></td>
<td><span data-ttu-id="66d89-123">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-123">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-124"><em>Player6</em>. <strong>AnimationAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-124"><em>Player6</em>.<strong>AnimationAtStart</strong></span></span></td>
<td><span data-ttu-id="66d89-125">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-125">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-126"><em>Player6</em>. <strong>AudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-126"><em>Player6</em>.<strong>AudioStream</strong></span></span></td>
<td><span data-ttu-id="66d89-127">Utilisez des <em>contrôles</em>. <strong>currentAudioLanguageIndex</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-127">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-128"><em>Player6</em>. <strong>AudioStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-128"><em>Player6</em>.<strong>AudioStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="66d89-129">Utilisez des <em>contrôles</em>. <strong>audioLanguageCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-129">Use <em>Controls</em>.<strong>audioLanguageCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-130"><em>Player6</em>. <strong>AutoRewind</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-130"><em>Player6</em>.<strong>AutoRewind</strong></span></span></td>
<td><span data-ttu-id="66d89-131">Utilisez des <em>contrôles</em>. <strong>CurrentPosition</strong> dans le script pour spécifier ou récupérer la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="66d89-131">Use <em>Controls</em>.<strong>currentPosition</strong> in script to specify or retrieve the current position.</span></span> <span data-ttu-id="66d89-132">Vous pouvez également utiliser des marqueurs et le <em>lecteur</em>. événement <strong>markerHit</strong> .</span><span class="sxs-lookup"><span data-stu-id="66d89-132">Alternatively, use markers and the <em>Player</em>.<strong>markerHit</strong> event.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-133"><em>Player6</em>. <strong>Redimensionnement automatique</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-133"><em>Player6</em>.<strong>AutoSize</strong></span></span></td>
<td><span data-ttu-id="66d89-134">Le dimensionnement automatique est le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-134">Automatic sizing is the default behavior.</span></span> <span data-ttu-id="66d89-135">Pour remplacer le dimensionnement automatique, définissez les propriétés de hauteur et de largeur dans la <OBJECT> balise ou dans le script.</span><span class="sxs-lookup"><span data-stu-id="66d89-135">To override automatic sizing, set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-136"><em>Player6</em>. <strong>Démarrage automatique</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-136"><em>Player6</em>.<strong>AutoStart</strong></span></span></td>
<td><span data-ttu-id="66d89-137">Utilisez les <em>paramètres</em>. <strong>démarrage automatique</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-137">Use <em>Settings</em>.<strong>autoStart</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-138"><em>Player6</em>. <strong>Solde</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-138"><em>Player6</em>.<strong>Balance</strong></span></span></td>
<td><span data-ttu-id="66d89-139">Utilisez les <em>paramètres</em>. <strong>équilibrer</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-139">Use <em>Settings</em>.<strong>balance</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-140"><em>Player6</em>. <strong>Bande passante</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-140"><em>Player6</em>.<strong>Bandwidth</strong></span></span></td>
<td><span data-ttu-id="66d89-141">Utilisez <em>réseau</em>. <strong>bande passante</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-141">Use <em>Network</em>.<strong>bandWidth</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-142"><em>Player6</em>. <strong>BaseURL</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-142"><em>Player6</em>.<strong>BaseURL</strong></span></span></td>
<td><span data-ttu-id="66d89-143">Utilisez les <em>paramètres</em>. <strong>baseURL</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-143">Use <em>Settings</em>.<strong>baseURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-144"><em>Player6</em>. <strong>BufferingCount</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-144"><em>Player6</em>.<strong>BufferingCount</strong></span></span></td>
<td><span data-ttu-id="66d89-145">Utilisez <em>réseau.</em> <strong>bufferingCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-145">Use <em>Network.</em><strong>bufferingCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-146"><em>Player6</em>. <strong>BufferingProgress</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-146"><em>Player6</em>.<strong>BufferingProgress</strong></span></span></td>
<td><span data-ttu-id="66d89-147">Utilisez <em>réseau</em>. <strong>bufferingProgress</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-147">Use <em>Network</em>.<strong>bufferingProgress</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-148"><em>Player6</em>. <strong>BufferingTime</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-148"><em>Player6</em>.<strong>BufferingTime</strong></span></span></td>
<td><span data-ttu-id="66d89-149">Utilisez <em>réseau</em>. <strong>bufferingTime</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-149">Use <em>Network</em>.<strong>bufferingTime</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-150"><em>Player6</em>. <strong>ButtonsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-150"><em>Player6</em>.<strong>ButtonsAvailable</strong></span></span></td>
<td><span data-ttu-id="66d89-151">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-151">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-152"><em>Player6</em>. <strong>CanPreview</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-152"><em>Player6</em>.<strong>CanPreview</strong></span></span></td>
<td><span data-ttu-id="66d89-153">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-153">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-154"><em>Player6</em>. <strong>CanScan</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-154"><em>Player6</em>.<strong>CanScan</strong></span></span></td>
<td><span data-ttu-id="66d89-155">Utilisez des <em>contrôles</em>. <strong>isAvailable</strong>( &quot; Fastforward &quot; ) et <em>contrôles</em>.<strong> isAvailable</strong>( &quot; FastReverse &quot; ).</span><span class="sxs-lookup"><span data-stu-id="66d89-155">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastForward&quot;) and <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastReverse&quot;).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-156"><em>Player6</em>. <strong>CanSeek</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-156"><em>Player6</em>.<strong>CanSeek</strong></span></span></td>
<td><span data-ttu-id="66d89-157">Utilisez des <em>contrôles</em>. <strong>isAvailable</strong> pour tester si une méthode de recherche particulière peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="66d89-157">Use <em>Controls</em>.<strong>isAvailable</strong> to test whether a particular seek method can be performed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-158"><em>Player6</em>. <strong>CanSeekToMarkers</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-158"><em>Player6</em>.<strong>CanSeekToMarkers</strong></span></span></td>
<td><span data-ttu-id="66d89-159">Utilisez des <em>contrôles</em>. <strong>isAvailable</strong>( &quot; CurrentMarker &quot; ).</span><span class="sxs-lookup"><span data-stu-id="66d89-159">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;CurrentMarker&quot;).</span></span> <span data-ttu-id="66d89-160">Utilisez un <em>média</em>. <strong>markerCount</strong> pour récupérer le nombre de marqueurs dans un élément multimédia particulier.</span><span class="sxs-lookup"><span data-stu-id="66d89-160">Use <em>Media</em>.<strong>markerCount</strong> to retrieve the count of markers in a particular media item.</span></span> <span data-ttu-id="66d89-161">Utilisez des <em>contrôles</em>. <strong>currentMarker</strong> pour spécifier ou récupérer le numéro de marqueur actuel.</span><span class="sxs-lookup"><span data-stu-id="66d89-161">Use <em>Controls</em>.<strong>currentMarker</strong> to specify or retrieve the current marker number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-162"><em>Player6</em>. <strong>CaptioningID</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-162"><em>Player6</em>.<strong>CaptioningID</strong></span></span></td>
<td><span data-ttu-id="66d89-163">Utilisez <em>ClosedCaption</em>. <strong>captioningID</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-163">Use <em>ClosedCaption</em>.<strong>captioningID</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-164"><em>Player6</em>. <strong>CCActive</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-164"><em>Player6</em>.<strong>CCActive</strong></span></span></td>
<td><span data-ttu-id="66d89-165">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-165">Not available.</span></span> <span data-ttu-id="66d89-166">Pour plus d’informations sur la façon dont les sous-titres ont été modifiés dans le lecteur Windows Media, consultez sous- <a href="closed-captioning.md">titrage</a> .</span><span class="sxs-lookup"><span data-stu-id="66d89-166">See <a href="closed-captioning.md">Closed Captioning</a> for information about how closed captioning has changed in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-167"><em>Player6</em>. <strong>ChannelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-167"><em>Player6</em>.<strong>ChannelDescription</strong></span></span></td>
<td><span data-ttu-id="66d89-168">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-168">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-169"><em>Player6</em>. <strong>ChannelName</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-169"><em>Player6</em>.<strong>ChannelName</strong></span></span></td>
<td><span data-ttu-id="66d89-170">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-170">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-171"><em>Player6</em>. <strong>ChannelURL</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-171"><em>Player6</em>.<strong>ChannelURL</strong></span></span></td>
<td><span data-ttu-id="66d89-172">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-172">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-173"><em>Player6</em>. <strong>ClickToPlay</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-173"><em>Player6</em>.<strong>ClickToPlay</strong></span></span></td>
<td><span data-ttu-id="66d89-174">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-174">Not available.</span></span> <span data-ttu-id="66d89-175">Vous devez fournir des contrôles dans votre interface utilisateur pour démarrer la lecture.</span><span class="sxs-lookup"><span data-stu-id="66d89-175">You should provide controls in your user interface to start playback.</span></span> <span data-ttu-id="66d89-176">L’utilisateur peut également cliquer avec le bouton droit sur l’image vidéo pour ouvrir un menu contextuel qui contient une sélection de <strong>lecture/pause</strong> si le <em>joueur</em>. <strong>enableContextMenu</strong> est égal à true.</span><span class="sxs-lookup"><span data-stu-id="66d89-176">Alternatively, the user can right-click the video image to open a pop-up menu that contains a <strong>Play/Pause</strong> selection if <em>Player</em>.<strong>enableContextMenu</strong> equals true.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-177"><em>Player6</em>. <strong>ClientID</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-177"><em>Player6</em>.<strong>ClientID</strong></span></span></td>
<td><span data-ttu-id="66d89-178">Non disponible. Le lecteur Windows Media série 9 ou version ultérieure permet à l’utilisateur de choisir si un ID de lecteur unique est transmis aux fournisseurs de contenu.</span><span class="sxs-lookup"><span data-stu-id="66d89-178">Not available.Windows Media Player 9 Series or later allows the user to select whether a unique Player ID is transmitted to content providers.</span></span><br/> <span data-ttu-id="66d89-179">Si l’utilisateur sélectionne cette option, le lecteur envoie un ID unique au serveur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="66d89-179">If the user selects this option, the Player sends a unique ID to the Windows Media server.</span></span> <span data-ttu-id="66d89-180">L’ID est enregistré dans le fichier journal du serveur, situé dans le.. <em>system32\logfiles</em> par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-180">The ID is logged in the server's log file, located in the ..<em>system32\logfiles</em> folder by default.</span></span> <span data-ttu-id="66d89-181">Le nom du champ de journal est &quot; c-playerid &quot; .</span><span class="sxs-lookup"><span data-stu-id="66d89-181">The log field name is &quot;c-playerid&quot;.</span></span> <span data-ttu-id="66d89-182">La journalisation du serveur n’est pas activée par défaut dans Windows Media Services.</span><span class="sxs-lookup"><span data-stu-id="66d89-182">Server logging is not enabled by default in Windows Media Services.</span></span><br/> <span data-ttu-id="66d89-183">Si l’utilisateur ne sélectionne pas cette option, le serveur génère un ID de session aléatoire, qui est unique pour chaque client pour une session donnée.</span><span class="sxs-lookup"><span data-stu-id="66d89-183">If the user does not select this option, the server generates a random session ID, which is unique for each client for a given session.</span></span><br/> <span data-ttu-id="66d89-184">Pour plus d’informations, consultez la documentation de Windows Media Services série 9.</span><span class="sxs-lookup"><span data-stu-id="66d89-184">For more information, see the Windows Media Services 9 Series documentation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-185"><em>Player6</em>. <strong>CodecCount</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-185"><em>Player6</em>.<strong>CodecCount</strong></span></span></td>
<td><span data-ttu-id="66d89-186">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-186">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-187"><em>Player6</em>. <strong>ColorKey</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-187"><em>Player6</em>.<strong>ColorKey</strong></span></span></td>
<td><span data-ttu-id="66d89-188">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-188">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-189"><em>Player6</em>. <strong>ConnectionSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-189"><em>Player6</em>.<strong>ConnectionSpeed</strong></span></span></td>
<td><span data-ttu-id="66d89-190">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-190">Not available.</span></span> <span data-ttu-id="66d89-191">Utilisez <em>réseau</em>. <strong>débit</strong> binaire pour déterminer la vitesse de transmission actuelle.</span><span class="sxs-lookup"><span data-stu-id="66d89-191">Use <em>Network</em>.<strong>bitRate</strong> to determine the current bit rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-192"><em>Player6</em>. <strong>ContactAddress</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-192"><em>Player6</em>.<strong>ContactAddress</strong></span></span></td>
<td><span data-ttu-id="66d89-193">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-193">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-194"><em>Player6</em>. <strong>ContactEmail</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-194"><em>Player6</em>.<strong>ContactEmail</strong></span></span></td>
<td><span data-ttu-id="66d89-195">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-195">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-196"><em>Player6</em>. <strong>ContactPhone</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-196"><em>Player6</em>.<strong>ContactPhone</strong></span></span></td>
<td><span data-ttu-id="66d89-197">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-197">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-198"><em>Player6</em>. <strong>CreationDate</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-198"><em>Player6</em>.<strong>CreationDate</strong></span></span></td>
<td><span data-ttu-id="66d89-199">Utilisez <em>MediaCollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) pour récupérer l’index de l’atome de date de création.</span><span class="sxs-lookup"><span data-stu-id="66d89-199">Use <em>MediaCollection</em>.<strong>getMediaAtom</strong>(&quot;CreationDate&quot;) to retrieve the index of the creation date atom.</span></span> <span data-ttu-id="66d89-200">Utilisez un <em>média</em>. <strong>getItemInfoByAtom</strong> pour récupérer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="66d89-200">Use <em>Media</em>.<strong>getItemInfoByAtom</strong> to retrieve the metadata.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-201"><em>Player6</em>. <strong>CurrentAngle</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-201"><em>Player6</em>.<strong>CurrentAngle</strong></span></span></td>
<td><span data-ttu-id="66d89-202">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-202">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-203"><em>Player6</em>. <strong>CurrentAudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-203"><em>Player6</em>.<strong>CurrentAudioStream</strong></span></span></td>
<td><span data-ttu-id="66d89-204">Utilisez des <em>contrôles</em>. <strong>currentAudioLanguageIndex</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-204">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-205"><em>Player6</em>. <strong>CurrentButton</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-205"><em>Player6</em>.<strong>CurrentButton</strong></span></span></td>
<td><span data-ttu-id="66d89-206">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-206">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-207"><em>Player6</em>. <strong>CurrentCCService</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-207"><em>Player6</em>.<strong>CurrentCCService</strong></span></span></td>
<td><span data-ttu-id="66d89-208">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-208">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-209"><em>Player6</em>. <strong>CurrentChapter</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-209"><em>Player6</em>.<strong>CurrentChapter</strong></span></span></td>
<td><span data-ttu-id="66d89-210">Récupère la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="66d89-210">Retrieve the current playlist.</span></span> <span data-ttu-id="66d89-211">Si la sélection actuelle n’est pas la même que la sélection retournée par <em>cdrom</em>. <strong>sélection</strong>, aucun chapitre n’est actuellement présent.</span><span class="sxs-lookup"><span data-stu-id="66d89-211">If the current playlist is not the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then there is no current chapter.</span></span> <span data-ttu-id="66d89-212">Dans le cas contraire, le numéro de chapitre actuel est l’index du média actuel dans la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="66d89-212">Otherwise, the current chapter number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-213"><em>Player6</em>. <strong>CurrentDiscSide</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-213"><em>Player6</em>.<strong>CurrentDiscSide</strong></span></span></td>
<td><span data-ttu-id="66d89-214">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-214">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-215"><em>Player6</em>. <strong>CurrentDomain</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-215"><em>Player6</em>.<strong>CurrentDomain</strong></span></span></td>
<td><span data-ttu-id="66d89-216">Utilisez un <em>DVD</em>. <strong>domaine</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-216">Use <em>DVD</em>.<strong>domain</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-217"><em>Player6</em>. <strong>CurrentMarker</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-217"><em>Player6</em>.<strong>CurrentMarker</strong></span></span></td>
<td><span data-ttu-id="66d89-218">Utilisez des <em>contrôles</em>. <strong>currentMarker</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-218">Use <em>Controls</em>.<strong>currentMarker</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-219"><em>Player6</em>. <strong>CurrentPosition</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-219"><em>Player6</em>.<strong>CurrentPosition</strong></span></span></td>
<td><span data-ttu-id="66d89-220">Utilisez des <em>contrôles</em>. <strong>CurrentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-220">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-221"><em>Player6</em>. <strong>CurrentSubpictureStream</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-221"><em>Player6</em>.<strong>CurrentSubpictureStream</strong></span></span></td>
<td><span data-ttu-id="66d89-222">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-222">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-223"><em>Player6</em>. <strong>CurrentTime</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-223"><em>Player6</em>.<strong>CurrentTime</strong></span></span></td>
<td><span data-ttu-id="66d89-224">Utilisez des <em>contrôles</em>. <strong>currentPositionTimeCode</strong>, <em>contrôles</em>. <strong>currentPositionString</strong>, ou <em>contrôles</em>. <strong>CurrentPosition.</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-224">Use <em>Controls</em>.<strong>currentPositionTimeCode</strong>, <em>Controls</em>.<strong>currentPositionString</strong>, or <em>Controls</em>.<strong>currentPosition.</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-225"><em>Player6</em>. <strong>CurrentTitle</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-225"><em>Player6</em>.<strong>CurrentTitle</strong></span></span></td>
<td><span data-ttu-id="66d89-226">Récupère la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="66d89-226">Retrieve the current playlist.</span></span> <span data-ttu-id="66d89-227">Si la sélection actuelle est la même que celle de la sélection renvoyée par <em>cdrom</em>. <strong>sélection</strong>, le numéro de titre est l’index du média actuel dans la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="66d89-227">If the current playlist is the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then the title number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-228"><em>Player6</em>. <strong>CurrentVolume</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-228"><em>Player6</em>.<strong>CurrentVolume</strong></span></span></td>
<td><span data-ttu-id="66d89-229">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-229">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-230"><em>Player6</em>. <strong>CursorType</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-230"><em>Player6</em>.<strong>CursorType</strong></span></span></td>
<td><span data-ttu-id="66d89-231">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-231">Not available.</span></span> <span data-ttu-id="66d89-232">Utilisez les styles Internet Explorer à la place.</span><span class="sxs-lookup"><span data-stu-id="66d89-232">Use Internet Explorer styles instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-233"><em>Player6</em>. <strong>Defaultframe</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-233"><em>Player6</em>.<strong>DefaultFrame</strong></span></span></td>
<td><span data-ttu-id="66d89-234">Utilisez les <em>paramètres</em>. <strong>defaultFrame</strong>, ou utilisez un</span><span class="sxs-lookup"><span data-stu-id="66d89-234">Use <em>Settings</em>.<strong>defaultFrame</strong>, or use a</span></span> <PARAM> <span data-ttu-id="66d89-235">attribut dans l' <OBJECT> élément : <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span><span class="sxs-lookup"><span data-stu-id="66d89-235">attribute in the <OBJECT> element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-236"><em>Player6</em>. <strong>DisplayBackColor</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-236"><em>Player6</em>.<strong>DisplayBackColor</strong></span></span></td>
<td><span data-ttu-id="66d89-237">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-237">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-238"><em>Player6</em>. <strong>DisplayForeColor</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-238"><em>Player6</em>.<strong>DisplayForeColor</strong></span></span></td>
<td><span data-ttu-id="66d89-239">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-239">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-240"><em>Player6</em>. <strong>DisplayMode</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-240"><em>Player6</em>.<strong>DisplayMode</strong></span></span></td>
<td><span data-ttu-id="66d89-241">La position actuelle peut être extraite en secondes depuis le début en tant que <strong>nombre</strong> à l’aide de <em>contrôles</em>. <strong>CurrentPosition</strong>, sous forme de <strong>chaîne</strong> au format hh : mm : SS (heures, minutes, secondes) à l’aide de <em>contrôles</em>. <strong>currentPositionString</strong>, ou format de code dans le temps à l’aide de <em>contrôles</em>. <strong>currentPositionTimeCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-241">The current position can be retrieved in seconds from the beginning as a <strong>Number</strong> using <em>Controls</em>.<strong>currentPosition</strong>, as a <strong>String</strong> formatted as HH:MM:SS (hours, minutes, seconds) using <em>Controls</em>.<strong>currentPositionString</strong>, or in time code format using <em>Controls</em>.<strong>currentPositionTimeCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-242"><em>Player6</em>. <strong>Diffuser</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-242"><em>Player6</em>.<strong>DisplaySize</strong></span></span></td>
<td><span data-ttu-id="66d89-243">L’affichage par défaut se redimensionne automatiquement pour s’adapter au média.</span><span class="sxs-lookup"><span data-stu-id="66d89-243">The default display automatically resizes to fit the media.</span></span> <span data-ttu-id="66d89-244">Vous pouvez définir les propriétés de hauteur et de largeur dans la <OBJECT> balise ou dans le script.</span><span class="sxs-lookup"><span data-stu-id="66d89-244">You can set the height and width properties in the <OBJECT> tag, or in script.</span></span> <span data-ttu-id="66d89-245">Utilisez le <em>lecteur</em>. <strong>plein</strong> écran pour basculer en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="66d89-245">Use <em>Player</em>.<strong>fullScreen</strong> to switch to full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-246"><em>Player6</em>. <strong>Durée</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-246"><em>Player6</em>.<strong>Duration</strong></span></span></td>
<td><span data-ttu-id="66d89-247">Utilisez un <em>média</em>. <strong>durée</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-247">Use <em>Media</em>.<strong>duration</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-248"><em>Player6</em>. <strong>DVD</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-248"><em>Player6</em>.<strong>DVD</strong></span></span></td>
<td><span data-ttu-id="66d89-249">Utilisez le <em>lecteur</em>. <strong>DVD</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-249">Use <em>Player</em>.<strong>DVD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-250"><em>Player6</em>. <strong>EnableContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-250"><em>Player6</em>.<strong>EnableContextMenu</strong></span></span></td>
<td><span data-ttu-id="66d89-251">Utilisez le <em>lecteur</em>. <strong>enableContextMenu</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-251">Use <em>Player</em>.<strong>enableContextMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-252"><em>Player6</em>. <strong>Activé</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-252"><em>Player6</em>.<strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="66d89-253">Utilisez le <em>lecteur</em>. <strong>activé</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-253">Use <em>Player</em>.<strong>enabled</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-254"><em>Player6</em>. <strong>EnableFullScreenControls</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-254"><em>Player6</em>.<strong>EnableFullScreenControls</strong></span></span></td>
<td><span data-ttu-id="66d89-255">Lorsque vous utilisez le lecteur Windows Media série 9 ou une version ultérieure, les contrôles en plein écran sont automatiquement activés, sauf si vous utilisez <em>le lecteur.</em> <strong></strong>  =  UIMODE &quot; aucune &quot; .</span><span class="sxs-lookup"><span data-stu-id="66d89-255">When using Windows Media Player 9 Series or later, full-screen controls are enabled automatically unless <em>Player</em>.<strong>uiMode</strong> = &quot;none&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-256"><em>Player6</em>. <strong>EnablePositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-256"><em>Player6</em>.<strong>EnablePositionControls</strong></span></span></td>
<td><span data-ttu-id="66d89-257">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-257">Not available.</span></span> <span data-ttu-id="66d89-258">Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-258">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-259"><em>Player6</em>. <strong>EnableTracker</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-259"><em>Player6</em>.<strong>EnableTracker</strong></span></span></td>
<td><span data-ttu-id="66d89-260">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-260">Not available.</span></span> <span data-ttu-id="66d89-261">Vous pouvez fournir un contrôle personnalisé ou utiliser le <em>joueur</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-261">You can provide a custom control or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-262"><em>Player6</em>. <strong>EntryCount</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-262"><em>Player6</em>.<strong>EntryCount</strong></span></span></td>
<td><span data-ttu-id="66d89-263">Utilisez la <em>sélection</em>. <strong>nombre</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-263">Use <em>Playlist</em>.<strong>count</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-264"><em>Player6</em>. <strong>ErrorCode</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-264"><em>Player6</em>.<strong>ErrorCode</strong></span></span></td>
<td><span data-ttu-id="66d89-265">Utilisez <em>ErrorItem</em>. <strong>ErrorCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-265">Use <em>ErrorItem</em>.<strong>errorCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-266"><em>Player6</em>. <strong>ErrorCorrection</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-266"><em>Player6</em>.<strong>ErrorCorrection</strong></span></span></td>
<td><span data-ttu-id="66d89-267">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-267">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-268"><em>Player6</em>. <strong>ErrorDescription</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-268"><em>Player6</em>.<strong>ErrorDescription</strong></span></span></td>
<td><span data-ttu-id="66d89-269">Utilisez <em>ErrorItem</em>. <strong>errorDescription</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-269">Use <em>ErrorItem</em>.<strong>errorDescription</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-270"><em>Player6</em>. <strong>Nom du fichier</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-270"><em>Player6</em>.<strong>FileName</strong></span></span></td>
<td><span data-ttu-id="66d89-271">Utilisez le <em>lecteur</em>. <strong>URL</strong> ou <em>lecteur</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-271">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="66d89-272">Utilisez des <em>contrôles</em>. <strong>CurrentItem</strong> lorsque vous travaillez dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="66d89-272">Use <em>Controls</em>.<strong>currentItem</strong> when working within a playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-273"><em>Player6</em>. <strong>FramesPerSecond</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-273"><em>Player6</em>.<strong>FramesPerSecond</strong></span></span></td>
<td><span data-ttu-id="66d89-274">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-274">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-275"><em>Player6</em>. <strong>HasError</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-275"><em>Player6</em>.<strong>HasError</strong></span></span></td>
<td><span data-ttu-id="66d89-276">Utilisez l' <em>erreur</em>. <strong>errorCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-276">Use <em>Error</em>.<strong>errorCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-277"><em>Player6</em>. <strong>HasMultipleItems</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-277"><em>Player6</em>.<strong>HasMultipleItems</strong></span></span></td>
<td><span data-ttu-id="66d89-278">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-278">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-279"><em>Player6</em>. <strong>ImageSourceHeight</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-279"><em>Player6</em>.<strong>ImageSourceHeight</strong></span></span></td>
<td><span data-ttu-id="66d89-280">Utilisez un <em>média</em>. <strong>imageSourceHeight</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-280">Use <em>Media</em>.<strong>imageSourceHeight</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-281"><em>Player6</em>. <strong>ImageSourceWidth</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-281"><em>Player6</em>.<strong>ImageSourceWidth</strong></span></span></td>
<td><span data-ttu-id="66d89-282">Utilisez un <em>média</em>. <strong>imageSourceWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-282">Use <em>Media</em>.<strong>imageSourceWidth</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-283"><em>Player6</em>. <strong>InvokeURLs</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-283"><em>Player6</em>.<strong>InvokeURLs</strong></span></span></td>
<td><span data-ttu-id="66d89-284">Utilisez les <em>paramètres</em>. <strong>invokeURLs</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-284">Use <em>Settings</em>.<strong>invokeURLs</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-285"><em>Player6</em>. <strong>IsBroadcast</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-285"><em>Player6</em>.<strong>IsBroadcast</strong></span></span></td>
<td><span data-ttu-id="66d89-286">Utilisez <em>réseau</em>. <strong>sourceProtocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-286">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-287"><em>Player6</em>. <strong>IsDurationValid</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-287"><em>Player6</em>.<strong>IsDurationValid</strong></span></span></td>
<td><span data-ttu-id="66d89-288">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-288">Not available.</span></span> <span data-ttu-id="66d89-289"><em>Média</em>. <strong>Duration</strong> contient une valeur valide lorsqu’elle est utilisée avec l’objet Media actuel.</span><span class="sxs-lookup"><span data-stu-id="66d89-289"><em>Media</em>.<strong>duration</strong> contains a valid value when used with the current media object.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-290"><em>Player6</em>. <strong>Langue</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-290"><em>Player6</em>.<strong>Language</strong></span></span></td>
<td><span data-ttu-id="66d89-291">Utilisez des <em>contrôles</em>. <strong>currentAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-291">Use <em>Controls</em>.<strong>currentAudioLanguage</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-292"><em>Player6</em>. <strong>LostPackets</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-292"><em>Player6</em>.<strong>LostPackets</strong></span></span></td>
<td><span data-ttu-id="66d89-293">Utilisez <em>réseau</em>. <strong>lostPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-293">Use <em>Network</em>.<strong>lostPackets</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-294"><em>Player6</em>. <strong>MarkerCount</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-294"><em>Player6</em>.<strong>MarkerCount</strong></span></span></td>
<td><span data-ttu-id="66d89-295">Utilisez un <em>média</em>. <strong>markerCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-295">Use <em>Media</em>.<strong>markerCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-296"><em>Player6</em>. <strong>Muet</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-296"><em>Player6</em>.<strong>Mute</strong></span></span></td>
<td><span data-ttu-id="66d89-297">Utilisez les <em>paramètres</em>. <strong>muet</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-297">Use <em>Settings</em>.<strong>mute</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-298"><em>Player6</em>. <strong>OpenState</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-298"><em>Player6</em>.<strong>OpenState</strong></span></span></td>
<td><span data-ttu-id="66d89-299">Utilisez le <em>lecteur</em>. <strong>openState</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-299">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-300"><em>Player6</em>. <strong>PlayCount</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-300"><em>Player6</em>.<strong>PlayCount</strong></span></span></td>
<td><span data-ttu-id="66d89-301">Utilisez les <em>paramètres</em>. <strong>playCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-301">Use <em>Settings</em>.<strong>playCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-302"><em>Player6</em>. <strong>Lecture</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-302"><em>Player6</em>.<strong>PlayState</strong></span></span></td>
<td><span data-ttu-id="66d89-303">Utilisez le <em>lecteur</em>. <strong>lecture</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-303">Use <em>Player</em>.<strong>playState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-304"><em>Player6</em>. <strong>PreviewMode</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-304"><em>Player6</em>.<strong>PreviewMode</strong></span></span></td>
<td><span data-ttu-id="66d89-305">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-305">Not available.</span></span> <span data-ttu-id="66d89-306">Utilisez une structure de boucle de script avec un minuteur HTML pour dupliquer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="66d89-306">Use a script loop structure with an HTML timer to duplicate this functionality.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-307"><em>Player6</em>. <strong>Taux</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-307"><em>Player6</em>.<strong>Rate</strong></span></span></td>
<td><span data-ttu-id="66d89-308">Utilisez les <em>paramètres</em>. <strong>taux</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-308">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-309"><em>Player6</em>. <strong>ReadyState</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-309"><em>Player6</em>.<strong>ReadyState</strong></span></span></td>
<td><span data-ttu-id="66d89-310">Utilisez le <em>lecteur</em>. <strong>openState</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-310">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-311"><em>Player6</em>. <strong>ReceivedPackets</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-311"><em>Player6</em>.<strong>ReceivedPackets</strong></span></span></td>
<td><span data-ttu-id="66d89-312">Utilisez <em>réseau</em>. <strong>receivedPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-312">Use <em>Network</em>.<strong>receivedPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-313"><em>Player6</em>. <strong>ReceptionQuality</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-313"><em>Player6</em>.<strong>ReceptionQuality</strong></span></span></td>
<td><span data-ttu-id="66d89-314">Utilisez <em>réseau</em>. <strong>receptionQuality</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-314">Use <em>Network</em>.<strong>receptionQuality</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-315"><em>Player6</em>. <strong>RecoveredPackets</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-315"><em>Player6</em>.<strong>RecoveredPackets</strong></span></span></td>
<td><span data-ttu-id="66d89-316">Utilisez <em>réseau</em>. <strong>recoveredPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-316">Use <em>Network</em>.<strong>recoveredPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-317"><em>Player6</em>. <strong>Racine</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-317"><em>Player6</em>.<strong>Root</strong></span></span></td>
<td><span data-ttu-id="66d89-318">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-318">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-319"><em>Player6</em>. <strong>SAMIFileName</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-319"><em>Player6</em>.<strong>SAMIFileName</strong></span></span></td>
<td><span data-ttu-id="66d89-320">Utilisez <em>ClosedCaption</em>. <strong>SAMIFileName</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-320">Use <em>ClosedCaption</em>.<strong>SAMIFileName</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-321"><em>Player6</em>. <strong>SAMILang</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-321"><em>Player6</em>.<strong>SAMILang</strong></span></span></td>
<td><span data-ttu-id="66d89-322">Utilisez <em>ClosedCaption</em>. <strong>SAMILang</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-322">Use <em>ClosedCaption</em>.<strong>SAMILang</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-323"><em>Player6</em>. <strong>SAMIStyle</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-323"><em>Player6</em>.<strong>SAMIStyle</strong></span></span></td>
<td><span data-ttu-id="66d89-324">Utilisez <em>ClosedCaption</em>. <strong>SAMIStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-324">Use <em>ClosedCaption</em>.<strong>SAMIStyle</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-325"><em>Player6</em>. <strong>SelectionEnd</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-325"><em>Player6</em>.<strong>SelectionEnd</strong></span></span></td>
<td><span data-ttu-id="66d89-326">Utilisez un <em>média</em>. <strong>durée</strong> pour déterminer la longueur d’un objet <strong>multimédia</strong> .</span><span class="sxs-lookup"><span data-stu-id="66d89-326">Use <em>Media</em>.<strong>duration</strong> to determine the length of a <strong>Media</strong> object.</span></span> <span data-ttu-id="66d89-327">Utilisez un marqueur avec des <em>contrôles</em>. <strong>currentMarker</strong> pour spécifier une position de fin personnalisée.</span><span class="sxs-lookup"><span data-stu-id="66d89-327">Use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom end position.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-328"><em>Player6</em>. <strong>SelectionStart</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-328"><em>Player6</em>.<strong>SelectionStart</strong></span></span></td>
<td><span data-ttu-id="66d89-329">Utilisez des <em>contrôles</em>. <strong>CurrentPosition</strong> pour commencer la lecture à partir d’une position particulière ou utiliser un marqueur avec des <em>contrôles</em>. <strong>currentMarker</strong> pour spécifier une position de départ personnalisée.</span><span class="sxs-lookup"><span data-stu-id="66d89-329">Use <em>Controls</em>.<strong>currentPosition</strong> to start playback from a particular position or use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom start position.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-330"><em>Player6</em>. <strong>SendErrorEvents</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-330"><em>Player6</em>.<strong>SendErrorEvents</strong></span></span></td>
<td><span data-ttu-id="66d89-331">Les erreurs sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="66d89-331">Errors are queued.</span></span> <span data-ttu-id="66d89-332">Utilisez l’objet <strong>Error</strong> et l’objet <strong>ErrorItem</strong> pour récupérer les informations d’erreur.</span><span class="sxs-lookup"><span data-stu-id="66d89-332">Use the <strong>Error</strong> object and the <strong>ErrorItem</strong> object to retrieve error information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-333"><em>Player6</em>. <strong>SendKeyboardEvents</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-333"><em>Player6</em>.<strong>SendKeyboardEvents</strong></span></span></td>
<td><span data-ttu-id="66d89-334">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-334">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-335"><em>Player6</em>. <strong>SendMouseClickEvents</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-335"><em>Player6</em>.<strong>SendMouseClickEvents</strong></span></span></td>
<td><span data-ttu-id="66d89-336">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-336">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-337"><em>Player6</em>. <strong>SendMouseMoveEvents</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-337"><em>Player6</em>.<strong>SendMouseMoveEvents</strong></span></span></td>
<td><span data-ttu-id="66d89-338">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-338">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-339"><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-339"><em>Player6</em>.<strong>SendOpenStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="66d89-340">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-340">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-341"><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-341"><em>Player6</em>.<strong>SendPlayStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="66d89-342">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-342">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-343"><em>Player6</em>. <strong>SendWarningEvents</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-343"><em>Player6</em>.<strong>SendWarningEvents</strong></span></span></td>
<td><span data-ttu-id="66d89-344">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-344">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-345"><em>Player6</em>. <strong>ShowAudioControls</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-345"><em>Player6</em>.<strong>ShowAudioControls</strong></span></span></td>
<td><span data-ttu-id="66d89-346">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-346">Not available.</span></span> <span data-ttu-id="66d89-347">Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-347">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-348"><em>Player6</em>. <strong>ShowCaptioning</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-348"><em>Player6</em>.<strong>ShowCaptioning</strong></span></span></td>
<td><span data-ttu-id="66d89-349">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-349">Not available.</span></span> <span data-ttu-id="66d89-350">Vous pouvez fournir un affichage de sous-titres personnalisé.</span><span class="sxs-lookup"><span data-stu-id="66d89-350">You can provide a custom closed caption display.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-351"><em>Player6</em>. <strong>ShowControls</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-351"><em>Player6</em>.<strong>ShowControls</strong></span></span></td>
<td><span data-ttu-id="66d89-352">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-352">Not available.</span></span> <span data-ttu-id="66d89-353">Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-353">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-354"><em>Player6</em>. <strong>ShowDisplay</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-354"><em>Player6</em>.<strong>ShowDisplay</strong></span></span></td>
<td><span data-ttu-id="66d89-355">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-355">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-356"><em>Player6</em>. <strong>ShowGotoBar</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-356"><em>Player6</em>.<strong>ShowGotoBar</strong></span></span></td>
<td><span data-ttu-id="66d89-357">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-357">Not available.</span></span> <span data-ttu-id="66d89-358">Vous pouvez fournir des fonctionnalités personnalisées à l’aide de l’objet Media</span><span class="sxs-lookup"><span data-stu-id="66d89-358">You can provide custom functionality using the Media object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-359"><em>Player6</em>. <strong>ShowPositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-359"><em>Player6</em>.<strong>ShowPositionControls</strong></span></span></td>
<td><span data-ttu-id="66d89-360">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-360">Not available.</span></span> <span data-ttu-id="66d89-361">Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-361">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-362"><em>Player6</em>. <strong>ShowStatusBar</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-362"><em>Player6</em>.<strong>ShowStatusBar</strong></span></span></td>
<td><span data-ttu-id="66d89-363">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-363">Not available.</span></span> <span data-ttu-id="66d89-364">Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-364">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-365"><em>Player6</em>. <strong>ShowTracker</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-365"><em>Player6</em>.<strong>ShowTracker</strong></span></span></td>
<td><span data-ttu-id="66d89-366">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-366">Not available.</span></span> <span data-ttu-id="66d89-367">Vous pouvez fournir des contrôles personnalisés ou utiliser <em>Player</em>. <strong>UIMODE</strong> pour choisir une configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="66d89-367">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-368"><em>Player6</em>. <strong>SourceLink</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-368"><em>Player6</em>.<strong>SourceLink</strong></span></span></td>
<td><span data-ttu-id="66d89-369">Utilisez un <em>média</em>. <strong>sourceURL</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-369">Use <em>Media</em>.<strong>sourceURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-370"><em>Player6</em>. <strong>SourceProtocol</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-370"><em>Player6</em>.<strong>SourceProtocol</strong></span></span></td>
<td><span data-ttu-id="66d89-371">Utilisez <em>réseau</em>. <strong>sourceProtocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-371">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-372"><em>Player6</em>. <strong>StreamCount</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-372"><em>Player6</em>.<strong>StreamCount</strong></span></span></td>
<td><span data-ttu-id="66d89-373">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-373">Not available.</span></span> <span data-ttu-id="66d89-374">Utilisez des <em>contrôles</em>. <strong>audioLanguageCount</strong> pour récupérer le nombre de flux de langage audio.</span><span class="sxs-lookup"><span data-stu-id="66d89-374">Use <em>Controls</em>.<strong>audioLanguageCount</strong> to retrieve the number of audio language streams.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-375"><em>Player6</em>. <strong>SubpictureOn</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-375"><em>Player6</em>.<strong>SubpictureOn</strong></span></span></td>
<td><span data-ttu-id="66d89-376">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-376">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-377"><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-377"><em>Player6</em>.<strong>SubpictureStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="66d89-378">Non disponible</span><span class="sxs-lookup"><span data-stu-id="66d89-378">Not available</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-379"><em>Player6</em>. <strong>TitlesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-379"><em>Player6</em>.<strong>TitlesAvailable</strong></span></span></td>
<td><span data-ttu-id="66d89-380">Utilisez ce qui suit :<code>Player.Cdrom.playlist.count - 1</code></span><span class="sxs-lookup"><span data-stu-id="66d89-380">Use the following:<code>Player.Cdrom.playlist.count - 1</code></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-381"><em>Player6</em>. <strong>TotalTitleTime</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-381"><em>Player6</em>.<strong>TotalTitleTime</strong></span></span></td>
<td><span data-ttu-id="66d89-382">Utilisez <em>currentMedia</em>. <strong>Duration</strong> ou <em>currentMedia</em>. <strong>durationString</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-382">Use <em>currentMedia</em>.<strong>duration</strong> or <em>currentMedia</em>.<strong>durationString</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-383"><em>Player6</em>. <strong>TransparentAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-383"><em>Player6</em>.<strong>TransparentAtStart</strong></span></span></td>
<td><span data-ttu-id="66d89-384">Utilisez un script pour spécifier les valeurs de hauteur et de largeur pour rendre le lecteur visible ou invisible.</span><span class="sxs-lookup"><span data-stu-id="66d89-384">Use script to specify the height and width values to make the player visible or invisible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-385"><em>Player6</em>. <strong>UniqueID</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-385"><em>Player6</em>.<strong>UniqueID</strong></span></span></td>
<td><span data-ttu-id="66d89-386">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-386">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-387"><em>Player6</em>. <strong>VideoBorder3D</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-387"><em>Player6</em>.<strong>VideoBorder3D</strong></span></span></td>
<td><span data-ttu-id="66d89-388">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-388">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-389"><em>Player6</em>. <strong>VideoBorderColor</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-389"><em>Player6</em>.<strong>VideoBorderColor</strong></span></span></td>
<td><span data-ttu-id="66d89-390">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-390">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-391"><em>Player6</em>. <strong>VideoBorderWidth</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-391"><em>Player6</em>.<strong>VideoBorderWidth</strong></span></span></td>
<td><span data-ttu-id="66d89-392">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-392">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-393"><em>Player6</em>. <strong>Volume</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-393"><em>Player6</em>.<strong>Volume</strong></span></span></td>
<td><span data-ttu-id="66d89-394">Utilisez les <em>paramètres</em>. <strong>Volume</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-394">Use <em>Settings</em>.<strong>Volume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-395"><em>Player6</em>. <strong>VolumesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-395"><em>Player6</em>.<strong>VolumesAvailable</strong></span></span></td>
<td><span data-ttu-id="66d89-396">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-396">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="66d89-397">Le tableau suivant compare les méthodes du modèle d’objet Windows Media Player version 6,4 avec le modèle objet Windows Media Player 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="66d89-397">The following table compares the Windows Media Player version 6.4 object model methods with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66d89-398">Lecteur Windows Media 6,4, méthode</span><span class="sxs-lookup"><span data-stu-id="66d89-398">Windows Media Player 6.4 method</span></span></th>
<th><span data-ttu-id="66d89-399">Windows Media Player 7 ou une version ultérieure équivalente</span><span class="sxs-lookup"><span data-stu-id="66d89-399">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66d89-400"><em>Player6</em>. <strong>AboutBox</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-400"><em>Player6</em>.<strong>AboutBox</strong></span></span></td>
<td><span data-ttu-id="66d89-401">Utilisez le <em>lecteur</em>. <strong>VERSIONINFO</strong> pour récupérer la version du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="66d89-401">Use <em>Player</em>.<strong>versionInfo</strong> to retrieve the version of Windows Media Player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-402"><em>Player6</em>. <strong>BackwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-402"><em>Player6</em>.<strong>BackwardScan</strong></span></span></td>
<td><span data-ttu-id="66d89-403">Utilisez les <em>paramètres</em>. <strong>taux</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-403">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-404"><em>Player6</em>. <strong>ButtonActivate</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-404"><em>Player6</em>.<strong>ButtonActivate</strong></span></span></td>
<td><span data-ttu-id="66d89-405">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-405">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-406"><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-406"><em>Player6</em>.<strong>ButtonSelectAndActivate</strong></span></span></td>
<td><span data-ttu-id="66d89-407">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-407">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-408"><em>Player6</em>. <strong>Annuler</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-408"><em>Player6</em>.<strong>Cancel</strong></span></span></td>
<td><span data-ttu-id="66d89-409">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-409">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-410"><em>Player6</em>. <strong>ChapterPlay</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-410"><em>Player6</em>.<strong>ChapterPlay</strong></span></span></td>
<td><span data-ttu-id="66d89-411">Si vous jouez déjà à la sélection de titre spécifiée, récupérez le chapitre souhaité en tant qu’objet multimédia à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="66d89-411">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="66d89-412">Ensuite, spécifiez <em>Player</em>. <strong>currentMedia</strong> à l’aide de l’objet multimédia retourné.</span><span class="sxs-lookup"><span data-stu-id="66d89-412">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-413"><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-413"><em>Player6</em>.<strong>ChapterPlayAutoStop</strong></span></span></td>
<td><span data-ttu-id="66d89-414">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-414">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-415"><em>Player6</em>. <strong>ChapterSearch</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-415"><em>Player6</em>.<strong>ChapterSearch</strong></span></span></td>
<td><span data-ttu-id="66d89-416">Si vous jouez déjà à la sélection de titre spécifiée, récupérez le chapitre souhaité en tant qu’objet multimédia à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="66d89-416">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="66d89-417">Ensuite, spécifiez <em>Player</em>. <strong>currentMedia</strong> à l’aide de l’objet multimédia retourné.</span><span class="sxs-lookup"><span data-stu-id="66d89-417">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-418"><em>Player6</em>. <strong>Fastforward</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-418"><em>Player6</em>.<strong>FastForward</strong></span></span></td>
<td><span data-ttu-id="66d89-419">Utilisez des <em>contrôles</em>. <strong>fastForward</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-419">Use <em>Controls</em>.<strong>fastForward</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-420"><em>Player6</em>. <strong>FastReverse</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-420"><em>Player6</em>.<strong>FastReverse</strong></span></span></td>
<td><span data-ttu-id="66d89-421">Utilisez des <em>contrôles</em>. <strong>fastReverse</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-421">Use <em>Controls</em>.<strong>fastReverse</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-422"><em>Player6</em>. <strong>ForwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-422"><em>Player6</em>.<strong>ForwardScan</strong></span></span></td>
<td><span data-ttu-id="66d89-423">Utilisez les <em>paramètres</em>. <strong>taux</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-423">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-424"><em>Player6</em>. <strong>GetAllGPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-424"><em>Player6</em>.<strong>GetAllGPRMs</strong></span></span></td>
<td><span data-ttu-id="66d89-425">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-425">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-426"><em>Player6</em>. <strong>GetAllSPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-426"><em>Player6</em>.<strong>GetAllSPRMs</strong></span></span></td>
<td><span data-ttu-id="66d89-427">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-427">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-428"><em>Player6</em>. <strong>GetAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-428"><em>Player6</em>.<strong>GetAudioLanguage</strong></span></span></td>
<td><span data-ttu-id="66d89-429">Utilisez des <em>contrôles</em>. <strong>currentAudioLanguage</strong> pour récupérer le LCID de la langue audio actuelle.</span><span class="sxs-lookup"><span data-stu-id="66d89-429">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to retrieve the LCID of the current audio language.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-430"><em>Player6</em>. <strong>GetCodecDescription</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-430"><em>Player6</em>.<strong>GetCodecDescription</strong></span></span></td>
<td><span data-ttu-id="66d89-431">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-431">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-432"><em>Player6</em>. <strong>GetCodecInstalled</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-432"><em>Player6</em>.<strong>GetCodecInstalled</strong></span></span></td>
<td><span data-ttu-id="66d89-433">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-433">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-434"><em>Player6</em>. <strong>GetCodecURL</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-434"><em>Player6</em>.<strong>GetCodecURL</strong></span></span></td>
<td><span data-ttu-id="66d89-435">Utilisez <em>ErrorItem</em>. <strong>customUrl</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-435">Use <em>ErrorItem</em>.<strong>customUrl</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-436"><em>Player6</em>. <strong>GetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-436"><em>Player6</em>.<strong>GetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="66d89-437">Utilisez le script pour effectuer une boucle dans la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="66d89-437">Use script to loop through the current playlist.</span></span> <span data-ttu-id="66d89-438">Utilisez un <em>média</em>. <strong>isIdentical</strong> pour comparer chaque entrée de la sélection au <em>lecteur</em>. objet <strong>currentMedia</strong> .</span><span class="sxs-lookup"><span data-stu-id="66d89-438">Use <em>Media</em>.<strong>isIdentical</strong> to compare each entry in the playlist to the <em>Player</em>.<strong>currentMedia</strong> object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-439"><em>Player6</em>. <strong>GetMarkerName</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-439"><em>Player6</em>.<strong>GetMarkerName</strong></span></span></td>
<td><span data-ttu-id="66d89-440">Utilisez un <em>média</em>. <strong>getMarkerName</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-440">Use <em>Media</em>.<strong>getMarkerName</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-441"><em>Player6</em>. <strong>GetMarkerTime</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-441"><em>Player6</em>.<strong>GetMarkerTime</strong></span></span></td>
<td><span data-ttu-id="66d89-442">Utilisez un <em>média</em>. <strong>getMarkerTime</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-442">Use <em>Media</em>.<strong>getMarkerTime</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-443"><em>Player6</em>. <strong>GetMediaInfoString</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-443"><em>Player6</em>.<strong>GetMediaInfoString</strong></span></span></td>
<td><span data-ttu-id="66d89-444">Utilisez un <em>média</em>. <strong>getItemInfo</strong>, <em>média</em>. <strong>getItemInfoByAtom</strong>et leurs méthodes associées pour récupérer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="66d89-444">Use <em>Media</em>.<strong>getItemInfo</strong>, <em>Media</em>.<strong>getItemInfoByAtom</strong>, and their associated methods to retrieve metadata.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-445"><em>Player6</em>. <strong>GetMediaParameter</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-445"><em>Player6</em>.<strong>GetMediaParameter</strong></span></span></td>
<td><span data-ttu-id="66d89-446">Utilisez la <em>sélection</em>. <strong>élément</strong> permettant de récupérer un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="66d89-446">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="66d89-447">Utilisez ensuite le <em>média</em>. <strong>getItemInfo</strong> pour récupérer la chaîne de paramètre.</span><span class="sxs-lookup"><span data-stu-id="66d89-447">Then use <em>Media</em>.<strong>getItemInfo</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-448"><em>Player6</em>. <strong>GetMediaParameterName</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-448"><em>Player6</em>.<strong>GetMediaParameterName</strong></span></span></td>
<td><span data-ttu-id="66d89-449">Utilisez la <em>sélection</em>. <strong>élément</strong> permettant de récupérer un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="66d89-449">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="66d89-450">Utilisez ensuite le <em>média</em>. <strong>getAttributeName</strong> pour récupérer la chaîne de paramètre.</span><span class="sxs-lookup"><span data-stu-id="66d89-450">Then use <em>Media</em>.<strong>getAttributeName</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-451"><em>Player6</em>. <strong>GetMoreInfoURL</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-451"><em>Player6</em>.<strong>GetMoreInfoURL</strong></span></span></td>
<td><span data-ttu-id="66d89-452">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-452">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-453"><em>Player6</em>. <strong>GetNumberOfChapters</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-453"><em>Player6</em>.<strong>GetNumberOfChapters</strong></span></span></td>
<td><span data-ttu-id="66d89-454">Si un titre est en cours de diffusion, utilisez <em>currentPlaylist</em>. <strong>nombre</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-454">If a title is currently playing, use <em>currentPlaylist</em>.<strong>count</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-455"><em>Player6</em>. <strong>GetStreamGroup</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-455"><em>Player6</em>.<strong>GetStreamGroup</strong></span></span></td>
<td><span data-ttu-id="66d89-456">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-456">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-457"><em>Player6</em>. <strong>GetStreamName</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-457"><em>Player6</em>.<strong>GetStreamName</strong></span></span></td>
<td><span data-ttu-id="66d89-458">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-458">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-459"><em>Player6</em>. <strong>GetStreamSelected</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-459"><em>Player6</em>.<strong>GetStreamSelected</strong></span></span></td>
<td><span data-ttu-id="66d89-460">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-460">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-461"><em>Player6</em>. <strong>GetSubpictureLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-461"><em>Player6</em>.<strong>GetSubpictureLanguage</strong></span></span></td>
<td><span data-ttu-id="66d89-462">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-462">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-463"><em>Player6</em>. <strong>Goup</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-463"><em>Player6</em>.<strong>GoUp</strong></span></span></td>
<td><span data-ttu-id="66d89-464">Utilisez un <em>DVD</em>. <strong>retour</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-464">Use <em>DVD</em>.<strong>back</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-465"><em>Player6</em>. <strong>IsSoundCardEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-465"><em>Player6</em>.<strong>IsSoundCardEnabled</strong></span></span></td>
<td><span data-ttu-id="66d89-466">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-466">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-467"><em>Player6</em>. <strong>LeftButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-467"><em>Player6</em>.<strong>LeftButtonSelect</strong></span></span></td>
<td><span data-ttu-id="66d89-468">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-468">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-469"><em>Player6</em>. <strong>LowerButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-469"><em>Player6</em>.<strong>LowerButtonSelect</strong></span></span></td>
<td><span data-ttu-id="66d89-470">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-470">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-471"><em>Player6</em>. <strong>MenuCall</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-471"><em>Player6</em>.<strong>MenuCall</strong></span></span></td>
<td><span data-ttu-id="66d89-472">Utilisez un <em>DVD</em>. <strong>titleMenu</strong> ou <em>DVD</em>. <strong>menu</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-472">Use <em>DVD</em>.<strong>titleMenu</strong> or <em>DVD</em>.<strong>topMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-473"><em>Player6</em>. <strong>Suivant</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-473"><em>Player6</em>.<strong>Next</strong></span></span></td>
<td><span data-ttu-id="66d89-474">Utilisez des <em>contrôles</em>. <strong>suivant</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-474">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-475"><em>Player6</em>. <strong>NextPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-475"><em>Player6</em>.<strong>NextPGSearch</strong></span></span></td>
<td><span data-ttu-id="66d89-476">Utilisez des <em>contrôles</em>. <strong>suivant</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-476">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-477"><em>Player6</em>. <strong>Ouvrir</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-477"><em>Player6</em>.<strong>Open</strong></span></span></td>
<td><span data-ttu-id="66d89-478">Utilisez le <em>lecteur</em>. <strong>URL</strong> ou <em>lecteur</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-478">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="66d89-479">Les fichiers sont toujours ouverts de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="66d89-479">Files always open asynchronously.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-480"><em>Player6</em>. <strong>Suspendre</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-480"><em>Player6</em>.<strong>Pause</strong></span></span></td>
<td><span data-ttu-id="66d89-481">Utilisez des <em>contrôles</em>. <strong>suspendre</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-481">Use <em>Controls</em>.<strong>pause</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-482"><em>Player6</em>. <strong>Lire</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-482"><em>Player6</em>.<strong>Play</strong></span></span></td>
<td><span data-ttu-id="66d89-483">Utilisez des <em>contrôles</em>. <strong>jouez</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-483">Use <em>Controls</em>.<strong>play</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-484"><em>Player6</em>. <strong>Précédent</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-484"><em>Player6</em>.<strong>Previous</strong></span></span></td>
<td><span data-ttu-id="66d89-485">Utilisez des <em>contrôles</em>. <strong>précédent</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-485">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-486"><em>Player6</em>. <strong>PrevPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-486"><em>Player6</em>.<strong>PrevPGSearch</strong></span></span></td>
<td><span data-ttu-id="66d89-487">Utilisez des <em>contrôles</em>. <strong>précédent</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-487">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-488"><em>Player6</em>. <strong>ResumeFromMenu</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-488"><em>Player6</em>.<strong>ResumeFromMenu</strong></span></span></td>
<td><span data-ttu-id="66d89-489">Utilisez un <em>DVD</em>. <strong>reprendre</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-489">Use <em>DVD</em>.<strong>resume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-490"><em>Player6</em>. <strong>RightButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-490"><em>Player6</em>.<strong>RightButtonSelect</strong></span></span></td>
<td><span data-ttu-id="66d89-491">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-491">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-492"><em>Player6</em>. <strong>SetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-492"><em>Player6</em>.<strong>SetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="66d89-493">Récupérez un objet multimédia à l’aide de <em>currentPlaylist</em>. <strong>Item</strong>(<em>entryNumber</em>).</span><span class="sxs-lookup"><span data-stu-id="66d89-493">Retrieve a media object using <em>currentPlaylist</em>.<strong>item</strong>(<em>entryNumber</em>).</span></span> <span data-ttu-id="66d89-494">Ensuite, spécifiez l’objet multimédia récupéré à l’aide de <em>contrôles</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-494">Then, specify the retrieved media object using <em>Controls</em>.<strong>currentItem</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-495"><em>Player6</em>. <strong>ShowDialog</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-495"><em>Player6</em>.<strong>ShowDialog</strong></span></span></td>
<td><span data-ttu-id="66d89-496">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-496">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-497"><em>Player6</em>. <strong>StillOff</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-497"><em>Player6</em>.<strong>StillOff</strong></span></span></td>
<td><span data-ttu-id="66d89-498">Utilisez des <em>contrôles</em>. <strong>jouez</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-498">Use <em>Controls</em>.<strong>play</strong>.</span></span> <span data-ttu-id="66d89-499">Vous pouvez également utiliser des <em>contrôles</em>. <strong>Next</strong> si actuellement en mode toujours.</span><span class="sxs-lookup"><span data-stu-id="66d89-499">Alternatively, use <em>Controls</em>.<strong>Next</strong> if currently in still mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-500"><em>Player6</em>. <strong>Arrêter</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-500"><em>Player6</em>.<strong>Stop</strong></span></span></td>
<td><span data-ttu-id="66d89-501">Utilisez des <em>contrôles</em>. <strong>Arrêtez</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-501">Use <em>Controls</em>.<strong>stop</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-502"><em>Player6</em>. <strong>StreamSelect</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-502"><em>Player6</em>.<strong>StreamSelect</strong></span></span></td>
<td><span data-ttu-id="66d89-503">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-503">Not available.</span></span> <span data-ttu-id="66d89-504">Utilisez des <em>contrôles</em>. <strong>currentAudioLanguage</strong> pour spécifier un flux de langue audio.</span><span class="sxs-lookup"><span data-stu-id="66d89-504">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to specify an audio language stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-505"><em>Player6</em>. <strong>TimePlay</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-505"><em>Player6</em>.<strong>TimePlay</strong></span></span></td>
<td><span data-ttu-id="66d89-506">À partir de la sélection racine, utilisez <em>currentPlaylist</em>. <strong>Item</strong>(<em>index</em>) pour récupérer un objet multimédia.</span><span class="sxs-lookup"><span data-stu-id="66d89-506">From the root playlist, use <em>currentPlaylist</em>.<strong>item</strong>(<em>index</em>) to retrieve a media object.</span></span> <span data-ttu-id="66d89-507">Ensuite, définissez l’objet multimédia en tant que l’objet en cours à l’aide de <em>contrôles</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-507">Then, set the media object as the current one using <em>Controls</em>.<strong>currentItem</strong>.</span></span> <span data-ttu-id="66d89-508">Ensuite, spécifiez les <em>contrôles</em>. <strong>CurrentPosition</strong> à l’aide d’une valeur de temps en secondes.</span><span class="sxs-lookup"><span data-stu-id="66d89-508">Then, specify <em>Controls</em>.<strong>currentPosition</strong> using a time value in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-509"><em>Player6</em>. <strong>TimeSearch</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-509"><em>Player6</em>.<strong>TimeSearch</strong></span></span></td>
<td><span data-ttu-id="66d89-510">Utilisez des <em>contrôles</em>. <strong>CurrentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-510">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-511"><em>Player6</em>. <strong>TitlePlay</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-511"><em>Player6</em>.<strong>TitlePlay</strong></span></span></td>
<td><span data-ttu-id="66d89-512">Si vous jouez déjà à la sélection de titre spécifiée, récupérez le chapitre souhaité en tant qu’objet multimédia à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="66d89-512">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="66d89-513">Ensuite, spécifiez <em>Player</em>. <strong>currentMedia</strong> à l’aide de l’objet multimédia retourné.</span><span class="sxs-lookup"><span data-stu-id="66d89-513">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/> <span data-ttu-id="66d89-514">Vous pouvez également utiliser <em>currentPlaylist</em>. <strong>élément</strong> pour récupérer un objet multimédia, puis utilisez l’objet multimédia retourné pour spécifier des <em>contrôles</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="66d89-514">Alternatively, use <em>currentPlaylist</em>.<strong>item</strong> to retrieve a media object, and then use the media object returned to specify <em>Controls</em>.<strong>currentItem</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-515"><em>Player6</em>. <strong>TopPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-515"><em>Player6</em>.<strong>TopPGSearch</strong></span></span></td>
<td><span data-ttu-id="66d89-516">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-516">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66d89-517"><em>Player6</em>. <strong>UOPValid</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-517"><em>Player6</em>.<strong>UOPValid</strong></span></span></td>
<td><span data-ttu-id="66d89-518">Non disponible</span><span class="sxs-lookup"><span data-stu-id="66d89-518">Not available</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66d89-519"><em>Player6</em>. <strong>UpperButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="66d89-519"><em>Player6</em>.<strong>UpperButtonSelect</strong></span></span></td>
<td><span data-ttu-id="66d89-520">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-520">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="66d89-521">Le tableau suivant compare les événements du modèle d’objet Windows Media Player version 6,4 avec le modèle objet Windows Media Player 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="66d89-521">The following table compares the Windows Media Player version 6.4 object model events with the Windows Media Player 7 or later object model.</span></span>



| <span data-ttu-id="66d89-522">Événement du lecteur Windows Media 6,4</span><span class="sxs-lookup"><span data-stu-id="66d89-522">Windows Media Player 6.4 event</span></span>  | <span data-ttu-id="66d89-523">Windows Media Player 7 ou une version ultérieure équivalente</span><span class="sxs-lookup"><span data-stu-id="66d89-523">Windows Media Player 7 or later equivalent</span></span>                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d89-524">*Player6*. **Mise en mémoire tampon**</span><span class="sxs-lookup"><span data-stu-id="66d89-524">*Player6*.**Buffering**</span></span>         | <span data-ttu-id="66d89-525">Utilisez le *lecteur*. **Mise en mémoire tampon**.</span><span class="sxs-lookup"><span data-stu-id="66d89-525">Use *Player*.**Buffering**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="66d89-526">*Player6*. **Cliquez sur**</span><span class="sxs-lookup"><span data-stu-id="66d89-526">*Player6*.**Click**</span></span>             | <span data-ttu-id="66d89-527">Utilisez le *lecteur*. **Cliquez sur**</span><span class="sxs-lookup"><span data-stu-id="66d89-527">Use *Player*.**Click**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="66d89-528">*Player6*. **DblClick**</span><span class="sxs-lookup"><span data-stu-id="66d89-528">*Player6*.**DblClick**</span></span>          | <span data-ttu-id="66d89-529">Utilisez le *lecteur*. **DoubleClick**</span><span class="sxs-lookup"><span data-stu-id="66d89-529">Use *Player*.**DoubleClick**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="66d89-530">*Player6*. Se **déconnecter**</span><span class="sxs-lookup"><span data-stu-id="66d89-530">*Player6*.**Disconnect**</span></span>        | <span data-ttu-id="66d89-531">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-531">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="66d89-532">*Player6*. **DisplayModeChange**</span><span class="sxs-lookup"><span data-stu-id="66d89-532">*Player6*.**DisplayModeChange**</span></span> | <span data-ttu-id="66d89-533">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-533">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="66d89-534">*Player6*. **DVDNotify**</span><span class="sxs-lookup"><span data-stu-id="66d89-534">*Player6*.**DVDNotify**</span></span>         | <span data-ttu-id="66d89-535">*Lecteur*. **DomainChange** et *Player*. Les **OpenPlaylistSwitch** sont des événements spécifiques aux DVD.</span><span class="sxs-lookup"><span data-stu-id="66d89-535">*Player*.**DomainChange** and *Player*.**OpenPlaylistSwitch** are DVD-specific events.</span></span> <span data-ttu-id="66d89-536">D’autres événements liés aux sélections, aux médias et aux supports de CD-ROM peuvent s’appliquer également en fonction de l’application.</span><span class="sxs-lookup"><span data-stu-id="66d89-536">Other events related to playlists, media, and CD-ROM media may apply as well depending on the application.</span></span>                        |
| <span data-ttu-id="66d89-537">*Player6*. **EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="66d89-537">*Player6*.**EndOfStream**</span></span>       | <span data-ttu-id="66d89-538">Utilisez le *lecteur*. **Lecture**.</span><span class="sxs-lookup"><span data-stu-id="66d89-538">Use *Player*.**PlayState**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="66d89-539">*Player6*. **Erreur**</span><span class="sxs-lookup"><span data-stu-id="66d89-539">*Player6*.**Error**</span></span>             | <span data-ttu-id="66d89-540">L’événement est inchangé.</span><span class="sxs-lookup"><span data-stu-id="66d89-540">The event is unchanged.</span></span> <span data-ttu-id="66d89-541">Toutefois, les erreurs sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="66d89-541">Errors, however, are queued.</span></span> <span data-ttu-id="66d89-542">Utilisez l’objet **Error** avec l’objet **ErrorItem** pour récupérer les informations d’erreur à partir de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="66d89-542">Use the **Error** object with the **ErrorItem** object to retrieve error information from the queue.</span></span> <span data-ttu-id="66d89-543">Consultez l’exemple de code dans la section précédente, gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="66d89-543">See the example code in the preceding section, Error handling.</span></span> |
| <span data-ttu-id="66d89-544">*Player6*. **Touche PG. suiv**</span><span class="sxs-lookup"><span data-stu-id="66d89-544">*Player6*.**KeyDown**</span></span>           | <span data-ttu-id="66d89-545">Utilisez le *lecteur*. **Touche PG. suiv**</span><span class="sxs-lookup"><span data-stu-id="66d89-545">Use *Player*.**Keydown**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="66d89-546">*Player6*. **Appuyez sur la touche**</span><span class="sxs-lookup"><span data-stu-id="66d89-546">*Player6*.**KeyPress**</span></span>          | <span data-ttu-id="66d89-547">Utilisez le *lecteur*. **Appuyez sur la touche**</span><span class="sxs-lookup"><span data-stu-id="66d89-547">Use *Player*.**KeyPress**</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="66d89-548">*Player6*. **KeyUp**</span><span class="sxs-lookup"><span data-stu-id="66d89-548">*Player6*.**KeyUp**</span></span>             | <span data-ttu-id="66d89-549">Utilisez le *lecteur*. **KeyUp**</span><span class="sxs-lookup"><span data-stu-id="66d89-549">Use *Player*.**KeyUp**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="66d89-550">*Player6*. **MarkerHit**</span><span class="sxs-lookup"><span data-stu-id="66d89-550">*Player6*.**MarkerHit**</span></span>         | <span data-ttu-id="66d89-551">Utilisez le *lecteur*. **MarkerHit**.</span><span class="sxs-lookup"><span data-stu-id="66d89-551">Use *Player*.**MarkerHit**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="66d89-552">*Player6*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="66d89-552">*Player6*.**MouseDown**</span></span>         | <span data-ttu-id="66d89-553">Utilisez le *lecteur*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="66d89-553">Use *Player*.**MouseDown**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="66d89-554">*Player6*. **MouseMove**</span><span class="sxs-lookup"><span data-stu-id="66d89-554">*Player6*.**MouseMove**</span></span>         | <span data-ttu-id="66d89-555">Utilisez le *lecteur*. **MouseMove**</span><span class="sxs-lookup"><span data-stu-id="66d89-555">Use *Player*.**MouseMove**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="66d89-556">*Player6*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="66d89-556">*Player6*.**MouseUp**</span></span>           | <span data-ttu-id="66d89-557">Utilisez le *lecteur*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="66d89-557">Use *Player*.**MouseUp**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="66d89-558">*Player6*. **NewStream**</span><span class="sxs-lookup"><span data-stu-id="66d89-558">*Player6*.**NewStream**</span></span>         | <span data-ttu-id="66d89-559">Utilisez le *lecteur*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="66d89-559">Use *Player*.**OpenStateChange**</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="66d89-560">*Player6*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="66d89-560">*Player6*.**OpenStateChange**</span></span>   | <span data-ttu-id="66d89-561">Utilisez le *lecteur*. **OpenStateChange**.</span><span class="sxs-lookup"><span data-stu-id="66d89-561">Use *Player*.**OpenStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="66d89-562">*Player6*. **PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="66d89-562">*Player6*.**PlayStateChange**</span></span>   | <span data-ttu-id="66d89-563">Utilisez le *lecteur*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="66d89-563">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="66d89-564">*Player6*. **PositionChange**</span><span class="sxs-lookup"><span data-stu-id="66d89-564">*Player6*.**PositionChange**</span></span>    | <span data-ttu-id="66d89-565">Utilisez le *lecteur*. **PositionChange**.</span><span class="sxs-lookup"><span data-stu-id="66d89-565">Use *Player*.**PositionChange**.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="66d89-566">*Player6*. **ReadyStateChange**</span><span class="sxs-lookup"><span data-stu-id="66d89-566">*Player6*.**ReadyStateChange**</span></span>  | <span data-ttu-id="66d89-567">Utilisez le *lecteur*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="66d89-567">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="66d89-568">*Player6*. **Commande**</span><span class="sxs-lookup"><span data-stu-id="66d89-568">*Player6*.**ScriptCommand**</span></span>     | <span data-ttu-id="66d89-569">Utilisez le *lecteur*. **Commande**.</span><span class="sxs-lookup"><span data-stu-id="66d89-569">Use *Player*.**ScriptCommand**.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="66d89-570">*Player6*. **Avertissement**</span><span class="sxs-lookup"><span data-stu-id="66d89-570">*Player6*.**Warning**</span></span>           | <span data-ttu-id="66d89-571">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="66d89-571">Not available.</span></span>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="66d89-572">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66d89-572">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66d89-573">**Guide de migration du modèle objet**</span><span class="sxs-lookup"><span data-stu-id="66d89-573">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="66d89-574">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="66d89-574">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





