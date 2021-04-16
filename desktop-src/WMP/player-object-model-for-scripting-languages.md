---
title: Modèle objet de lecteur pour les langages de script
description: Modèle objet de lecteur pour les langages de script
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Lecteur Windows Media, modèle objet
- Windows Media Player Object Model, à propos de
- modèle objet, à propos de
- Contrôle ActiveX du lecteur Windows Media, modèle objet
- Contrôle ActiveX, modèle objet
- Windows Media Player Mobile contrôle ActiveX, modèle objet
- Windows Media Player Mobile, modèle objet
- Kit de développement logiciel (SDK), modèle objet de contrôle ActiveX du lecteur Windows Media
- SDK (kit de développement logiciel), modèle objet de contrôle ActiveX du lecteur Windows Media
- documentation, modèle objet de contrôle ActiveX du lecteur Windows Media
- Windows Media Player, langages de script
- Windows Media Player Object Model, langages de script
- modèle objet, langages de script
- Contrôle ActiveX du lecteur Windows Media, langages de script
- Contrôle ActiveX, langages de script
- Windows Media Player Mobile contrôle ActiveX, langages de script
- Windows Media Player Mobile, langages de script
- langages de script
- Lecteur Windows Media, objet Player
- Modèle objet du lecteur Windows Media, objet Player
- modèle objet, objet Player
- Contrôle ActiveX du lecteur Windows Media, objet Player
- Contrôle ActiveX, objet Player
- Windows Media Player Mobile contrôle ActiveX, objet Player
- Windows Media Player Mobile, objet Player
- Objet Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104571074"
---
# <a name="player-object-model-for-scripting-languages"></a><span data-ttu-id="9ad07-129">Modèle objet de lecteur pour les langages de script</span><span class="sxs-lookup"><span data-stu-id="9ad07-129">Player Object Model for Scripting Languages</span></span>

<span data-ttu-id="9ad07-130">ActiveX utilise le concept d’objets pour contenir des fonctionnalités de programmation.</span><span class="sxs-lookup"><span data-stu-id="9ad07-130">ActiveX uses the concept of objects to contain programming functionality.</span></span> <span data-ttu-id="9ad07-131">Le lecteur Windows Media utilise plusieurs objets pour diviser les fonctionnalités fournies par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="9ad07-131">Windows Media Player uses several objects to divide up the functionality the control provides.</span></span> <span data-ttu-id="9ad07-132">L’objet racine est l’objet **Player** , et les autres objets sont attachés à l’objet **Player** par le biais de propriétés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9ad07-132">The root object is the **Player** object, and the other objects are attached to the **Player** object through specific properties.</span></span>

<span data-ttu-id="9ad07-133">Le diagramme suivant montre comment le modèle objet de contrôle ActiveX du lecteur Windows Media 11 fonctionne pour les langages de script.</span><span class="sxs-lookup"><span data-stu-id="9ad07-133">The following diagram shows how the Windows Media Player 11 ActiveX control object model works for scripting languages.</span></span>

![diagramme du modèle objet du lecteur Windows Media 11](images/playeromdiag.png)

<span data-ttu-id="9ad07-135">En C++ et parfois dans les langages .NET, les objets sont représentés par des interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="9ad07-135">In C++, and sometimes in .NET languages, objects are represented by COM interfaces.</span></span> <span data-ttu-id="9ad07-136">Dans le modèle objet du lecteur Windows Media, les noms d’interface COM sont identiques au nom de l’objet, mais ils portent le préfixe « IWMP ».</span><span class="sxs-lookup"><span data-stu-id="9ad07-136">In the Windows Media Player object model, COM interface names are the same as the object name, but are prefixed with "IWMP".</span></span> <span data-ttu-id="9ad07-137">Par exemple, l’objet **réseau** est exposé via l’interface **IWMPNetwork** .</span><span class="sxs-lookup"><span data-stu-id="9ad07-137">For example, the **Network** object is exposed through the **IWMPNetwork** interface.</span></span>

<span data-ttu-id="9ad07-138">Les sections suivantes fournissent des vues d’ensemble conceptuelles pour chaque objet :</span><span class="sxs-lookup"><span data-stu-id="9ad07-138">The following sections provide conceptual overviews for each object:</span></span>

