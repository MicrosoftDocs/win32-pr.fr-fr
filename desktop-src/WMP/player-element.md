---
title: Élément PLAYER
description: Élément PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Apparences du lecteur Windows Media, élément lecteur
- Skins, élément PLAYER
- Élément PLAYER
- informations de référence sur les habillages, élément PLAYER
- éléments, joueur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100757"
---
# <a name="player-element"></a><span data-ttu-id="e2a77-108">Élément PLAYER</span><span class="sxs-lookup"><span data-stu-id="e2a77-108">PLAYER Element</span></span>

<span data-ttu-id="e2a77-109">L’élément **Player** vous permet de définir des gestionnaires d’événements et de spécifier la propriété **URL** de l’objet **Player** au moment du design au sein d’un fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="e2a77-109">The **PLAYER** element lets you define event handlers and specify the **URL** property of the **Player** object at design time within a skin definition file.</span></span> <span data-ttu-id="e2a77-110">Dans le code de script, l’objet **Player** est accessible par le biais de l’attribut global **Player** plutôt que via un nom spécifié par un attribut **ID** , ce qui n’est pas pris en charge par l’élément **Player** .</span><span class="sxs-lookup"><span data-stu-id="e2a77-110">Within script code, the **Player** object is accessed through the **player** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **PLAYER** element.</span></span>

<span data-ttu-id="e2a77-111">L’élément **Player** prend en charge l’attribut suivant.</span><span class="sxs-lookup"><span data-stu-id="e2a77-111">The **PLAYER** element supports the following attribute.</span></span>



| <span data-ttu-id="e2a77-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="e2a77-112">Attribute</span></span>             | <span data-ttu-id="e2a77-113">Description</span><span class="sxs-lookup"><span data-stu-id="e2a77-113">Description</span></span>                                          |
|-----------------------|------------------------------------------------------|
| [<span data-ttu-id="e2a77-114">URL</span><span class="sxs-lookup"><span data-stu-id="e2a77-114">URL</span></span>](player-url.md) | <span data-ttu-id="e2a77-115">Spécifie ou récupère le nom du fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="e2a77-115">Specifies or retrieves the name of the file to play.</span></span> |



 

<span data-ttu-id="e2a77-116">L’élément **Player** peut implémenter des gestionnaires d’événements pour les événements suivants déclenchés à partir de l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="e2a77-116">The **PLAYER** element can implement event handlers for the following events fired from the **Player** object.</span></span>



