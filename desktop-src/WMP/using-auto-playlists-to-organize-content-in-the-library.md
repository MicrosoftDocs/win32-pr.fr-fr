---
title: Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque
description: Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player Online stores, sélections automatiques
- magasins en ligne, sélections automatiques
- tapez 1 magasins en ligne, sélections automatiques
- tapez 2 magasins en ligne, sélections automatiques
- Windows Media Player Online stores, organiser le contenu de la bibliothèque
- magasins en ligne, organiser le contenu de la bibliothèque
- tapez 1 magasins en ligne, organiser le contenu de la bibliothèque
- tapez 2 magasins en ligne, organiser le contenu de la bibliothèque
- Magasins en ligne du lecteur Windows Media, organisation du contenu de la bibliothèque
- magasins en ligne, organisation du contenu de la bibliothèque
- types 1 magasins en ligne, organisation du contenu de la bibliothèque
- type 2 magasins en ligne, organisation du contenu de la bibliothèque
- bibliothèque, organisation du contenu
- Organisation du contenu de la bibliothèque
- sélections automatiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507299"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a><span data-ttu-id="0c373-118">Utilisation de sélections automatiques pour organiser le contenu de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c373-118">Using Auto Playlists to Organize Content in the Library</span></span>

<span data-ttu-id="0c373-119">Vous pouvez utiliser les sélections automatiques pour organiser le contenu Premium que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="0c373-119">You can use auto playlists to organize premium content you provide.</span></span> <span data-ttu-id="0c373-120">Par exemple, vous pouvez utiliser le lecteur Windows Media pour créer une sélection automatique qui contient uniquement le contenu que vous avez fourni avec un classement utilisateur d’au moins quatre étoiles.</span><span class="sxs-lookup"><span data-stu-id="0c373-120">For example, you could use Windows Media Player to create an auto playlist that contains only content you provided having a user rating of at least four stars.</span></span> <span data-ttu-id="0c373-121">Vous pouvez ensuite ajouter la sélection automatique à la bibliothèque dans le lecteur Windows Media pour qu’elle s’affiche dans le nœud musique achetée sous le nœud serveur de distribution de contenu.</span><span class="sxs-lookup"><span data-stu-id="0c373-121">You can then add the auto playlist to the library in Windows Media Player so that it displays in the Purchased Music node under your content distributor node.</span></span>

<span data-ttu-id="0c373-122">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0c373-122">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="0c373-123">Créez la sélection automatique.</span><span class="sxs-lookup"><span data-stu-id="0c373-123">Create the auto playlist.</span></span>
2.  <span data-ttu-id="0c373-124">À l’aide de l’Explorateur Windows, accédez à la sélection automatique et récupérez le fichier. wpl.</span><span class="sxs-lookup"><span data-stu-id="0c373-124">Using Windows Explorer, browse to the auto playlist and retrieve the .wpl file.</span></span>
3.  <span data-ttu-id="0c373-125">À l’aide du modèle objet du lecteur Windows Media, ajoutez la sélection automatique à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="0c373-125">Using the Windows Media Player object model, add the auto playlist to the library.</span></span>
4.  <span data-ttu-id="0c373-126">Définissez l’attribut **WM/ContentDistributor** pour la sélection sur le nom de votre clé de serveur de distribution de contenu.</span><span class="sxs-lookup"><span data-stu-id="0c373-126">Set the **WM/ContentDistributor** attribute for the playlist to your content distributor key name.</span></span>
5.  <span data-ttu-id="0c373-127">Affectez à l’attribut **SyncOnly** de la playlist la valeur true.</span><span class="sxs-lookup"><span data-stu-id="0c373-127">Set the **SyncOnly** attribute for the playlist to true.</span></span>

<span data-ttu-id="0c373-128">L’exemple de code JScript suivant illustre une fonction qui ajoute une sélection automatique nommée « correspondances favorites » au nœud Proseware dans la bibliothèque :</span><span class="sxs-lookup"><span data-stu-id="0c373-128">The following JScript example code shows a function that adds an auto playlist named "Favorite Hits" to the Proseware node in the library:</span></span>


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a><span data-ttu-id="0c373-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c373-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c373-130">À propos de l’intégration de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c373-130">About Library Integration</span></span>](download-manager-overview.md)
</dt> <dt>

[<span data-ttu-id="0c373-131">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="0c373-131">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="0c373-132">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="0c373-132">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="0c373-133">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="0c373-133">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="0c373-134">**Sélections statiques et automatiques**</span><span class="sxs-lookup"><span data-stu-id="0c373-134">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> <dt>

[<span data-ttu-id="0c373-135">**Attribut SyncOnly**</span><span class="sxs-lookup"><span data-stu-id="0c373-135">**SyncOnly Attribute**</span></span>](synconly-attribute.md)
</dt> <dt>

[<span data-ttu-id="0c373-136">**Attribut WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="0c373-136">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="0c373-137">**Utilisation de la bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="0c373-137">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




