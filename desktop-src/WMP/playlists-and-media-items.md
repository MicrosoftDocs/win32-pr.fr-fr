---
title: Sélections et éléments multimédias
description: Sélections et éléments multimédias
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Lecteur Windows Media, sélections
- Modèle objet du lecteur Windows Media, sélections
- modèle objet, sélections
- Windows Media Player Mobile, sélections
- Contrôle ActiveX du lecteur Windows Media, sélections
- Contrôle ActiveX mobile du lecteur Windows Media, sélections
- Contrôle ActiveX, sélections
- sélections, éléments multimédias
- sélections de métafichiers, éléments multimédias
- Sélections de métafichiers Windows Media, éléments multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939819"
---
# <a name="playlists-and-media-items"></a><span data-ttu-id="71f48-113">Sélections et éléments multimédias</span><span class="sxs-lookup"><span data-stu-id="71f48-113">Playlists and Media Items</span></span>

<span data-ttu-id="71f48-114">Une sélection est un ensemble d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="71f48-114">A playlist is a set of media items.</span></span> <span data-ttu-id="71f48-115">Un objet **playlist** peut manipuler les objets **multimédia** qui représentent ces éléments.</span><span class="sxs-lookup"><span data-stu-id="71f48-115">A **Playlist** object can manipulate the **Media** objects that represent those items.</span></span>

## <a name="retrieving-media-items"></a><span data-ttu-id="71f48-116">Récupération d’éléments multimédias</span><span class="sxs-lookup"><span data-stu-id="71f48-116">Retrieving Media Items</span></span>

<span data-ttu-id="71f48-117">Pour une sélection existante, vous pouvez lire la *sélection*. propriété **Count** pour déterminer le nombre d’éléments multimédias présents dans la sélection, et vous pouvez obtenir une référence à l’objet **Media** correspondant à un élément spécifique à l’aide de la *sélection*. propriété **Item** .</span><span class="sxs-lookup"><span data-stu-id="71f48-117">For an existing playlist, you can read the *Playlist*.**count** property to determine how many media items are in the playlist, and you can get a reference to the **Media** object corresponding to a specific item using the *Playlist*.**item** property.</span></span>

<span data-ttu-id="71f48-118">L’exemple C# suivant récupère une référence d’objet à un élément multimédia spécifique.</span><span class="sxs-lookup"><span data-stu-id="71f48-118">The following C# example retrieves an object reference to a specific media item.</span></span> <span data-ttu-id="71f48-119">(Tout au long de cette rubrique, la variable *plist* est une référence à un objet **playlist** .)</span><span class="sxs-lookup"><span data-stu-id="71f48-119">(Throughout this topic, the variable *pList* is a reference to a **Playlist** object.)</span></span>


```C++
currMedia = pList.Item(0);

```



<span data-ttu-id="71f48-120">L’exemple C# suivant récupère les noms de tous les éléments multimédias dans une sélection et les place dans une zone de liste nommée lstOutput.</span><span class="sxs-lookup"><span data-stu-id="71f48-120">The following C# example retrieves the names of all the media items in a playlist and puts them in a ListBox named lstOutput.</span></span>


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a><span data-ttu-id="71f48-121">Ajout d’éléments à une sélection</span><span class="sxs-lookup"><span data-stu-id="71f48-121">Adding Items to a Playlist</span></span>

<span data-ttu-id="71f48-122">Vous pouvez ajouter un élément multimédia à la fin d’une sélection ou à une position spécifique dans une sélection, à l’aide de la *sélection*. **appendItem** et *playlist*. méthodes **InsertItem** .</span><span class="sxs-lookup"><span data-stu-id="71f48-122">You can add a media item to the end of a playlist or at a specific position in a playlist, using the *Playlist*.**appendItem** and *Playlist*.**insertItem** methods.</span></span>