| <span data-ttu-id="e2a77-117">Événement</span><span class="sxs-lookup"><span data-stu-id="e2a77-117">Event</span></span>                                                                                            | <span data-ttu-id="e2a77-118">Description</span><span class="sxs-lookup"><span data-stu-id="e2a77-118">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="e2a77-119">AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-119">AudioLanguageChange</span></span>](player-player-audiolanguagechange.md)                                     | <span data-ttu-id="e2a77-120">Se produit lorsque le langage audio actuel change.</span><span class="sxs-lookup"><span data-stu-id="e2a77-120">Occurs when the current audio language changes.</span></span>                                  |
| [<span data-ttu-id="e2a77-121">des réponses</span><span class="sxs-lookup"><span data-stu-id="e2a77-121">Buffering</span></span>](player-player-buffering.md)                                                         | <span data-ttu-id="e2a77-122">Se produit lorsque le lecteur Windows Media commence ou met fin à la mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e2a77-122">Occurs when Windows Media Player begins or ends buffering.</span></span>                       |
| [<span data-ttu-id="e2a77-123">CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-123">CdromMediaChange</span></span>](player-player-cdrommediachange.md)                                           | <span data-ttu-id="e2a77-124">Se produit lorsque le support CD change.</span><span class="sxs-lookup"><span data-stu-id="e2a77-124">Occurs when the CD media changes.</span></span>                                                |
| [<span data-ttu-id="e2a77-125">CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-125">CurrentItemChange</span></span>](player-player-currentitemchange.md)                                         | <span data-ttu-id="e2a77-126">Se produit lorsque l’élément actuel change.</span><span class="sxs-lookup"><span data-stu-id="e2a77-126">Occurs when the current item changes.</span></span>                                            |
| [<span data-ttu-id="e2a77-127">CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="e2a77-127">CurrentMediaItemAvailable</span></span>](player-player-currentmediaitemavailable.md)                         | <span data-ttu-id="e2a77-128">Se produit lorsque l’élément multimédia actuel devient disponible.</span><span class="sxs-lookup"><span data-stu-id="e2a77-128">Occurs when the current media item becomes available.</span></span>                            |
| [<span data-ttu-id="e2a77-129">CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-129">CurrentPlaylistChange</span></span>](player-player-currentplaylistchange.md)                                 | <span data-ttu-id="e2a77-130">Se produit lors de la modification de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="e2a77-130">Occurs when the current playlist changes.</span></span>                                        |
| [<span data-ttu-id="e2a77-131">CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="e2a77-131">CurrentPlaylistItemAvailable</span></span>](player-player-currentplaylistitemavailable.md)                   | <span data-ttu-id="e2a77-132">Se produit lorsque l’élément de sélection actuel devient disponible.</span><span class="sxs-lookup"><span data-stu-id="e2a77-132">Occurs when the current playlist item becomes available.</span></span>                         |
| [<span data-ttu-id="e2a77-133">DomainChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-133">DomainChange</span></span>](player-player-domainchange.md)                                                   | <span data-ttu-id="e2a77-134">Se produit lorsque le domaine DVD change.</span><span class="sxs-lookup"><span data-stu-id="e2a77-134">Occurs when the DVD domain changes.</span></span>                                              |
| [<span data-ttu-id="e2a77-135">Error</span><span class="sxs-lookup"><span data-stu-id="e2a77-135">Error</span></span>](player-player-error.md)                                                                 | <span data-ttu-id="e2a77-136">Se produit lorsque le contrôle du lecteur Windows Media a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e2a77-136">Occurs when the Windows Media Player control has an error condition.</span></span>             |
| [<span data-ttu-id="e2a77-137">MarkerHit</span><span class="sxs-lookup"><span data-stu-id="e2a77-137">MarkerHit</span></span>](player-player-markerhit.md)                                                         | <span data-ttu-id="e2a77-138">Se produit lorsque le lecteur Windows Media rencontre un marqueur dans le clip.</span><span class="sxs-lookup"><span data-stu-id="e2a77-138">Occurs when Windows Media Player encounters a marker in the clip.</span></span>                |
| [<span data-ttu-id="e2a77-139">MediaChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-139">MediaChange</span></span>](player-player-mediachange.md)                                                     | <span data-ttu-id="e2a77-140">Se produit lorsqu’un élément multimédia change.</span><span class="sxs-lookup"><span data-stu-id="e2a77-140">Occurs when a media item changes.</span></span>                                                |
| [<span data-ttu-id="e2a77-141">MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="e2a77-141">MediaCollectionAttributeStringAdded</span></span>](player-player-mediacollectionattributestringadded.md)     | <span data-ttu-id="e2a77-142">Se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e2a77-142">Occurs when an attribute value is added to the library.</span></span>                          |
| [<span data-ttu-id="e2a77-143">MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="e2a77-143">MediaCollectionAttributeStringChanged</span></span>](player-player-mediacollectionattributestringchanged.md) | <span data-ttu-id="e2a77-144">Se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée.</span><span class="sxs-lookup"><span data-stu-id="e2a77-144">Occurs when an attribute value in the library is changed.</span></span>                        |
| [<span data-ttu-id="e2a77-145">MediaCollectionAttributeStringRemoved</span><span class="sxs-lookup"><span data-stu-id="e2a77-145">MediaCollectionAttributeStringRemoved</span></span>](player-player-mediacollectionattributestringremoved.md) | <span data-ttu-id="e2a77-146">Se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e2a77-146">Occurs when an attribute value is removed from the library.</span></span>                      |
| [<span data-ttu-id="e2a77-147">MediaCollectionChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-147">MediaCollectionChange</span></span>](player-player-mediacollectionchange.md)                                 | <span data-ttu-id="e2a77-148">Se produit lorsque l’objet **MediaCollection** est modifié.</span><span class="sxs-lookup"><span data-stu-id="e2a77-148">Occurs when the **MediaCollection** object changes.</span></span>                              |
| [<span data-ttu-id="e2a77-149">MediaError</span><span class="sxs-lookup"><span data-stu-id="e2a77-149">MediaError</span></span>](player-player-mediaerror.md)                                                       | <span data-ttu-id="e2a77-150">Se produit lorsque l’objet **multimédia** a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e2a77-150">Occurs when the **Media** object has an error condition.</span></span>                         |
| [<span data-ttu-id="e2a77-151">ModeChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-151">ModeChange</span></span>](player-player-modechange.md)                                                       | <span data-ttu-id="e2a77-152">Se produit lors du basculement entre le mode aléatoire et le mode normal.</span><span class="sxs-lookup"><span data-stu-id="e2a77-152">Occurs when switching between shuffle and normal mode.</span></span>                           |
| [<span data-ttu-id="e2a77-153">OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="e2a77-153">OpenPlaylistSwitch</span></span>](player-player-openplaylistswitch.md)                                       | <span data-ttu-id="e2a77-154">Se produit lorsqu’un titre sur un DVD commence à être lu.</span><span class="sxs-lookup"><span data-stu-id="e2a77-154">Occurs when a title on a DVD begins playing.</span></span>                                     |
| [<span data-ttu-id="e2a77-155">OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-155">OpenStateChange</span></span>](player-player-openstatechange.md)                                             | <span data-ttu-id="e2a77-156">Se produit lorsque *Player*. **openState** change.</span><span class="sxs-lookup"><span data-stu-id="e2a77-156">Occurs when *player*.**openState** changes.</span></span>                                      |
| [<span data-ttu-id="e2a77-157">PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-157">PlaylistChange</span></span>](player-player-playlistchange.md)                                               | <span data-ttu-id="e2a77-158">Se produit lorsqu’une sélection est modifiée.</span><span class="sxs-lookup"><span data-stu-id="e2a77-158">Occurs when a playlist changes.</span></span>                                                  |
| [<span data-ttu-id="e2a77-159">PlaylistCollectionChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-159">PlaylistCollectionChange</span></span>](player-player-playlistcollectionchange.md)                           | <span data-ttu-id="e2a77-160">Se produit lors d’une modification de la collection de sélections.</span><span class="sxs-lookup"><span data-stu-id="e2a77-160">Occurs when something changes in the playlist collection.</span></span>                        |
| [<span data-ttu-id="e2a77-161">PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="e2a77-161">PlaylistCollectionPlaylistAdded</span></span>](player-player-playlistcollectionplaylistadded.md)             | <span data-ttu-id="e2a77-162">Se produit lorsqu’une sélection est ajoutée à la collection de sélections.</span><span class="sxs-lookup"><span data-stu-id="e2a77-162">Occurs when a playlist is added to the playlist collection.</span></span>                      |
| [<span data-ttu-id="e2a77-163">PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="e2a77-163">PlaylistCollectionPlaylistRemoved</span></span>](player-player-playlistcollectionplaylistremoved.md)         | <span data-ttu-id="e2a77-164">Se produit lorsqu’une sélection est supprimée de la collection de sélections.</span><span class="sxs-lookup"><span data-stu-id="e2a77-164">Occurs when a playlist is removed from the playlist collection.</span></span>                  |
| [<span data-ttu-id="e2a77-165">PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-165">PlayStateChange</span></span>](player-player-playstatechange.md)                                             | <span data-ttu-id="e2a77-166">Se produit lorsque *Player*. **lecture** change.</span><span class="sxs-lookup"><span data-stu-id="e2a77-166">Occurs when *player*.**playState** changes.</span></span>                                      |
| [<span data-ttu-id="e2a77-167">PositionChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-167">PositionChange</span></span>](player-player-positionchange.md)                                               | <span data-ttu-id="e2a77-168">Se produit lorsque *Player*. *contrôles*. **CurrentPosition** change.</span><span class="sxs-lookup"><span data-stu-id="e2a77-168">Occurs when *player*.*controls*.**currentPosition** changes.</span></span>                     |
| [<span data-ttu-id="e2a77-169">ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="e2a77-169">ScriptCommand</span></span>](player-player-scriptcommand.md)                                                 | <span data-ttu-id="e2a77-170">Se produit lorsque le lecteur Windows Media rencontre une commande de script incorporée dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="e2a77-170">Occurs when Windows Media Player encounters a script command embedded in a file.</span></span> |
| [<span data-ttu-id="e2a77-171">StatusChange</span><span class="sxs-lookup"><span data-stu-id="e2a77-171">StatusChange</span></span>](player-player-statuschange.md)                                                   | <span data-ttu-id="e2a77-172">Se produit lorsque la propriété **Status** change de valeur.</span><span class="sxs-lookup"><span data-stu-id="e2a77-172">Occurs when the **status** property changes value.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="e2a77-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2a77-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2a77-174">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="e2a77-174">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="e2a77-175">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="e2a77-175">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




