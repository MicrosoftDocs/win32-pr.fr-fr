---
title: Référence du modèle objet pour l’écriture de scripts
description: Référence du modèle objet pour l’écriture de scripts
ms.assetid: a900fd55-2213-46db-84ad-93f199c60182
keywords:
- Lecteur Windows Media, modèle objet
- Windows Media Player Mobile, modèle objet
- Modèle objet du lecteur Windows Media, référence
- modèle objet, référence
- Contrôle ActiveX, référence
- Contrôle ActiveX du lecteur Windows Media, référence
- Windows Media Player Mobile contrôle ActiveX, référence
- référence pour le modèle d’objet, script
- Lecteur Windows Media, référence de script
- Windows Media Player Mobile, référence de script
- Windows Media Player Object Model, référence de script
- modèle objet, référence de script
- Contrôle ActiveX du lecteur Windows Media, référence de script
- Windows Media Player Mobile contrôle ActiveX, référence de script
- Contrôle ActiveX, référence de script
- Référence du modèle objet de script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f20e5bacf6a1fd93579ce40e8957b7ce7aefae0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510626"
---
# <a name="object-model-reference-for-scripting"></a><span data-ttu-id="1e894-119">Référence du modèle objet pour l’écriture de scripts</span><span class="sxs-lookup"><span data-stu-id="1e894-119">Object Model Reference for Scripting</span></span>

<span data-ttu-id="1e894-120">La référence du modèle objet pour les scripts contient des informations détaillées sur le modèle objet de contrôle ActiveX du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e894-120">The object model reference for scripting contains detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="1e894-121">Les informations de cette section sont présentées dans un style conçu pour être utilisé avec des langages de script tels que Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="1e894-121">The information in this section is presented in a style designed for use with script languages like Microsoft JScript.</span></span>

> [!Note]  
> <span data-ttu-id="1e894-122">Toutes les méthodes, propriétés et événements sont entièrement pris en charge dans le lecteur Windows Media 10 mobile ou ultérieur, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="1e894-122">All methods, properties, and events are fully supported in Windows Media Player 10 Mobile or later unless explicitly stated otherwise.</span></span>

 

<span data-ttu-id="1e894-123">La référence du modèle objet pour les scripts contient la documentation pour les objets suivants, ainsi que les méthodes, propriétés et événements associés.</span><span class="sxs-lookup"><span data-stu-id="1e894-123">The object model reference for scripting contains documentation for the following objects and their associated methods, properties, and events.</span></span>