<span data-ttu-id="71f48-123">Tout au long de cette rubrique, l’objet **Player** a été défini de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="71f48-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="71f48-124">L’exemple C# suivant illustre les deux techniques en ajoutant l’élément multimédia actuel à une sélection nommée « BluesTest », tout d’abord à la fin, puis au début de la sélection.</span><span class="sxs-lookup"><span data-stu-id="71f48-124">The following C# example demonstrates both techniques by adding the current media item to a playlist named "BluesTest", first at the end and then at the beginning of the playlist.</span></span>


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



<span data-ttu-id="71f48-125">Lorsque vous créez une nouvelle playlist vide à l’aide de *PlaylistCollection*. méthode **newPlaylist** . vous pouvez y ajouter des éléments multimédias en appelant de manière répétée la *sélection*. méthode **appendItem** .</span><span class="sxs-lookup"><span data-stu-id="71f48-125">When you create a new, empty playlist by using the *PlaylistCollection*.**newPlaylist** method, you can add media items to it by repeatedly calling the *Playlist*.**appendItem** method.</span></span>

## <a name="manipulating-media-items-in-a-playlist"></a><span data-ttu-id="71f48-126">Manipulation d’éléments multimédias dans une sélection</span><span class="sxs-lookup"><span data-stu-id="71f48-126">Manipulating Media Items in a Playlist</span></span>

<span data-ttu-id="71f48-127">Vous pouvez modifier la position d’un élément multimédia dans la sélection à l’aide de la *sélection*. méthode **moveItem** .</span><span class="sxs-lookup"><span data-stu-id="71f48-127">You can change the position of a media item in the playlist by using the *Playlist*.**moveItem** method.</span></span> <span data-ttu-id="71f48-128">Vous spécifiez l’élément par son index actuel, puis vous spécifiez le nouvel index.</span><span class="sxs-lookup"><span data-stu-id="71f48-128">You specify the item by its current index, and then you specify the new index.</span></span> <span data-ttu-id="71f48-129">L’exemple C# suivant déplace un élément de l’index 5 vers l’index 0 dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="71f48-129">The following C# example moves an item from index 5 to index 0 within a playlist.</span></span>


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



<span data-ttu-id="71f48-130">Vous pouvez supprimer un élément multimédia de la sélection à l’aide de la **sélection**. méthode **RemoveItem** .</span><span class="sxs-lookup"><span data-stu-id="71f48-130">You can remove a media item from the playlist by using the **Playlist**.**removeItem** method.</span></span> <span data-ttu-id="71f48-131">Notez que si l’élément supprimé n’était pas le dernier élément de la sélection, les valeurs d’index des éléments suivants changent.</span><span class="sxs-lookup"><span data-stu-id="71f48-131">Note that if the removed item was not the final item in the playlist, the index values of the subsequent items change.</span></span> <span data-ttu-id="71f48-132">L’exemple C# suivant supprime l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="71f48-132">The following C# example removes the specified item.</span></span>


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> <span data-ttu-id="71f48-133">Les utilisateurs peuvent modifier le contenu d’une sélection en dehors de votre application.</span><span class="sxs-lookup"><span data-stu-id="71f48-133">Users can change the contents of a playlist outside of your application.</span></span> <span data-ttu-id="71f48-134">Chaque fois que vous manipulez les éléments d’une sélection, vous devez surveiller et gérer les événements liés aux playlists du contrôle du lecteur Windows Media pour vous assurer que votre code fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="71f48-134">Whenever you manipulate the items in a playlist, you should monitor and handle the playlist-related events of the Windows Media Player control to ensure that your code works correctly.</span></span> <span data-ttu-id="71f48-135">Ces événements sont *Player*. **CurrentPlaylistChange** et *Player*. **PlaylistChange**.</span><span class="sxs-lookup"><span data-stu-id="71f48-135">These events are *Player*.**CurrentPlaylistChange** and *Player*.**PlaylistChange**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="71f48-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71f48-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71f48-137">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="71f48-137">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="71f48-138">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="71f48-138">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="71f48-139">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="71f48-139">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




