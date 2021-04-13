---
title: Accès à la bibliothèque par programmation
description: Accès à la bibliothèque par programmation
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Lecteur Windows Media, bibliothèque
- Modèle objet du lecteur Windows Media, bibliothèque
- modèle objet, bibliothèque
- Contrôle ActiveX du lecteur Windows Media, bibliothèque pour le modèle objet
- Contrôle ActiveX, bibliothèque pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, bibliothèque pour le modèle objet
- Windows Media Player Mobile, bibliothèque pour le modèle objet
- Bibliothèque du lecteur Windows Media, accès par programmation
- bibliothèque, accès
- accès à la bibliothèque du lecteur Windows Media par programmation
- Bibliothèque du lecteur Windows Media, ajout d’éléments multimédias
- bibliothèque, ajout d’éléments multimédias
- Bibliothèque du lecteur Windows Media, récupération d’éléments multimédias
- bibliothèque, récupération d’éléments multimédias
- Bibliothèque du lecteur Windows Media, suppression d’éléments multimédias
- bibliothèque, suppression d’éléments multimédias
- Ajout d’éléments multimédias à la bibliothèque du lecteur Windows Media
- récupération d’éléments multimédias à partir de la bibliothèque du lecteur Windows Media
- suppression d’éléments multimédias de la bibliothèque du lecteur Windows Media
- récupération de métadonnées
- Bibliothèque du lecteur Windows Media, récupération des métadonnées à partir des éléments multimédias
- bibliothèque, récupération de métadonnées à partir d’éléments multimédias
- métadonnées, récupération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380146"
---
# <a name="accessing-the-library-programmatically"></a><span data-ttu-id="b8566-126">Accès à la bibliothèque par programmation</span><span class="sxs-lookup"><span data-stu-id="b8566-126">Accessing the Library Programmatically</span></span>

<span data-ttu-id="b8566-127">Dans le code, la bibliothèque est représentée par l’objet **MediaCollection** (ou l’interface **IWMPMediaCollection** ).</span><span class="sxs-lookup"><span data-stu-id="b8566-127">In code, the library is represented by the **MediaCollection** object (or the **IWMPMediaCollection** interface).</span></span> <span data-ttu-id="b8566-128">Les éléments multimédias sont représentés en tant qu’objets **multimédias** (ou par l’interface **IWMPMedia** ).</span><span class="sxs-lookup"><span data-stu-id="b8566-128">Media items are represented as **Media** objects (or by the **IWMPMedia** interface).</span></span> <span data-ttu-id="b8566-129">Les éléments de sélection sont représentés en tant qu’objets de **sélection** (ou par l’interface **IWMPPlaylist** ).</span><span class="sxs-lookup"><span data-stu-id="b8566-129">Playlist items are represented as **Playlist** objects (or by the **IWMPPlaylist** interface).</span></span> <span data-ttu-id="b8566-130">Par souci de simplicité, cette section fait simplement référence aux noms d’objets, lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="b8566-130">For simplicity, this section will simply refer to object names, when possible.</span></span>