| <span data-ttu-id="1e894-124">Object</span><span class="sxs-lookup"><span data-stu-id="1e894-124">Object</span></span>                                              | <span data-ttu-id="1e894-125">Description</span><span class="sxs-lookup"><span data-stu-id="1e894-125">Description</span></span>                                                                                                                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e894-126">-</span><span class="sxs-lookup"><span data-stu-id="1e894-126">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="1e894-127">Méthodes et propriétés d’accès à un CD ou un DVD dans son lecteur.</span><span class="sxs-lookup"><span data-stu-id="1e894-127">Methods and properties for accessing a CD or DVD in its drive.</span></span>                                                                                                                                 |
| [<span data-ttu-id="1e894-128">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="1e894-128">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="1e894-129">Méthodes et propriétés permettant d’accéder à une collection de lecteurs de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="1e894-129">Methods and properties for accessing a collection of CD or DVD drives.</span></span>                                                                                                                         |
| [<span data-ttu-id="1e894-130">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="1e894-130">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="1e894-131">Propriétés pour l’inclusion de légendes avec un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="1e894-131">Properties for including captions with a media item.</span></span>                                                                                                                                           |
| [<span data-ttu-id="1e894-132">Contrôles</span><span class="sxs-lookup"><span data-stu-id="1e894-132">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="1e894-133">Méthodes et propriétés représentant les contrôles de transport du lecteur Windows Media, tels que lecture, arrêt et pause.</span><span class="sxs-lookup"><span data-stu-id="1e894-133">Methods and properties representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>                                                                             |
| [<span data-ttu-id="1e894-134">DVD</span><span class="sxs-lookup"><span data-stu-id="1e894-134">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="1e894-135">Une propriété, des méthodes et des événements pour travailler avec des DVD.</span><span class="sxs-lookup"><span data-stu-id="1e894-135">A property, methods, and events for working with DVDs.</span></span>                                                                                                                                         |
| [<span data-ttu-id="1e894-136">Error</span><span class="sxs-lookup"><span data-stu-id="1e894-136">Error</span></span>](error-object.md)                           | <span data-ttu-id="1e894-137">Méthodes et propriétés permettant d’accéder à une collection d’objets **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="1e894-137">Methods and properties providing access to a collection of **ErrorItem** objects.</span></span>                                                                                                              |
| [<span data-ttu-id="1e894-138">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="1e894-138">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="1e894-139">Propriétés qui fournissent des informations sur les erreurs.</span><span class="sxs-lookup"><span data-stu-id="1e894-139">Properties that provide information about errors.</span></span>                                                                                                                                              |
| [<span data-ttu-id="1e894-140">Média</span><span class="sxs-lookup"><span data-stu-id="1e894-140">Media</span></span>](media-object.md)                           | <span data-ttu-id="1e894-141">Méthodes et propriétés relatives aux éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="1e894-141">Methods and properties relating to media items.</span></span>                                                                                                                                                |
| [<span data-ttu-id="1e894-142">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="1e894-142">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="1e894-143">Méthodes qui fournissent l’accès à une collection d’objets **multimédias** .</span><span class="sxs-lookup"><span data-stu-id="1e894-143">Methods that provide access to a collection of **Media** objects.</span></span>                                                                                                                              |
| [<span data-ttu-id="1e894-144">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="1e894-144">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="1e894-145">Propriétés permettant de récupérer des informations sur les valeurs d’image de l’attribut de métadonnées **WM/Picture** .</span><span class="sxs-lookup"><span data-stu-id="1e894-145">Properties for retrieving information on the image values of the **WM/Picture** metadata attribute.</span></span>                                                                                            |
| [<span data-ttu-id="1e894-146">MetadataText</span><span class="sxs-lookup"><span data-stu-id="1e894-146">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="1e894-147">Propriétés pour la récupération de métadonnées pour les attributs de métadonnées textuelles complexes.</span><span class="sxs-lookup"><span data-stu-id="1e894-147">Properties for retrieving metadata for complex textual metadata attributes.</span></span>                                                                                                                    |
| [<span data-ttu-id="1e894-148">Réseau</span><span class="sxs-lookup"><span data-stu-id="1e894-148">Network</span></span>](network-object.md)                       | <span data-ttu-id="1e894-149">Propriétés relatives à la connexion réseau du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e894-149">Properties relating to the network connection of Windows Media Player.</span></span>                                                                                                                         |
| [<span data-ttu-id="1e894-150">Lecteur</span><span class="sxs-lookup"><span data-stu-id="1e894-150">Player</span></span>](player-object.md)                         | <span data-ttu-id="1e894-151">Méthodes, propriétés et événements auxquels le lecteur Windows Media peut être programmé pour répondre.</span><span class="sxs-lookup"><span data-stu-id="1e894-151">Methods, properties, and events that Windows Media Player can be programmed to respond to.</span></span>                                                                                                     |
| [<span data-ttu-id="1e894-152">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="1e894-152">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="1e894-153">Méthodes et propriétés pour basculer entre un contrôle du lecteur Windows Media distant et le mode complet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="1e894-153">Methods and properties for switching between a remoted Windows Media Player control and the full mode of the Player.</span></span> <span data-ttu-id="1e894-154">Peut uniquement être utilisé avec les programmes C++ qui incorporent le contrôle en mode distant.</span><span class="sxs-lookup"><span data-stu-id="1e894-154">Can only be used with C++ programs that embed the control in remote mode.</span></span> |
| [<span data-ttu-id="1e894-155">Playlist</span><span class="sxs-lookup"><span data-stu-id="1e894-155">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="1e894-156">Méthodes et propriétés de manipulation de listes d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="1e894-156">Methods and properties for manipulating lists of media items.</span></span>                                                                                                                                  |
| [<span data-ttu-id="1e894-157">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="1e894-157">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="1e894-158">Une méthode et une propriété permettant d’accéder à une collection d’objets **playlist** par numéro d’index.</span><span class="sxs-lookup"><span data-stu-id="1e894-158">A method and a property for accessing a collection of **Playlist** objects by index number.</span></span>                                                                                                    |
| [<span data-ttu-id="1e894-159">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="1e894-159">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="1e894-160">Méthodes pour organiser une collection d’objets **playlist** .</span><span class="sxs-lookup"><span data-stu-id="1e894-160">Methods for organizing a collection of **Playlist** objects.</span></span>                                                                                                                                   |
| [<span data-ttu-id="1e894-161">Requête</span><span class="sxs-lookup"><span data-stu-id="1e894-161">Query</span></span>](query-object.md)                           | <span data-ttu-id="1e894-162">Méthodes de modification d’une requête composée.</span><span class="sxs-lookup"><span data-stu-id="1e894-162">Methods for modifying a compound query.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="1e894-163">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e894-163">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="1e894-164">Propriétés qui autorisent la spécification ou la récupération des paramètres du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e894-164">Properties that allow the specification or retrieval of Windows Media Player settings.</span></span>                                                                                                         |
| [<span data-ttu-id="1e894-165">StringCollection</span><span class="sxs-lookup"><span data-stu-id="1e894-165">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="1e894-166">Une méthode et une propriété pour manipuler des collections de chaînes.</span><span class="sxs-lookup"><span data-stu-id="1e894-166">A method and a property for manipulating collections of strings.</span></span>                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="1e894-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e894-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e894-168">**Référence du modèle objet du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1e894-168">**Windows Media Player Object Model Reference**</span></span>](windows-media-player-object-model-reference.md)
</dt> </dl>

 

 




