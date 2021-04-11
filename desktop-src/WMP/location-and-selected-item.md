---
title: Emplacement et élément sélectionné
description: Emplacement et élément sélectionné
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Magasins en ligne Windows Media Player, emplacements
- magasins en ligne, emplacements
- tapez 1 magasins en ligne, emplacements
- Magasins en ligne Windows Media Player, emplacements de bibliothèque
- magasins en ligne, emplacements de bibliothèque
- types 1 magasins en ligne, emplacements de bibliothèque
- Windows Media Player Online stores, éléments sélectionnés
- magasins en ligne, éléments sélectionnés
- tapez 1 magasins en ligne, éléments sélectionnés
- Bibliothèque du lecteur Windows Media, emplacements
- Bibliothèque du lecteur Windows Media, éléments sélectionnés
- bibliothèque, emplacements
- bibliothèque, éléments sélectionnés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196687"
---
# <a name="location-and-selected-item"></a><span data-ttu-id="14560-116">Emplacement et élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-116">Location and Selected Item</span></span>

<span data-ttu-id="14560-117">Le lecteur Windows Media utilise les cinq éléments suivants pour caractériser son affichage actuel du contenu de la boutique en ligne :</span><span class="sxs-lookup"><span data-stu-id="14560-117">Windows Media Player uses the following five items to characterize its current view of online store content:</span></span>

-   <span data-ttu-id="14560-118">tâche</span><span class="sxs-lookup"><span data-stu-id="14560-118">task</span></span>
-   <span data-ttu-id="14560-119">type d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-119">library location type</span></span>
-   <span data-ttu-id="14560-120">ID d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-120">library location ID</span></span>
-   <span data-ttu-id="14560-121">type d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-121">selected item type</span></span>
-   <span data-ttu-id="14560-122">ID de l’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-122">selected item ID</span></span>

<span data-ttu-id="14560-123">En règle générale, vous pouvez considérer la vue dans le lecteur Windows Media comme un conteneur d’éléments.</span><span class="sxs-lookup"><span data-stu-id="14560-123">Typically, you can think of the view in Windows Media Player as a container of items.</span></span> <span data-ttu-id="14560-124">Le conteneur a un type et un élément a un type.</span><span class="sxs-lookup"><span data-stu-id="14560-124">The container has a type, and an item has a type.</span></span> <span data-ttu-id="14560-125">Tous les éléments d’un conteneur ont le même type.</span><span class="sxs-lookup"><span data-stu-id="14560-125">All the items in a container have the same type.</span></span> <span data-ttu-id="14560-126">Les types d’emplacement et les types d’élément sont spécifiés par les [constantes d’emplacement](library-location-constants.md)de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="14560-126">Location types and item types are both specified by the [library location constants](library-location-constants.md).</span></span> <span data-ttu-id="14560-127">Par exemple, si la vue actuelle affiche un album individuel, le type d’emplacement de la bibliothèque est CPAlbumID et, étant donné qu’un album contient des suivis, le type d’élément sélectionné est CPTrackID.</span><span class="sxs-lookup"><span data-stu-id="14560-127">For example, if the current view is showing an individual album, the library location type is CPAlbumID, and, because an album contains tracks, the selected item type is CPTrackID.</span></span>

<span data-ttu-id="14560-128">Le tableau suivant montre l’emplacement et les types d’éléments de plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="14560-128">The following table shows the location and item types for several containers.</span></span>