-   [<span data-ttu-id="9ad07-139">À propos des objets cdrom et CdromCollection</span><span class="sxs-lookup"><span data-stu-id="9ad07-139">About the Cdrom and CdromCollection Objects</span></span>](about-the-cdrom-and-cdromcollection-objects.md)
-   [<span data-ttu-id="9ad07-140">À propos de l’objet ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="9ad07-140">About the ClosedCaption Object</span></span>](about-the-closedcaption-object.md)
-   [<span data-ttu-id="9ad07-141">À propos de l’objet contrôles</span><span class="sxs-lookup"><span data-stu-id="9ad07-141">About the Controls Object</span></span>](about-the-controls-object.md)
-   [<span data-ttu-id="9ad07-142">À propos de l’objet DVD</span><span class="sxs-lookup"><span data-stu-id="9ad07-142">About the DVD Object</span></span>](about-the-dvd-object.md)
-   [<span data-ttu-id="9ad07-143">À propos des objets Error et ErrorItem</span><span class="sxs-lookup"><span data-stu-id="9ad07-143">About the Error and ErrorItem Objects</span></span>](about-the-error-and-erroritem-objects.md)
-   [<span data-ttu-id="9ad07-144">À propos des objets MediaCollection et Media</span><span class="sxs-lookup"><span data-stu-id="9ad07-144">About the MediaCollection and Media Objects</span></span>](about-the-mediacollection-and-media-objects.md)
-   [<span data-ttu-id="9ad07-145">À propos de l’objet MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="9ad07-145">About the MetadataPicture Object</span></span>](about-the-metadatapicture-object.md)
-   [<span data-ttu-id="9ad07-146">À propos de l’objet MetadataText</span><span class="sxs-lookup"><span data-stu-id="9ad07-146">About the MetadataText Object</span></span>](about-the-metadatatext-object.md)
-   [<span data-ttu-id="9ad07-147">À propos de l’objet réseau</span><span class="sxs-lookup"><span data-stu-id="9ad07-147">About the Network Object</span></span>](about-the-network-object.md)
-   [<span data-ttu-id="9ad07-148">À propos de l’objet Player</span><span class="sxs-lookup"><span data-stu-id="9ad07-148">About the Player Object</span></span>](about-the-player-object.md)
-   [<span data-ttu-id="9ad07-149">À propos de l’objet PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="9ad07-149">About the PlayerApplication Object</span></span>](about-the-playerapplication-object.md)
-   [<span data-ttu-id="9ad07-150">À propos des objets playlist, PlaylistCollection et PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="9ad07-150">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [<span data-ttu-id="9ad07-151">À propos de l’objet de requête</span><span class="sxs-lookup"><span data-stu-id="9ad07-151">About the Query Object</span></span>](about-the-query-object.md)
-   [<span data-ttu-id="9ad07-152">À propos de l’objet Settings</span><span class="sxs-lookup"><span data-stu-id="9ad07-152">About the Settings Object</span></span>](about-the-settings-object.md)
-   [<span data-ttu-id="9ad07-153">À propos de l’objet StringCollection</span><span class="sxs-lookup"><span data-stu-id="9ad07-153">About the StringCollection Object</span></span>](about-the-stringcollection-object.md)

<span data-ttu-id="9ad07-154">Des fonctionnalités supplémentaires sont disponibles par le biais de certaines interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="9ad07-154">Additional functionality is available through certain COM interfaces.</span></span> <span data-ttu-id="9ad07-155">La possibilité d’accéder à ces interfaces peut dépendre du langage que vous utilisez pour la programmation et d’autres facteurs, tels que le mode utilisé pour créer l’instance du contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9ad07-155">Whether you can access these interfaces may depend on the language you use for programming and other factors, such as the mode used to create the instance of the Windows Media Player control.</span></span> <span data-ttu-id="9ad07-156">Pour obtenir la liste complète des interfaces COM exposées par le contrôle du lecteur Windows Media, consultez la [Référence du modèle objet pour C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="9ad07-156">For a complete list of COM interfaces exposed by the Windows Media Player control, see the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ad07-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ad07-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ad07-158">**À propos du modèle objet Player**</span><span class="sxs-lookup"><span data-stu-id="9ad07-158">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="9ad07-159">**Utilisation du contrôle du lecteur Windows Media dans une solution .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="9ad07-159">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




