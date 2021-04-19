---
title: Sélections et objet PlaylistCollection
description: Sélections et objet PlaylistCollection
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Lecteur Windows Media, sélections
- Modèle objet du lecteur Windows Media, sélections
- modèle objet, sélections
- Windows Media Player Mobile, sélections
- Contrôle ActiveX du lecteur Windows Media, sélections
- Contrôle ActiveX mobile du lecteur Windows Media, sélections
- Contrôle ActiveX, sélections
- sélections, objet PlaylistCollection
- sélections de métafichiers, objet PlaylistCollection
- Sélections de métafichiers Windows Media, objet PlaylistCollection
- Objet PlaylistCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513454"
---
# <a name="playlists-and-the-playlistcollection-object"></a><span data-ttu-id="fb2dd-114">Sélections et objet PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="fb2dd-114">Playlists and the PlaylistCollection Object</span></span>

<span data-ttu-id="fb2dd-115">L’objet **PlaylistCollection** vous donne accès aux sélections de la bibliothèque et contient des méthodes permettant de créer de nouvelles playlists vides et de nouvelles sélections à partir des fichiers de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-115">The **PlaylistCollection** object gives you access to playlists in the library and has methods for creating new, empty playlists and new playlists from metafiles.</span></span>

## <a name="working-with-existing-playlists"></a><span data-ttu-id="fb2dd-116">Utilisation des sélections existantes</span><span class="sxs-lookup"><span data-stu-id="fb2dd-116">Working with Existing Playlists</span></span>

<span data-ttu-id="fb2dd-117">*PlaylistCollection*. **GetAll** et *PlaylistCollection*. les méthodes **GetByName** retournent chacune un objet **PlaylistArray** , qui peut contenir plusieurs sélections.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-117">The *PlaylistCollection*.**getAll** and *PlaylistCollection*.**getByName** methods each return a **PlaylistArray** object, which can contain multiple playlists.</span></span>

<span data-ttu-id="fb2dd-118">*PlaylistCollection*. la méthode **GetAll** retourne toutes les playlists existantes qui se trouvent dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-118">The *PlaylistCollection*.**getAll** method returns all of the existing playlists that are in the library.</span></span> <span data-ttu-id="fb2dd-119">Par exemple, vous pouvez appeler cette méthode, puis récupérer les sélections dans l’objet **PlaylistArray** pour déterminer si un nom de playlist donné a déjà été utilisé, ou pour afficher toutes les playlists de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-119">For example, you can call this method and then retrieve the playlists in the **PlaylistArray** object to determine whether a given playlist name has already been used, or to display all of the playlists to the user.</span></span> <span data-ttu-id="fb2dd-120">L’exemple de code dans les [attributs de sélection](playlist-attributes.md) utilise la méthode **GetAll** .</span><span class="sxs-lookup"><span data-stu-id="fb2dd-120">The sample code in [Playlist Attributes](playlist-attributes.md) uses the **getAll** method.</span></span>

<span data-ttu-id="fb2dd-121">*PlaylistCollection*. la méthode **GetByName** retourne toutes les sélections avec un nom donné.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-121">The *PlaylistCollection*.**getByName** method returns all of the playlists with a given name.</span></span> <span data-ttu-id="fb2dd-122">Vous pouvez utiliser cette méthode pour gérer chacune de ces sélections séparément.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-122">You can use this method to handle each of those playlists separately.</span></span>

<span data-ttu-id="fb2dd-123">Vous pouvez également utiliser la méthode **GetByName** pour récupérer une sélection unique par nom.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-123">You can also use the **getByName** method to retrieve a unique playlist by name.</span></span> <span data-ttu-id="fb2dd-124">Dans ce cas, l’objet **PlaylistArray** n’a qu’un seul élément.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-124">In that case, the **PlaylistArray** object has only one element.</span></span> <span data-ttu-id="fb2dd-125">L’exemple C# suivant illustre cette technique.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-125">The following C# example demonstrates this technique.</span></span>


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a><span data-ttu-id="fb2dd-126">Utilisation de nouvelles sélections</span><span class="sxs-lookup"><span data-stu-id="fb2dd-126">Working with New Playlists</span></span>

<span data-ttu-id="fb2dd-127">Vous pouvez utiliser *PlaylistCollection*. méthode **newPlaylist** pour créer une nouvelle playlist vide.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-127">You can use the *PlaylistCollection*.**newPlaylist** method to create a new, empty playlist.</span></span> <span data-ttu-id="fb2dd-128">La méthode retourne une référence au nouvel objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="fb2dd-128">The method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="fb2dd-129">Vous pouvez ensuite appeler la *sélection*. méthode **appendItem** pour ajouter des éléments multimédias à la sélection.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-129">You can then call the *Playlist*.**appendItem** method to add media items to the playlist.</span></span>

<span data-ttu-id="fb2dd-130">Vous pouvez également créer une nouvelle sélection basée sur un métafichier de sélection.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-130">You can also create a new playlist based on a playlist metafile.</span></span> <span data-ttu-id="fb2dd-131">Tout d’abord, transmettez le nom de la sélection et le chemin d’accès au métafichier au *joueur*. méthode **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="fb2dd-131">First, pass the name of the playlist and the path to the metafile to the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="fb2dd-132">Cette méthode retourne une référence au nouvel objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="fb2dd-132">That method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="fb2dd-133">Ensuite, transmettez le nouvel objet **playlist** à *PlaylistCollection*. méthode **importPlaylist** pour l’ajouter à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-133">Then, pass the new **Playlist** object to the *PlaylistCollection*.**importPlaylist** method to add it to the library.</span></span>

<span data-ttu-id="fb2dd-134">Notez la différence entre les *PlaylistCollection*. méthode **newPlaylist** et *Player*. méthode **newPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="fb2dd-134">Notice the difference between the *PlaylistCollection*.**newPlaylist** method and the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="fb2dd-135">La méthode **PlaylistCollection** crée une nouvelle playlist vide et l’ajoute à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-135">The **PlaylistCollection** method creates a new, empty playlist and adds it to the library.</span></span> <span data-ttu-id="fb2dd-136">La méthode **Player** crée un nouvel objet de **sélection** rempli, mais ne l’ajoute pas à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-136">The **Player** method creates a new, populated **Playlist** object but does not add it to the library.</span></span>

<span data-ttu-id="fb2dd-137">Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="fb2dd-137">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="fb2dd-138">L’exemple C# suivant illustre l’importation d’une sélection à partir d’un métafichier.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-138">The following C# example demonstrates importing a playlist from a metafile.</span></span> <span data-ttu-id="fb2dd-139">L’argument *strPListName* spécifie le nom de la nouvelle sélection.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-139">The *strPListName* argument specifies the name of the new playlist.</span></span> <span data-ttu-id="fb2dd-140">*StrMetaFileName* spécifie le nom du métafichier à partir duquel la sélection est importée.</span><span class="sxs-lookup"><span data-stu-id="fb2dd-140">The *strMetaFileName* specifies the name of the metafile from which the playlist is imported.</span></span>


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a><span data-ttu-id="fb2dd-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb2dd-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb2dd-142">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="fb2dd-142">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="fb2dd-143">**Player. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="fb2dd-143">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="fb2dd-144">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="fb2dd-144">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="fb2dd-145">**Objet PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="fb2dd-145">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="fb2dd-146">**Objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="fb2dd-146">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="fb2dd-147">**Sélections et éléments multimédias**</span><span class="sxs-lookup"><span data-stu-id="fb2dd-147">**Playlists and Media Items**</span></span>](playlists-and-media-items.md)
</dt> </dl>

 

 




