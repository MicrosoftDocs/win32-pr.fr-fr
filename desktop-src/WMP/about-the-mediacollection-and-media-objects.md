---
title: À propos des objets MediaCollection et Media
description: À propos des objets MediaCollection et Media
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Lecteur Windows Media, objet MediaCollection
- Modèle objet du lecteur Windows Media, objet MediaCollection
- modèle objet, objet MediaCollection
- Contrôle ActiveX du lecteur Windows Media, objet MediaCollection
- Contrôle ActiveX, objet MediaCollection
- Contrôle ActiveX Windows Media Player Mobile, objet MediaCollection
- Windows Media Player Mobile, objet MediaCollection
- Objet MediaCollection
- Lecteur Windows Media, objet multimédia
- Windows Media Player Object Model, Media Object
- modèle objet, objet Media
- Contrôle ActiveX du lecteur Windows Media, objet multimédia
- Contrôle ActiveX, objet multimédia
- Windows Media Player Mobile contrôle ActiveX, objet multimédia
- Windows Media Player Mobile, objet multimédia
- Objet Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510016"
---
# <a name="about-the-mediacollection-and-media-objects"></a><span data-ttu-id="0c080-119">À propos des objets MediaCollection et Media</span><span class="sxs-lookup"><span data-stu-id="0c080-119">About the MediaCollection and Media Objects</span></span>

<span data-ttu-id="0c080-120">Les objets **MediaCollection** et **Media** gouvernent la collection de supports, qui définit l’emplacement des fichiers multimédias numériques auxquels le lecteur Windows Media peut accéder.</span><span class="sxs-lookup"><span data-stu-id="0c080-120">The **MediaCollection** and **Media** objects govern the media collection, which defines the locations of digital media files that Windows Media Player can access.</span></span> <span data-ttu-id="0c080-121">Vous récupérez l’objet **MediaCollection** à partir de la propriété **MediaCollection** de l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="0c080-121">You get the **MediaCollection** object from the **mediaCollection** property of the **Player** object.</span></span> <span data-ttu-id="0c080-122">La propriété **mediaCollection** retourne l’objet **mediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="0c080-122">The **mediaCollection** property returns the **MediaCollection** object.</span></span> <span data-ttu-id="0c080-123">Vous pouvez uniquement accéder aux propriétés de l’objet **MediaCollection** après l’avoir créé.</span><span class="sxs-lookup"><span data-stu-id="0c080-123">You can only access the properties of the **MediaCollection** object after you have created it.</span></span> <span data-ttu-id="0c080-124">Par exemple, pour ajouter un objet **multimédia** (une chanson), utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="0c080-124">For example, to add a **Media** object (a song), use the following code:</span></span>


```C++
player.mediacollection.add('laure.wma');

```



<span data-ttu-id="0c080-125">Vous avez ajouté le fichier Laure. WMA à la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="0c080-125">You have added the file laure.wma to the media collection.</span></span>

<span data-ttu-id="0c080-126">Vous pouvez récupérer l’objet **multimédia** en cours à l’aide de la propriété **currentMedia** du **lecteur**.</span><span class="sxs-lookup"><span data-stu-id="0c080-126">You can get the current **Media** object by using the **currentMedia** property of the **Player**.</span></span> <span data-ttu-id="0c080-127">Par exemple, ce code obtient la propriété **Duration** de l’objet **média** actuel :</span><span class="sxs-lookup"><span data-stu-id="0c080-127">For example, this code gets the **duration** property of the current **Media** object:</span></span>


```C++
myduration = player.currentmedia.duration;

```



<span data-ttu-id="0c080-128">Il existe de nombreuses façons d’obtenir un objet **multimédia** afin de pouvoir accéder à ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="0c080-128">There are many ways to get a **Media** object so that you can access its properties.</span></span> <span data-ttu-id="0c080-129">Par exemple, si vous souhaitez accéder à la propriété **Duration** du média actuel, chacune des lignes de code suivantes peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="0c080-129">For example, if you want to access the **duration** property of the current media, each of the following lines of code could be used.</span></span>

<span data-ttu-id="0c080-130">Pour connaître la durée du média en cours de diffusion :</span><span class="sxs-lookup"><span data-stu-id="0c080-130">To get the duration of the currently playing media:</span></span>


```C++
player.currentMedia.duration;

```



<span data-ttu-id="0c080-131">Pour obtenir la durée du média actuel dans une sélection :</span><span class="sxs-lookup"><span data-stu-id="0c080-131">To get the duration of the current media in a playlist:</span></span>


```C++
player.controls.currentItem.duration;

```



<span data-ttu-id="0c080-132">Pour obtenir la durée du troisième élément multimédia dans une sélection :</span><span class="sxs-lookup"><span data-stu-id="0c080-132">To get the duration of the third media item in a playlist:</span></span>


```C++
player.currentPlaylist.item(2).duration;

```



<span data-ttu-id="0c080-133">Pour obtenir la durée du troisième élément multimédia dans un genre « jazz » :</span><span class="sxs-lookup"><span data-stu-id="0c080-133">To get the duration of the third media item in a "Jazz" genre:</span></span>


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



<span data-ttu-id="0c080-134">Pour connaître la durée du troisième élément multimédia de la deuxième sélection :</span><span class="sxs-lookup"><span data-stu-id="0c080-134">To get the duration of the third media item in the second playlist:</span></span>


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a><span data-ttu-id="0c080-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c080-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c080-136">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="0c080-136">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="0c080-137">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="0c080-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="0c080-138">**Modèle objet de lecteur pour les langages de script**</span><span class="sxs-lookup"><span data-stu-id="0c080-138">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