| <span data-ttu-id="14560-129">Description du conteneur</span><span class="sxs-lookup"><span data-stu-id="14560-129">Description of container</span></span>                              | <span data-ttu-id="14560-130">Type d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-130">Library location type</span></span> | <span data-ttu-id="14560-131">Type d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-131">Selected item type</span></span> |
|-------------------------------------------------------|-----------------------|--------------------|
| <span data-ttu-id="14560-132">Un album qui est un conteneur de pistes</span><span class="sxs-lookup"><span data-stu-id="14560-132">An album that is a container of tracks</span></span>                | <span data-ttu-id="14560-133">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="14560-133">CPAlbumID</span></span>             | <span data-ttu-id="14560-134">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="14560-134">CPTrackID</span></span>          |
| <span data-ttu-id="14560-135">Liste qui est un conteneur de pistes</span><span class="sxs-lookup"><span data-stu-id="14560-135">A list that is a container of tracks</span></span>                  | <span data-ttu-id="14560-136">CPListID</span><span class="sxs-lookup"><span data-stu-id="14560-136">CPListID</span></span>              | <span data-ttu-id="14560-137">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="14560-137">CPTrackID</span></span>          |
| <span data-ttu-id="14560-138">Liste qui est un conteneur d’albums</span><span class="sxs-lookup"><span data-stu-id="14560-138">A list that is a container of albums</span></span>                  | <span data-ttu-id="14560-139">CPListID</span><span class="sxs-lookup"><span data-stu-id="14560-139">CPListID</span></span>              | <span data-ttu-id="14560-140">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="14560-140">CPAlbumID</span></span>          |
| <span data-ttu-id="14560-141">Station de radio qui est un conteneur de listes</span><span class="sxs-lookup"><span data-stu-id="14560-141">A radio station that is a container of lists</span></span>          | <span data-ttu-id="14560-142">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="14560-142">CPRadioID</span></span>             | <span data-ttu-id="14560-143">CPListID</span><span class="sxs-lookup"><span data-stu-id="14560-143">CPListID</span></span>           |
| <span data-ttu-id="14560-144">Ensemble de tous les albums, qui est un conteneur d’albums</span><span class="sxs-lookup"><span data-stu-id="14560-144">The set of all albums, which is a container of albums</span></span> | <span data-ttu-id="14560-145">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="14560-145">AllCPAlbumIDs</span></span>         | <span data-ttu-id="14560-146">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="14560-146">CPAlbumID</span></span>          |
| <span data-ttu-id="14560-147">Ensemble de tous les genres, qui est un conteneur de genres</span><span class="sxs-lookup"><span data-stu-id="14560-147">The set of all genres, which is a container of genres</span></span> | <span data-ttu-id="14560-148">AllCPGenreIDs</span><span class="sxs-lookup"><span data-stu-id="14560-148">AllCPGenreIDs</span></span>         | <span data-ttu-id="14560-149">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="14560-149">CPGenreID</span></span>          |



 

<span data-ttu-id="14560-150">Les onglets du lecteur Windows Media représentent des tâches différentes.</span><span class="sxs-lookup"><span data-stu-id="14560-150">The tabs in Windows Media Player represent different tasks.</span></span> <span data-ttu-id="14560-151">Le lecteur affiche le contenu de la boutique en ligne dans trois volets de tâches différents : **bibliothèque**, **gravure** et **synchronisation**. Le volet des tâches de la bibliothèque est également appelé volet des tâches **Parcourir** .</span><span class="sxs-lookup"><span data-stu-id="14560-151">The Player displays online store content in three different task panes: **Library**, **Burn**, and **Sync**. The Library task pane is also called the **Browse** task pane.</span></span> <span data-ttu-id="14560-152">Parfois, un volet de tâches est appelé *fonctionnalité*. vous pouvez donc voir des termes tels que la fonctionnalité de *gravure* et la *fonctionnalité de synchronisation* dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="14560-152">Sometimes, a task pane is called a *feature*, so you might see terms like *Burn feature* and *Sync feature* in this documentation.</span></span>

<span data-ttu-id="14560-153">Les exemples suivants montrent comment le lecteur Windows Media utilise les cinq éléments d’information (tâche, type d’emplacement de la bibliothèque, ID d’emplacement de la bibliothèque, type d’élément sélectionné, ID d’élément sélectionné) pour caractériser différentes vues.</span><span class="sxs-lookup"><span data-stu-id="14560-153">The following examples show how Windows Media Player uses the five pieces of information (task, library location type, library location ID, selected item type, selected Item ID) to characterize different views.</span></span>

<span data-ttu-id="14560-154">Dans le volet de tâches **graver** , le lecteur affiche un album en tant que conteneur de pistes.</span><span class="sxs-lookup"><span data-stu-id="14560-154">In the **Burn** task pane, the Player is displaying an album as a container of tracks.</span></span> <span data-ttu-id="14560-155">L’ID de l’album est 250.</span><span class="sxs-lookup"><span data-stu-id="14560-155">The album has an ID of 250.</span></span> <span data-ttu-id="14560-156">Dans la vue, l’élément sélectionné est la piste qui a l’ID 800.</span><span class="sxs-lookup"><span data-stu-id="14560-156">In the view, the selected item is the track that has an ID of 800.</span></span> <span data-ttu-id="14560-157">Notez que 800 est l’ID de la piste dans le catalogue du magasin en ligne, et non le numéro de la piste sur l’album.</span><span class="sxs-lookup"><span data-stu-id="14560-157">Note that 800 is the ID of the track in the online store's catalog, not the number of the track on the album.</span></span>



