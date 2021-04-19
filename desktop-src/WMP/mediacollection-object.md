---
title: Objet MediaCollection
description: L’objet MediaCollection offre un moyen d’organiser une grande collection d’éléments multimédias. Elle peut être interrogée pour générer automatiquement des sélections.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Objet MediaCollection lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106513503"
---
# <a name="mediacollection-object"></a><span data-ttu-id="93606-105">Objet MediaCollection</span><span class="sxs-lookup"><span data-stu-id="93606-105">MediaCollection Object</span></span>

<span data-ttu-id="93606-106">L’objet **MediaCollection** offre un moyen d’organiser une grande collection d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="93606-106">The **MediaCollection** object provides a way to organize a large collection of media items.</span></span> <span data-ttu-id="93606-107">Elle peut être interrogée pour générer automatiquement des sélections.</span><span class="sxs-lookup"><span data-stu-id="93606-107">It can be queried to generate playlists automatically.</span></span>

<span data-ttu-id="93606-108">L’objet **MediaCollection** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="93606-108">The **MediaCollection** object supports the following methods.</span></span>



| <span data-ttu-id="93606-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="93606-109">Method</span></span>                                                                           | <span data-ttu-id="93606-110">Description</span><span class="sxs-lookup"><span data-stu-id="93606-110">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93606-111">add</span><span class="sxs-lookup"><span data-stu-id="93606-111">add</span></span>](mediacollection-add.md)                                                   | <span data-ttu-id="93606-112">Ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="93606-112">Adds a new media item or playlist to the library.</span></span>                                                                                                              |
| [<span data-ttu-id="93606-113">createQuery</span><span class="sxs-lookup"><span data-stu-id="93606-113">createQuery</span></span>](mediacollection-createquery.md)                                   | <span data-ttu-id="93606-114">Crée un objet de [requête](query-object.md) .</span><span class="sxs-lookup"><span data-stu-id="93606-114">Creates a new [Query](query-object.md) object.</span></span>                                                                                                                |
| [<span data-ttu-id="93606-115">getAll</span><span class="sxs-lookup"><span data-stu-id="93606-115">getAll</span></span>](mediacollection-getall.md)                                             | <span data-ttu-id="93606-116">Récupère un objet [playlist](playlist-object.md) contenant tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="93606-116">Retrieves a [Playlist](playlist-object.md) object containing all media items in the library.</span></span>                                                                  |
| [<span data-ttu-id="93606-117">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="93606-117">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) | <span data-ttu-id="93606-118">Récupère un objet [StringCollection](stringcollection-object.md) représentant l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="93606-118">Retrieves a [StringCollection](stringcollection-object.md) object representing the set of all values for a specified attribute within a specified media type.</span></span> |
| [<span data-ttu-id="93606-119">getByAlbum</span><span class="sxs-lookup"><span data-stu-id="93606-119">getByAlbum</span></span>](mediacollection-getbyalbum.md)                                     | <span data-ttu-id="93606-120">Récupère un objet de [sélection](playlist-object.md) contenant des éléments multimédias de l’album spécifié.</span><span class="sxs-lookup"><span data-stu-id="93606-120">Retrieves a [Playlist](playlist-object.md) object containing media items from the specified album.</span></span>                                                            |
| [<span data-ttu-id="93606-121">getByAttribute</span><span class="sxs-lookup"><span data-stu-id="93606-121">getByAttribute</span></span>](mediacollection-getbyattribute.md)                             | <span data-ttu-id="93606-122">Récupère un objet de [sélection](playlist-object.md) contenant les éléments multimédias avec l’attribut spécifié ayant la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="93606-122">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified attribute having the specified value.</span></span>                             |
| [<span data-ttu-id="93606-123">getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="93606-123">getByAttributeAndMediaType</span></span>](mediacollection-getbyattributeandmediatype.md)     | <span data-ttu-id="93606-124">Récupère un objet de [sélection](playlist-object.md) contenant des objets [multimédias](media-object.md) avec l’attribut et le type de média spécifiés.</span><span class="sxs-lookup"><span data-stu-id="93606-124">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects having the specified attribute and media type.</span></span>                 |
| [<span data-ttu-id="93606-125">getByAuthor</span><span class="sxs-lookup"><span data-stu-id="93606-125">getByAuthor</span></span>](mediacollection-getbyauthor.md)                                   | <span data-ttu-id="93606-126">Récupère un objet de [sélection](playlist-object.md) contenant des éléments multimédias par l’auteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="93606-126">Retrieves a [Playlist](playlist-object.md) object containing media items by the specified author.</span></span>                                                             |
| [<span data-ttu-id="93606-127">getByGenre</span><span class="sxs-lookup"><span data-stu-id="93606-127">getByGenre</span></span>](mediacollection-getbygenre.md)                                     | <span data-ttu-id="93606-128">Récupère un objet de [sélection](playlist-object.md) contenant des éléments multimédias avec le genre spécifié.</span><span class="sxs-lookup"><span data-stu-id="93606-128">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified genre.</span></span>                                                            |
| [<span data-ttu-id="93606-129">getByName</span><span class="sxs-lookup"><span data-stu-id="93606-129">getByName</span></span>](mediacollection-getbyname.md)                                       | <span data-ttu-id="93606-130">Récupère un objet de [sélection](playlist-object.md) contenant des éléments multimédias portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="93606-130">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified name.</span></span>                                                             |
| [<span data-ttu-id="93606-131">getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="93606-131">getMediaAtom</span></span>](mediacollection-getmediaatom.md)                                 | <span data-ttu-id="93606-132">Récupère l’index auquel une propriété spécifiée réside dans le jeu de propriétés disponibles.</span><span class="sxs-lookup"><span data-stu-id="93606-132">Retrieves the index at which a specified property resides within the set of available properties.</span></span>                                                              |
| [<span data-ttu-id="93606-133">getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="93606-133">getPlaylistByQuery</span></span>](mediacollection-getplaylistbyquery.md)                     | <span data-ttu-id="93606-134">Récupère un objet de [sélection](playlist-object.md) contenant des objets [multimédias](media-object.md) qui correspondent aux conditions de requête.</span><span class="sxs-lookup"><span data-stu-id="93606-134">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects that match the query conditions.</span></span>                               |
| [<span data-ttu-id="93606-135">getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="93606-135">getStringCollectionByQuery</span></span>](mediacollection-getstringcollectionbyquery.md)     | <span data-ttu-id="93606-136">Récupère un objet [StringCollection](stringcollection-object.md) contenant des chaînes qui correspondent aux conditions de requête.</span><span class="sxs-lookup"><span data-stu-id="93606-136">Retrieves a [StringCollection](stringcollection-object.md) object containing strings that match the query conditions.</span></span>                                         |
| [<span data-ttu-id="93606-137">isDeleted</span><span class="sxs-lookup"><span data-stu-id="93606-137">isDeleted</span></span>](mediacollection-isdeleted.md)                                       | <span data-ttu-id="93606-138">Récupère une valeur indiquant si l’élément multimédia spécifié se trouve dans le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="93606-138">Retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>                                                                  |
| [<span data-ttu-id="93606-139">remove</span><span class="sxs-lookup"><span data-stu-id="93606-139">remove</span></span>](mediacollection-remove.md)                                             | <span data-ttu-id="93606-140">Supprime un élément de la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="93606-140">Removes an item from the media collection.</span></span>                                                                                                                     |
| [<span data-ttu-id="93606-141">setDeleted</span><span class="sxs-lookup"><span data-stu-id="93606-141">setDeleted</span></span>](mediacollection-setdeleted.md)                                     | <span data-ttu-id="93606-142">Déplace l’élément multimédia spécifié vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="93606-142">Moves the specified media item to the deleted items folder.</span></span>                                                                                                    |



 

<span data-ttu-id="93606-143">L’objet **MediaCollection** est accessible par le biais de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="93606-143">The **MediaCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="93606-144">Object</span><span class="sxs-lookup"><span data-stu-id="93606-144">Object</span></span>                      | <span data-ttu-id="93606-145">Propriété</span><span class="sxs-lookup"><span data-stu-id="93606-145">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="93606-146">Lecteur</span><span class="sxs-lookup"><span data-stu-id="93606-146">Player</span></span>](player-object.md) | [<span data-ttu-id="93606-147">mediaCollection</span><span class="sxs-lookup"><span data-stu-id="93606-147">mediaCollection</span></span>](player-mediacollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="93606-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93606-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93606-149">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="93606-149">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




