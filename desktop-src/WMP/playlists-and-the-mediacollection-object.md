---
title: Sélections et objet MediaCollection
description: Sélections et objet MediaCollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Lecteur Windows Media, sélections
- Modèle objet du lecteur Windows Media, sélections
- modèle objet, sélections
- Windows Media Player Mobile, sélections
- Contrôle ActiveX du lecteur Windows Media, sélections
- Contrôle ActiveX mobile du lecteur Windows Media, sélections
- Contrôle ActiveX, sélections
- sélections, objet MediaCollection
- sélections de métafichiers, objet MediaCollection
- Sélections de métafichiers Windows Media, objet MediaCollection
- Objet MediaCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379781"
---
# <a name="playlists-and-the-mediacollection-object"></a><span data-ttu-id="30bed-114">Sélections et objet MediaCollection</span><span class="sxs-lookup"><span data-stu-id="30bed-114">Playlists and the MediaCollection Object</span></span>

<span data-ttu-id="30bed-115">L’objet **MediaCollection** vous donne accès à diverses sélections spéciales et inclut une méthode pour créer une nouvelle sélection à partir d’un métafichier.</span><span class="sxs-lookup"><span data-stu-id="30bed-115">The **MediaCollection** object gives you access to a variety of special playlists, and includes a method for creating a new playlist from a metafile.</span></span>

<span data-ttu-id="30bed-116">Les méthodes suivantes récupèrent des sélections spéciales :</span><span class="sxs-lookup"><span data-stu-id="30bed-116">The following methods retrieve special playlists:</span></span>

-   <span data-ttu-id="30bed-117">**getAll**</span><span class="sxs-lookup"><span data-stu-id="30bed-117">**getAll**</span></span>
-   <span data-ttu-id="30bed-118">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="30bed-118">**getByAlbum**</span></span>
-   <span data-ttu-id="30bed-119">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="30bed-119">**getByAttribute**</span></span>
-   <span data-ttu-id="30bed-120">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="30bed-120">**getByAuthor**</span></span>
-   <span data-ttu-id="30bed-121">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="30bed-121">**getByGenre**</span></span>
-   <span data-ttu-id="30bed-122">**getByName**</span><span class="sxs-lookup"><span data-stu-id="30bed-122">**getByName**</span></span>

<span data-ttu-id="30bed-123">Comme leur nom le suggère, ces méthodes récupèrent les sélections contenant tous les éléments multimédias de la bibliothèque qui correspondent à certains critères.</span><span class="sxs-lookup"><span data-stu-id="30bed-123">As their names suggest, these methods retrieve playlists containing all of the media items in the library that match certain criteria.</span></span>

<span data-ttu-id="30bed-124">Veillez à ne pas confondre le *MediaCollection*. méthode **GetByName** avec *PlaylistCollection*. méthode **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="30bed-124">Be careful not to confuse the *MediaCollection*.**getByName** method with the *PlaylistCollection*.**getByName** method.</span></span> <span data-ttu-id="30bed-125">La méthode **MediaCollection** retourne un objet **playlist** contenant tous les éléments multimédias portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="30bed-125">The **MediaCollection** method returns a **Playlist** object containing all of the media items that have the specified name.</span></span> <span data-ttu-id="30bed-126">La méthode **PlaylistCollection** retourne un objet **PlaylistArray** contenant toutes les sélections portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="30bed-126">The **PlaylistCollection** method returns a **PlaylistArray** object containing all of the playlists that have the specified name.</span></span>

<span data-ttu-id="30bed-127">Vous pouvez utiliser *MediaCollection*. **Ajoutez** une méthode pour ajouter des sélections ainsi que des éléments multimédias à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="30bed-127">You can use the *MediaCollection*.**add** method to add playlists as well as media items to the library.</span></span> <span data-ttu-id="30bed-128">Pour ajouter une sélection, vous transmettez à la méthode le chemin d’accès au métafichier qui définit la sélection.</span><span class="sxs-lookup"><span data-stu-id="30bed-128">To add a playlist, you pass the method the path to the metafile that defines the playlist.</span></span> <span data-ttu-id="30bed-129">La méthode retourne toujours un objet **Media** .</span><span class="sxs-lookup"><span data-stu-id="30bed-129">The method always returns a **Media** object.</span></span> <span data-ttu-id="30bed-130">Vous ne pouvez pas effectuer un cast entre des objets de **média** et de **sélection** .</span><span class="sxs-lookup"><span data-stu-id="30bed-130">You cannot cast between **Media** and **Playlist** objects.</span></span> <span data-ttu-id="30bed-131">Pour utiliser la sélection que vous avez ajoutée, récupérez l’objet de **sélection** portant le même nom que l’objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="30bed-131">To work with the playlist that you added, retrieve the **Playlist** object that has the same name as the **Media** object.</span></span>

<span data-ttu-id="30bed-132">L’exemple C# suivant montre comment récupérer des médias par type à l’aide de **MediaCollection**. méthode **getByAttribute** .</span><span class="sxs-lookup"><span data-stu-id="30bed-132">The following C# example demonstrates how to retrieve media by type using the **MediaCollection**.**getByAttribute** method.</span></span> <span data-ttu-id="30bed-133">Ce code récupère les noms de tous les attributs associés à un type donné, ainsi que l’État en lecture/écriture ou en lecture seule de ces attributs.</span><span class="sxs-lookup"><span data-stu-id="30bed-133">This code retrieves the names of all attributes associated with a given type as well as the read/write or read-only status of those attributes.</span></span> <span data-ttu-id="30bed-134">Il génère un fichier unique qui contient des listes d’attributs pour les types audio, vidéo, radio, sélection, autre, musique et photo.</span><span class="sxs-lookup"><span data-stu-id="30bed-134">It generates a single file that contains lists of attributes for the Audio, Video, Radio, Playlist, Other, Music, and Photo types.</span></span>


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



<span data-ttu-id="30bed-135">L’exemple C# suivant montre comment ajouter une sélection d’un métafichier à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="30bed-135">The following C# example demonstrates how to add a playlist from a metafile to the library.</span></span>


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



<span data-ttu-id="30bed-136">Les sélections statiques incluent des éléments multimédias spécifiques.</span><span class="sxs-lookup"><span data-stu-id="30bed-136">Static playlists include specific media items.</span></span> <span data-ttu-id="30bed-137">Les sélections automatiques recherchent la bibliothèque à chaque fois qu’elles sont ouvertes et peuvent contenir différents éléments multimédias à des moments différents.</span><span class="sxs-lookup"><span data-stu-id="30bed-137">Auto playlists search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="30bed-138">Vous pouvez ajouter des sélections statiques et automatiques à la bibliothèque à l’aide de *MediaCollection*. **Ajouter** une méthode.</span><span class="sxs-lookup"><span data-stu-id="30bed-138">You can add both static and auto playlists to the library by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="30bed-139">Vous pouvez également ajouter des sélections statiques à l’aide de *PlaylistCollection*. méthode **importPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="30bed-139">You can also add static playlists by using the *PlaylistCollection*.**importPlaylist** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30bed-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30bed-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30bed-141">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="30bed-141">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="30bed-142">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="30bed-142">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="30bed-143">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="30bed-143">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="30bed-144">**Objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="30bed-144">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="30bed-145">**Sélections et objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="30bed-145">**Playlists and the PlaylistCollection Object**</span></span>](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="30bed-146">**Sélections statiques et automatiques**</span><span class="sxs-lookup"><span data-stu-id="30bed-146">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> </dl>

 

 