| <span data-ttu-id="14560-158">Élément</span><span class="sxs-lookup"><span data-stu-id="14560-158">Item</span></span>                  | <span data-ttu-id="14560-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="14560-159">Value</span></span>     |
|-----------------------|-----------|
| <span data-ttu-id="14560-160">tâche</span><span class="sxs-lookup"><span data-stu-id="14560-160">task</span></span>                  | <span data-ttu-id="14560-161">Écrire</span><span class="sxs-lookup"><span data-stu-id="14560-161">Burn</span></span>      |
| <span data-ttu-id="14560-162">type d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-162">library location type</span></span> | <span data-ttu-id="14560-163">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="14560-163">CPAlbumID</span></span> |
| <span data-ttu-id="14560-164">ID d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-164">library location ID</span></span>   | <span data-ttu-id="14560-165">250</span><span class="sxs-lookup"><span data-stu-id="14560-165">250</span></span>       |
| <span data-ttu-id="14560-166">type d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-166">selected item type</span></span>    | <span data-ttu-id="14560-167">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="14560-167">CPTrackID</span></span> |
| <span data-ttu-id="14560-168">ID de l’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-168">selected item ID</span></span>      | <span data-ttu-id="14560-169">800</span><span class="sxs-lookup"><span data-stu-id="14560-169">800</span></span>       |



 

<span data-ttu-id="14560-170">Dans le volet de tâches **synchroniser** , le lecteur affiche l’ensemble de tous les albums, qui est un conteneur d’albums.</span><span class="sxs-lookup"><span data-stu-id="14560-170">In the **Sync** task pane, the Player is displaying the set of all albums, which is a container of albums.</span></span> <span data-ttu-id="14560-171">Dans la vue, l’élément sélectionné est l’album dont l’ID est 300.</span><span class="sxs-lookup"><span data-stu-id="14560-171">In the view, the selected item is the album that has an ID of 300.</span></span> <span data-ttu-id="14560-172">Notez que l’ID d’emplacement de la bibliothèque n’est pas applicable à cette vue.</span><span class="sxs-lookup"><span data-stu-id="14560-172">Note that the library location ID is not applicable to this view.</span></span>



| <span data-ttu-id="14560-173">Élément</span><span class="sxs-lookup"><span data-stu-id="14560-173">Item</span></span>                  | <span data-ttu-id="14560-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="14560-174">Value</span></span>         |
|-----------------------|---------------|
| <span data-ttu-id="14560-175">tâche</span><span class="sxs-lookup"><span data-stu-id="14560-175">task</span></span>                  | <span data-ttu-id="14560-176">Synchronisation</span><span class="sxs-lookup"><span data-stu-id="14560-176">Sync</span></span>          |
| <span data-ttu-id="14560-177">type d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-177">library location type</span></span> | <span data-ttu-id="14560-178">AllCPAlbumIDs</span><span class="sxs-lookup"><span data-stu-id="14560-178">AllCPAlbumIDs</span></span> |
| <span data-ttu-id="14560-179">ID d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-179">library location ID</span></span>   | <span data-ttu-id="14560-180">N/A</span><span class="sxs-lookup"><span data-stu-id="14560-180">N/A</span></span>           |
| <span data-ttu-id="14560-181">type d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-181">selected item type</span></span>    | <span data-ttu-id="14560-182">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="14560-182">CPAlbumID</span></span>     |
| <span data-ttu-id="14560-183">ID de l’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-183">selected item ID</span></span>      | <span data-ttu-id="14560-184">300</span><span class="sxs-lookup"><span data-stu-id="14560-184">300</span></span>           |



 

