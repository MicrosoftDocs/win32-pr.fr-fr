---
title: Objet playlist
description: L’objet playlist offre un moyen d’organiser les éléments multimédias dans une liste pour faciliter leur manipulation à l’aide des propriétés et méthodes suivantes.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Objet playlist lecteur Windows Media
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030010"
---
# <a name="playlist-object"></a><span data-ttu-id="c5666-104">Objet playlist</span><span class="sxs-lookup"><span data-stu-id="c5666-104">Playlist Object</span></span>

<span data-ttu-id="c5666-105">L’objet **playlist** offre un moyen d’organiser les éléments multimédias dans une liste pour faciliter leur manipulation à l’aide des propriétés et méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5666-105">The **Playlist** object provides a way to organize media items in a list for easy manipulation by using the following properties and methods.</span></span>

<span data-ttu-id="c5666-106">L’objet **playlist** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5666-106">The **Playlist** object supports the following properties.</span></span>



| <span data-ttu-id="c5666-107">Propriété</span><span class="sxs-lookup"><span data-stu-id="c5666-107">Property</span></span>                                      | <span data-ttu-id="c5666-108">Description</span><span class="sxs-lookup"><span data-stu-id="c5666-108">Description</span></span>                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="c5666-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="c5666-109">attributeCount</span></span>](playlist-attributecount.md) | <span data-ttu-id="c5666-110">Récupère le nombre d’attributs associés à la sélection.</span><span class="sxs-lookup"><span data-stu-id="c5666-110">Retrieves the number of attributes associated with the playlist.</span></span> |
| [<span data-ttu-id="c5666-111">attributeName</span><span class="sxs-lookup"><span data-stu-id="c5666-111">attributeName</span></span>](playlist-attributename.md)   | <span data-ttu-id="c5666-112">Récupère le nom d’un attribut spécifié par un index.</span><span class="sxs-lookup"><span data-stu-id="c5666-112">Retrieves the name of an attribute specified by an index.</span></span>        |
| [<span data-ttu-id="c5666-113">count</span><span class="sxs-lookup"><span data-stu-id="c5666-113">count</span></span>](playlist-count.md)                   | <span data-ttu-id="c5666-114">Récupère le nombre d’éléments dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="c5666-114">Retrieves the number of items in the playlist.</span></span>                   |
| [<span data-ttu-id="c5666-115">name</span><span class="sxs-lookup"><span data-stu-id="c5666-115">name</span></span>](playlist-name.md)                     | <span data-ttu-id="c5666-116">Spécifie ou récupère le nom de la sélection.</span><span class="sxs-lookup"><span data-stu-id="c5666-116">Specifies or retrieves the name of the playlist.</span></span>                 |



 

<span data-ttu-id="c5666-117">L’objet **playlist** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5666-117">The **Playlist** object supports the following methods.</span></span>



