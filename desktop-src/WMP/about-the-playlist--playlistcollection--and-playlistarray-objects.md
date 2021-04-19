---
title: À propos des objets playlist, PlaylistCollection et PlaylistArray
description: À propos des objets playlist, PlaylistCollection et PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Lecteur Windows Media, objet playlist
- Modèle objet du lecteur Windows Media, objet playlist
- modèle objet, objet playlist
- Contrôle ActiveX du lecteur Windows Media, objet playlist
- Contrôle ActiveX, objet playlist
- Contrôle ActiveX Windows Media Player Mobile, objet playlist
- Windows Media Player Mobile, objet playlist
- Objet playlist
- Lecteur Windows Media, objet PlaylistCollection
- Modèle objet du lecteur Windows Media, objet PlaylistCollection
- modèle objet, objet PlaylistCollection
- Contrôle ActiveX du lecteur Windows Media, objet PlaylistCollection
- Contrôle ActiveX, objet PlaylistCollection
- Contrôle ActiveX Windows Media Player Mobile, objet PlaylistCollection
- Windows Media Player Mobile, objet PlaylistCollection
- Objet PlaylistCollection
- Lecteur Windows Media, objet PlaylistArray
- Modèle objet du lecteur Windows Media, objet PlaylistArray
- modèle objet, objet PlaylistArray
- Contrôle ActiveX du lecteur Windows Media, objet PlaylistArray
- Contrôle ActiveX, objet PlaylistArray
- Contrôle ActiveX Windows Media Player Mobile, objet PlaylistArray
- Windows Media Player Mobile, objet PlaylistArray
- Objet PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509797"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a><span data-ttu-id="40cab-127">À propos des objets playlist, PlaylistCollection et PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="40cab-127">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>

<span data-ttu-id="40cab-128">Les objets **playlist**, **PlaylistCollection** et **PlaylistArray** régissent les sélections que le lecteur Windows Media peut utiliser pour spécifier l’ordre dans lequel le contenu est lu.</span><span class="sxs-lookup"><span data-stu-id="40cab-128">The **Playlist**, **PlaylistCollection**, and **PlaylistArray** objects govern the playlists that Windows Media Player can use to specify the order in which content will be played.</span></span> <span data-ttu-id="40cab-129">Vous récupérez l’objet **PlaylistCollection** à partir de la propriété **PlaylistCollection** de l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="40cab-129">You get the **PlaylistCollection** object from the **playlistCollection** property of the **Player** object.</span></span> <span data-ttu-id="40cab-130">La propriété **playlistCollection** retourne l’objet **playlistCollection** .</span><span class="sxs-lookup"><span data-stu-id="40cab-130">The **playlistCollection** property returns the **PlaylistCollection** object.</span></span> <span data-ttu-id="40cab-131">Vous pouvez uniquement accéder aux propriétés de l’objet **PlaylistCollection** après l’avoir créé.</span><span class="sxs-lookup"><span data-stu-id="40cab-131">You can only access the properties of the **PlaylistCollection** object after you have created it.</span></span> <span data-ttu-id="40cab-132">Par exemple, pour créer une nouvelle sélection, vous devez d’abord obtenir l’objet **PlaylistCollection** , puis utiliser une méthode sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="40cab-132">For example, to create a new playlist, you must first get the **PlaylistCollection** object and then use a method on that object.</span></span>


```C++
player.playlistcollection.newplaylist('myplaylist');
```



<span data-ttu-id="40cab-133">Vous pouvez récupérer la sélection en cours à l’aide de la propriété **currentPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="40cab-133">You can get the current playlist by using the **currentPlaylist** property.</span></span> <span data-ttu-id="40cab-134">Par exemple, pour obtenir le nom de la sélection actuelle, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="40cab-134">For example, to get the name of the current playlist, use the following code:</span></span>


```C++
myname = player.currentplaylist.name;
```



<span data-ttu-id="40cab-135">L’objet **PlaylistArray** est retourné par les méthodes **GetAll** et **GetByName** de l’objet **PlaylistCollection** .</span><span class="sxs-lookup"><span data-stu-id="40cab-135">The **PlaylistArray** object is returned by the **getAll** and **getByName** methods of the **PlaylistCollection** object.</span></span> <span data-ttu-id="40cab-136">Pour obtenir le nombre de sélections, par exemple, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="40cab-136">To get the number of playlists, for example, use the following code:</span></span>


```C++
howmany = player.playlistcollection.getAll().count;
```



<span data-ttu-id="40cab-137">Pour récupérer une sélection connue par son nom, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="40cab-137">To retrieve a known playlist by name, use the following code:</span></span>


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="40cab-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40cab-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40cab-139">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="40cab-139">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="40cab-140">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="40cab-140">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="40cab-141">**Objet PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="40cab-141">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="40cab-142">**Objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="40cab-142">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 




