---
title: Objet PlaylistCollection
description: L’objet PlaylistCollection offre un moyen d’organiser vos sélections.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Objet PlaylistCollection lecteur Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106540758"
---
# <a name="playlistcollection-object"></a><span data-ttu-id="4f5fe-104">Objet PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="4f5fe-104">PlaylistCollection Object</span></span>

<span data-ttu-id="4f5fe-105">L’objet **PlaylistCollection** offre un moyen d’organiser vos sélections.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-105">The **PlaylistCollection** object provides a way to organize your playlists.</span></span>

<span data-ttu-id="4f5fe-106">L’objet **PlaylistCollection** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-106">The **PlaylistCollection** object supports the following methods.</span></span>



| <span data-ttu-id="4f5fe-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="4f5fe-107">Method</span></span>                                                  | <span data-ttu-id="4f5fe-108">Description</span><span class="sxs-lookup"><span data-stu-id="4f5fe-108">Description</span></span>                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f5fe-109">getAll</span><span class="sxs-lookup"><span data-stu-id="4f5fe-109">getAll</span></span>](playlistcollection-getall.md)                 | <span data-ttu-id="4f5fe-110">Récupère un objet [PlaylistArray](playlistarray-object.md) contenant toutes les sélections de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-110">Retrieves a [PlaylistArray](playlistarray-object.md) object containing all the playlists in the library.</span></span>                |
| [<span data-ttu-id="4f5fe-111">getByName</span><span class="sxs-lookup"><span data-stu-id="4f5fe-111">getByName</span></span>](playlistcollection-getbyname.md)           | <span data-ttu-id="4f5fe-112">Récupère un objet [PlaylistArray](playlistarray-object.md) contenant les playlists portant le nom spécifié, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-112">Retrieves a [PlaylistArray](playlistarray-object.md) object containing playlists with the specified name, if any exist.</span></span> |
| [<span data-ttu-id="4f5fe-113">importPlaylist</span><span class="sxs-lookup"><span data-stu-id="4f5fe-113">importPlaylist</span></span>](playlistcollection-importplaylist.md) | <span data-ttu-id="4f5fe-114">Ajoute une sélection statique à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-114">Adds a static playlist to the library.</span></span>                                                                                   |
| [<span data-ttu-id="4f5fe-115">isDeleted</span><span class="sxs-lookup"><span data-stu-id="4f5fe-115">isDeleted</span></span>](playlistcollection-isdeleted.md)           | <span data-ttu-id="4f5fe-116">Récupère une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-116">Retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>                              |
| [<span data-ttu-id="4f5fe-117">newPlaylist</span><span class="sxs-lookup"><span data-stu-id="4f5fe-117">newPlaylist</span></span>](playlistcollection-newplaylist.md)       | <span data-ttu-id="4f5fe-118">Crée une nouvelle sélection dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-118">Creates a new playlist in the library.</span></span>                                                                                   |
| [<span data-ttu-id="4f5fe-119">remove</span><span class="sxs-lookup"><span data-stu-id="4f5fe-119">remove</span></span>](playlistcollection-remove.md)                 | <span data-ttu-id="4f5fe-120">Supprime une sélection de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-120">Removes a playlist from the library.</span></span>                                                                                     |
| [<span data-ttu-id="4f5fe-121">setDeleted</span><span class="sxs-lookup"><span data-stu-id="4f5fe-121">setDeleted</span></span>](playlistcollection-setdeleted.md)         | <span data-ttu-id="4f5fe-122">Déplace une sélection vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-122">Moves a playlist to the deleted items folder.</span></span>                                                                            |



 

<span data-ttu-id="4f5fe-123">L’objet **PlaylistCollection** est accessible par le biais de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="4f5fe-123">The **PlaylistCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="4f5fe-124">Object</span><span class="sxs-lookup"><span data-stu-id="4f5fe-124">Object</span></span>                      | <span data-ttu-id="4f5fe-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="4f5fe-125">Property</span></span>                                            |
|-----------------------------|-----------------------------------------------------|
| [<span data-ttu-id="4f5fe-126">Lecteur</span><span class="sxs-lookup"><span data-stu-id="4f5fe-126">Player</span></span>](player-object.md) | [<span data-ttu-id="4f5fe-127">playlistCollection</span><span class="sxs-lookup"><span data-stu-id="4f5fe-127">playlistCollection</span></span>](player-playlistcollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="4f5fe-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f5fe-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5fe-129">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="4f5fe-129">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