<span data-ttu-id="b8566-131">À l’aide de l’objet **MediaCollection** , vous pouvez travailler avec des éléments multimédias et des sélections.</span><span class="sxs-lookup"><span data-stu-id="b8566-131">By using the **MediaCollection** object, you can work with media items and playlists.</span></span> <span data-ttu-id="b8566-132">La bibliothèque expose également l’objet **PlaylistCollection** (ou l’interface **IWMPPlaylistCollection** ), qui fournit certaines fonctionnalités spécifiques à l’utilisation des sélections.</span><span class="sxs-lookup"><span data-stu-id="b8566-132">The library also exposes the **PlaylistCollection** object (or the **IWMPPlaylistCollection** interface), which provides some functionality specific to working with playlists.</span></span> <span data-ttu-id="b8566-133">La plupart du temps, l’objet **MediaCollection** vous fournit les fonctionnalités dont vous avez besoin, même lorsque vous travaillez avec des sélections.</span><span class="sxs-lookup"><span data-stu-id="b8566-133">Most of the time, the **MediaCollection** object will provide you with the functionality you need, even when working with playlists.</span></span> <span data-ttu-id="b8566-134">Pour plus d’informations sur l’utilisation des éléments multimédias, consultez [gestion des éléments multimédias](managing-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="b8566-134">For more information about working with media items, see [Managing Media Items](managing-media-items.md).</span></span> <span data-ttu-id="b8566-135">Pour plus d’informations sur l’utilisation des sélections, consultez [gestion des sélections](managing-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="b8566-135">For more information about working with playlists, see [Managing Playlists](managing-playlists.md).</span></span>

## <a name="adding-media-items-to-the-library"></a><span data-ttu-id="b8566-136">Ajout d’éléments multimédias à la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8566-136">Adding Media Items to the Library</span></span>

<span data-ttu-id="b8566-137">L’ajout de contenu multimédia numérique à la bibliothèque est simple.</span><span class="sxs-lookup"><span data-stu-id="b8566-137">Adding digital media content to the library is straightforward.</span></span> <span data-ttu-id="b8566-138">Appelez simplement la méthode [MediaCollection. Add](mediacollection-add.md) , en fournissant le chemin d’accès au fichier multimédia en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="b8566-138">Simply call the [MediaCollection.add](mediacollection-add.md) method, providing the path to the media file as an argument.</span></span>

## <a name="retrieving-media-items-from-the-library"></a><span data-ttu-id="b8566-139">Récupération d’éléments multimédias à partir de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8566-139">Retrieving Media Items from the Library</span></span>

<span data-ttu-id="b8566-140">Lorsque vous récupérez des éléments multimédias à partir de la bibliothèque, ce que vous récupérez vraiment est une sélection.</span><span class="sxs-lookup"><span data-stu-id="b8566-140">When you retrieve media items from the library, what you really retrieve is a playlist.</span></span> <span data-ttu-id="b8566-141">Même si vous envisagez de récupérer un seul élément multimédia, vous obtiendrez un objet de **sélection** contenant un seul élément, qui sera associé à l’index zéro.</span><span class="sxs-lookup"><span data-stu-id="b8566-141">Even if you expect to retrieve only one media item, you will get a **Playlist** object containing a single item, which will be associated with index zero.</span></span> <span data-ttu-id="b8566-142">Par exemple, si vous souhaitez récupérer un objet **multimédia** qui représente la chanson nommée « Jeanne », vous pouvez utiliser le code JScript suivant :</span><span class="sxs-lookup"><span data-stu-id="b8566-142">For example, if you want to retrieve a **Media** object that represents the song named "Jeanne", you could use the following JScript code:</span></span>


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



<span data-ttu-id="b8566-143">Le code précédent récupère une sélection contenant tous les éléments multimédias portant le nom « Jeanne » comme titre.</span><span class="sxs-lookup"><span data-stu-id="b8566-143">The preceding code retrieves a playlist containing all the media items having the name "Jeanne" as the title.</span></span> <span data-ttu-id="b8566-144">Pour cet exemple, supposons que vous savez qu’il n’existe qu’une seule chanson par ce nom dans la bibliothèque (Notez que la bibliothèque prend en charge plusieurs chansons portant le même nom).</span><span class="sxs-lookup"><span data-stu-id="b8566-144">For this example, assume that you know there is only one song by that name in the library (note that the library supports multiple songs having the same name).</span></span> <span data-ttu-id="b8566-145">Cela signifie que vous pouvez vous attendre à ce que le nombre d’éléments dans la sélection que vous avez récupéré soit égal à un et que l’élément multimédia soit représenté par l’index zéro.</span><span class="sxs-lookup"><span data-stu-id="b8566-145">This means you could expect the count of items in the playlist you retrieved to equal one and the media item would be represented by index zero.</span></span> <span data-ttu-id="b8566-146">L’exemple de code suivant poursuit l’exemple précédent pour illustrer la façon dont vous récupérez l’élément multimédia à partir de la sélection à l’aide de la méthode [playlist. Item](playlist-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b8566-146">The following example code continues the previous example to demonstrate how you would retrieve the media item from the playlist by using the [Playlist.item](playlist-item.md) method.</span></span>


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



<span data-ttu-id="b8566-147">Pour plus d’informations sur la récupération d’éléments multimédias à partir de sélections, consultez [sélections et éléments multimédias](playlists-and-media-items.md) dans le [Guide de contrôle du lecteur](player-control-guide.md).</span><span class="sxs-lookup"><span data-stu-id="b8566-147">For more information about retrieving media items from playlists, see [Playlists and Media Items](playlists-and-media-items.md) in the [Player Control Guide](player-control-guide.md).</span></span>

## <a name="retrieving-metadata-from-a-media-item"></a><span data-ttu-id="b8566-148">Récupération de métadonnées d’un élément multimédia</span><span class="sxs-lookup"><span data-stu-id="b8566-148">Retrieving Metadata from a Media Item</span></span>

<span data-ttu-id="b8566-149">Après avoir récupéré un objet **multimédia** , vous pouvez lire les valeurs d’attribut associées au contenu.</span><span class="sxs-lookup"><span data-stu-id="b8566-149">After you retrieve a **Media** object, you can read the attribute values associated with the content.</span></span> <span data-ttu-id="b8566-150">Dans le cas le plus simple, vous souhaiterez simplement connaître une seule valeur, telle que le nom de l’artiste qui a effectué une piste musicale. L’exemple JScript suivant montre comment utiliser la méthode [Media. getItemInfo](media-getiteminfo.md) pour récupérer le nom de l’artiste à partir du média récupéré dans l’exemple précédent :</span><span class="sxs-lookup"><span data-stu-id="b8566-150">In the simplest case, you might simply want to know a single value, such as the name of the artist who performed a music track. The following JScript example shows how to use the [Media.getItemInfo](media-getiteminfo.md) method to retrieve the name of the artist from the media retrieved in the previous example:</span></span>


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



<span data-ttu-id="b8566-151">Un élément multimédia peut avoir de nombreux attributs différents et l’utilisation des métadonnées n’est pas toujours aussi simple que le cas simple indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="b8566-151">A media item can have many different attributes, and working with metadata is not always as straightforward as the simple case shown in the previous example.</span></span> <span data-ttu-id="b8566-152">Par exemple, certains attributs peuvent contenir plusieurs valeurs ou avoir des valeurs dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="b8566-152">For instance, some attributes can contain multiple values or have values in more than one language.</span></span> <span data-ttu-id="b8566-153">Pour plus d’informations sur l’utilisation des métadonnées, consultez [attributs d’élément multimédia](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b8566-153">For more information about working with metadata, see [Media Item Attributes](media-item-attributes.md).</span></span> <span data-ttu-id="b8566-154">Pour plus d’informations sur les différents attributs, leurs significations et la prise en charge des types de fichiers, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b8566-154">For more information about the various attributes, their meanings, and file type support, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="removing-media-items-from-the-library"></a><span data-ttu-id="b8566-155">Suppression d’éléments multimédias de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8566-155">Removing Media Items from the Library</span></span>

<span data-ttu-id="b8566-156">La suppression du contenu multimédia numérique de la bibliothèque est également simple.</span><span class="sxs-lookup"><span data-stu-id="b8566-156">Removing digital media content from the library is also straightforward.</span></span> <span data-ttu-id="b8566-157">Appelez simplement **MediaCollection. Remove**, en fournissant l’objet **multimédia** qui représente l’élément comme premier argument et la valeur **true** comme deuxième argument.</span><span class="sxs-lookup"><span data-stu-id="b8566-157">Simply call **MediaCollection.remove**, providing the **Media** object that represents the item as the first argument and the value **true** as the second.</span></span> <span data-ttu-id="b8566-158">L’exemple JScript suivant supprime le fichier nommé Jeanne (récupéré dans l’exemple précédent) de la bibliothèque :</span><span class="sxs-lookup"><span data-stu-id="b8566-158">The following JScript example removes the file named Jeanne (retrieved in the previous example) from the library:</span></span>


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a><span data-ttu-id="b8566-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8566-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8566-160">**À propos de la bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="b8566-160">**About the Library**</span></span>](about-the-library.md)
</dt> <dt>

[<span data-ttu-id="b8566-161">**À propos des objets MediaCollection et Media**</span><span class="sxs-lookup"><span data-stu-id="b8566-161">**About the MediaCollection and Media Objects**</span></span>](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[<span data-ttu-id="b8566-162">**À propos des objets playlist, PlaylistCollection et PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="b8566-162">**About the Playlist, PlaylistCollection, and PlaylistArray Objects**</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[<span data-ttu-id="b8566-163">**Utilisation de la bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="b8566-163">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




