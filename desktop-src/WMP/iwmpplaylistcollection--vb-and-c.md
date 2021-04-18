---
title: Interface IWMPPlaylistCollection (VB et C) (WMP. h)
description: Fournit des méthodes pour manipuler des interfaces IWMPPlaylist et IWMPPlaylistArray dans une collection.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- IWMPPlaylistCollection (VB et C) interface Windows Media Player
- Interface IWMPPlaylistCollection (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc97f9e98838fedc3bd5441d6bfda2da5319dd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525966"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a><span data-ttu-id="62c96-105">Interface IWMPPlaylistCollection (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="62c96-105">IWMPPlaylistCollection (VB and C#) interface</span></span>

<span data-ttu-id="62c96-106">Fournit des méthodes pour manipuler des interfaces **IWMPPlaylist** et **IWMPPlaylistArray** dans une collection.</span><span class="sxs-lookup"><span data-stu-id="62c96-106">Provides methods for manipulating **IWMPPlaylist** and **IWMPPlaylistArray** interfaces in a collection.</span></span>

## <a name="members"></a><span data-ttu-id="62c96-107">Membres</span><span class="sxs-lookup"><span data-stu-id="62c96-107">Members</span></span>

<span data-ttu-id="62c96-108">L’interface **IWMPPlaylistCollection (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="62c96-108">The **IWMPPlaylistCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="62c96-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="62c96-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="62c96-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="62c96-110">Methods</span></span>

<span data-ttu-id="62c96-111">L’interface **IWMPPlaylistCollection (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="62c96-111">The **IWMPPlaylistCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="62c96-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="62c96-112">Method</span></span>                                                                                                 | <span data-ttu-id="62c96-113">Description</span><span class="sxs-lookup"><span data-stu-id="62c96-113">Description</span></span>                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62c96-114">**getAll**</span><span class="sxs-lookup"><span data-stu-id="62c96-114">**getAll**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | <span data-ttu-id="62c96-115">Retourne une interface **IWMPPlaylistArray** qui fournit l’accès à toutes les playlists de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="62c96-115">Returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span><br/>             |
| [<span data-ttu-id="62c96-116">**getByName**</span><span class="sxs-lookup"><span data-stu-id="62c96-116">**getByName**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | <span data-ttu-id="62c96-117">Retourne une interface **IWMPPlaylistArray** qui fournit l’accès aux sélections portant le nom spécifié, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="62c96-117">Returns an **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span><br/> |
| [<span data-ttu-id="62c96-118">**importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="62c96-118">**importPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | <span data-ttu-id="62c96-119">Ajoute une sélection statique à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="62c96-119">Adds a static playlist to the library.</span></span><br/>                                                                              |
| [<span data-ttu-id="62c96-120">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="62c96-120">**isDeleted**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | <span data-ttu-id="62c96-121">Retourne une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="62c96-121">Returns a value indicating whether the specified playlist is in the deleted items folder.</span></span><br/>                           |
| [<span data-ttu-id="62c96-122">**newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="62c96-122">**newPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | <span data-ttu-id="62c96-123">Retourne une interface **IWMPPlaylist** pour une nouvelle playlist vide dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="62c96-123">Returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span><br/>                                     |
| [<span data-ttu-id="62c96-124">**Installez**</span><span class="sxs-lookup"><span data-stu-id="62c96-124">**remove**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | <span data-ttu-id="62c96-125">Supprime une sélection de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="62c96-125">Removes a playlist from the library.</span></span><br/>                                                                                |
| <span data-ttu-id="62c96-126">**setDeleted**</span><span class="sxs-lookup"><span data-stu-id="62c96-126">**setDeleted**</span></span>                                                                                         | <span data-ttu-id="62c96-127">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="62c96-127">No longer supported.</span></span><br/>                                                                                                |



 

<span data-ttu-id="62c96-128">Procurez-vous une interface **IWMPPlaylistCollection** à l’aide de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="62c96-128">Get an **IWMPPlaylistCollection** interface by using the following property.</span></span>



| <span data-ttu-id="62c96-129">Object</span><span class="sxs-lookup"><span data-stu-id="62c96-129">Object</span></span>                                                                   | <span data-ttu-id="62c96-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="62c96-130">Property</span></span>                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62c96-131">Objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="62c96-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="62c96-132">**playlistCollection**</span><span class="sxs-lookup"><span data-stu-id="62c96-132">**playlistCollection**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="62c96-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62c96-133">Requirements</span></span>



| <span data-ttu-id="62c96-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62c96-134">Requirement</span></span> | <span data-ttu-id="62c96-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="62c96-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62c96-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="62c96-136">Header</span></span><br/> | <dl> <span data-ttu-id="62c96-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c96-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c96-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62c96-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c96-139">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="62c96-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="62c96-140">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="62c96-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="62c96-141">**Interface IWMPPlaylistArray (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="62c96-141">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