<span data-ttu-id="14560-185">Dans le contrôle Tree-View, le nœud racine du magasin en ligne est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="14560-185">In the tree-view control, the root node for the online store is selected.</span></span> <span data-ttu-id="14560-186">Dans ce cas, il n’y a aucun conteneur et, par conséquent, il n’y a aucun élément.</span><span class="sxs-lookup"><span data-stu-id="14560-186">In this case, there is no container, and consequently, there are no items.</span></span> <span data-ttu-id="14560-187">Le volet des tâches **bibliothèque** complète affiche une page de détection.</span><span class="sxs-lookup"><span data-stu-id="14560-187">The entire **Library** task pane is displaying a discovery page.</span></span>



| <span data-ttu-id="14560-188">Élément</span><span class="sxs-lookup"><span data-stu-id="14560-188">Item</span></span>                  | <span data-ttu-id="14560-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="14560-189">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="14560-190">tâche</span><span class="sxs-lookup"><span data-stu-id="14560-190">task</span></span>                  | <span data-ttu-id="14560-191">Parcourir</span><span class="sxs-lookup"><span data-stu-id="14560-191">Browse</span></span>          |
| <span data-ttu-id="14560-192">type d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-192">library location type</span></span> | <span data-ttu-id="14560-193">RootLocation</span><span class="sxs-lookup"><span data-stu-id="14560-193">RootLocation</span></span>    |
| <span data-ttu-id="14560-194">ID d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-194">library location ID</span></span>   | <span data-ttu-id="14560-195">N/A</span><span class="sxs-lookup"><span data-stu-id="14560-195">N/A</span></span>             |
| <span data-ttu-id="14560-196">type d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-196">selected item type</span></span>    | <span data-ttu-id="14560-197">UnknownLocation</span><span class="sxs-lookup"><span data-stu-id="14560-197">UnknownLocation</span></span> |
| <span data-ttu-id="14560-198">ID de l’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-198">selected item ID</span></span>      | <span data-ttu-id="14560-199">N/A</span><span class="sxs-lookup"><span data-stu-id="14560-199">N/A</span></span>             |



 

<span data-ttu-id="14560-200">Dans le volet de tâches **synchronisation** , le lecteur affiche l’année 2002 en tant que conteneur de pistes.</span><span class="sxs-lookup"><span data-stu-id="14560-200">In the **Sync** task pane, the Player is displaying the year 2002 as a container of tracks.</span></span> <span data-ttu-id="14560-201">Dans la vue, l’élément sélectionné est la piste qui a l’ID 450.</span><span class="sxs-lookup"><span data-stu-id="14560-201">In the view, the selected item is the track that has an ID of 450.</span></span>



| <span data-ttu-id="14560-202">Élément</span><span class="sxs-lookup"><span data-stu-id="14560-202">Item</span></span>                  | <span data-ttu-id="14560-203">Valeur</span><span class="sxs-lookup"><span data-stu-id="14560-203">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="14560-204">tâche</span><span class="sxs-lookup"><span data-stu-id="14560-204">task</span></span>                  | <span data-ttu-id="14560-205">Synchronisation</span><span class="sxs-lookup"><span data-stu-id="14560-205">Sync</span></span>            |
| <span data-ttu-id="14560-206">type d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-206">library location type</span></span> | <span data-ttu-id="14560-207">ReleaseDateYear</span><span class="sxs-lookup"><span data-stu-id="14560-207">ReleaseDateYear</span></span> |
| <span data-ttu-id="14560-208">ID d’emplacement de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14560-208">library location ID</span></span>   | <span data-ttu-id="14560-209">2002</span><span class="sxs-lookup"><span data-stu-id="14560-209">2002</span></span>            |
| <span data-ttu-id="14560-210">type d’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-210">selected item type</span></span>    | <span data-ttu-id="14560-211">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="14560-211">CPTrackID</span></span>       |
| <span data-ttu-id="14560-212">ID de l’élément sélectionné</span><span class="sxs-lookup"><span data-stu-id="14560-212">selected item ID</span></span>      | <span data-ttu-id="14560-213">450</span><span class="sxs-lookup"><span data-stu-id="14560-213">450</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="14560-214">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14560-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14560-215">**À propos des magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="14560-215">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="14560-216">**Pages de découverte**</span><span class="sxs-lookup"><span data-stu-id="14560-216">**Discovery Pages**</span></span>](discovery-pages.md)
</dt> </dl>

 

 