| <span data-ttu-id="c5666-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="c5666-118">Method</span></span>                                  | <span data-ttu-id="c5666-119">Description</span><span class="sxs-lookup"><span data-stu-id="c5666-119">Description</span></span>                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5666-120">appendItem</span><span class="sxs-lookup"><span data-stu-id="c5666-120">appendItem</span></span>](playlist-appenditem.md)   | <span data-ttu-id="c5666-121">Ajoute un élément multimédia à la fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="c5666-121">Adds a media item to the end of the playlist.</span></span>                                                          |
| <span data-ttu-id="c5666-122">**clear**</span><span class="sxs-lookup"><span data-stu-id="c5666-122">**clear**</span></span>                               | <span data-ttu-id="c5666-123">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="c5666-123">Reserved for future use.</span></span>                                                                               |
| [<span data-ttu-id="c5666-124">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="c5666-124">getItemInfo</span></span>](playlist-getiteminfo.md) | <span data-ttu-id="c5666-125">Récupère la valeur d’un attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="c5666-125">Retrieves the value of a playlist attribute.</span></span>                                                           |
| [<span data-ttu-id="c5666-126">insertItem</span><span class="sxs-lookup"><span data-stu-id="c5666-126">insertItem</span></span>](playlist-insertitem.md)   | <span data-ttu-id="c5666-127">Insère un élément multimédia dans la sélection à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="c5666-127">Inserts a media item into the playlist at the specified location.</span></span>                                      |
| [<span data-ttu-id="c5666-128">isIdentical</span><span class="sxs-lookup"><span data-stu-id="c5666-128">isIdentical</span></span>](playlist-isidentical.md) | <span data-ttu-id="c5666-129">Récupère une valeur indiquant si l’objet de **sélection** fourni est identique à l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="c5666-129">Retrieves a value indicating whether the supplied **Playlist** object is identical to the current one.</span></span> |
| [<span data-ttu-id="c5666-130">item</span><span class="sxs-lookup"><span data-stu-id="c5666-130">item</span></span>](playlist-item.md)               | <span data-ttu-id="c5666-131">Récupère l’élément multimédia à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="c5666-131">Retrieves the media item at the specified index.</span></span>                                                       |
| [<span data-ttu-id="c5666-132">moveItem</span><span class="sxs-lookup"><span data-stu-id="c5666-132">moveItem</span></span>](playlist-moveitem.md)       | <span data-ttu-id="c5666-133">Modifie l’emplacement d’un élément dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="c5666-133">Changes the location of an item in the playlist.</span></span>                                                       |
| [<span data-ttu-id="c5666-134">removeItem</span><span class="sxs-lookup"><span data-stu-id="c5666-134">removeItem</span></span>](playlist-removeitem.md)   | <span data-ttu-id="c5666-135">Supprime l’élément spécifié de la sélection.</span><span class="sxs-lookup"><span data-stu-id="c5666-135">Removes the specified item from the playlist.</span></span>                                                          |
| [<span data-ttu-id="c5666-136">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="c5666-136">setItemInfo</span></span>](playlist-setiteminfo.md) | <span data-ttu-id="c5666-137">Spécifie la valeur d’un attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="c5666-137">Specifies the value of a playlist attribute.</span></span>                                                           |



 

<span data-ttu-id="c5666-138">L’objet **playlist** est accessible par le biais des propriétés et méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5666-138">The **Playlist** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="c5666-139">Object</span><span class="sxs-lookup"><span data-stu-id="c5666-139">Object</span></span>                                              | <span data-ttu-id="c5666-140">Propriété ou méthode</span><span class="sxs-lookup"><span data-stu-id="c5666-140">Property or method</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5666-141">-</span><span class="sxs-lookup"><span data-stu-id="c5666-141">Cdrom</span></span>](cdrom-object.md)                           | [<span data-ttu-id="c5666-142">playlist</span><span class="sxs-lookup"><span data-stu-id="c5666-142">playlist</span></span>](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c5666-143">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="c5666-143">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="c5666-144">[GetAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [GetByName](mediacollection-getbyname.md)</span><span class="sxs-lookup"><span data-stu-id="c5666-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span></span> |
| [<span data-ttu-id="c5666-145">Lecteur</span><span class="sxs-lookup"><span data-stu-id="c5666-145">Player</span></span>](player-object.md)                         | <span data-ttu-id="c5666-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="c5666-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="c5666-147">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="c5666-147">PlaylistArray</span></span>](playlistarray-object.md)           | [<span data-ttu-id="c5666-148">item</span><span class="sxs-lookup"><span data-stu-id="c5666-148">item</span></span>](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c5666-149">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="c5666-149">PlaylistCollection</span></span>](playlistcollection-object.md) | [<span data-ttu-id="c5666-150">newPlaylist</span><span class="sxs-lookup"><span data-stu-id="c5666-150">newPlaylist</span></span>](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

<span data-ttu-id="c5666-151">Parce qu’il s’agit de la méthode d’accès la plus courante, *Player*. **currentPlaylist** est utilisé à des fins d’illustration dans les sections de syntaxe de référence.</span><span class="sxs-lookup"><span data-stu-id="c5666-151">Because it is the most common means of access, *player*.**currentPlaylist** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5666-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5666-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5666-153">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="c5666-153">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




