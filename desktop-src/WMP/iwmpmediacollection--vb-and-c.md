---
title: Interface IWMPMediaCollection (VB et C) (WMP. h)
description: Fournit des méthodes qui peuvent être utilisées pour organiser une grande collection d’éléments multimédias.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- IWMPMediaCollection (VB et C) interface Windows Media Player
- Interface IWMPMediaCollection (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542797"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a><span data-ttu-id="b3e59-105">Interface IWMPMediaCollection (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="b3e59-105">IWMPMediaCollection (VB and C#) interface</span></span>

<span data-ttu-id="b3e59-106">Fournit des méthodes qui peuvent être utilisées pour organiser une grande collection d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="b3e59-106">Provides methods that can be used to organize a large collection of media items.</span></span>

## <a name="members"></a><span data-ttu-id="b3e59-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b3e59-107">Members</span></span>

<span data-ttu-id="b3e59-108">L’interface **IWMPMediaCollection (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b3e59-108">The **IWMPMediaCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="b3e59-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b3e59-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b3e59-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b3e59-110">Methods</span></span>

<span data-ttu-id="b3e59-111">L’interface **IWMPMediaCollection (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b3e59-111">The **IWMPMediaCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="b3e59-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="b3e59-112">Method</span></span>                                                                                                                       | <span data-ttu-id="b3e59-113">Description</span><span class="sxs-lookup"><span data-stu-id="b3e59-113">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3e59-114">**add**</span><span class="sxs-lookup"><span data-stu-id="b3e59-114">**add**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | <span data-ttu-id="b3e59-115">Ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b3e59-115">Adds a new media item or playlist to the library.</span></span><br/>                                                                                  |
| [<span data-ttu-id="b3e59-116">**getAll**</span><span class="sxs-lookup"><span data-stu-id="b3e59-116">**getAll**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | <span data-ttu-id="b3e59-117">Retourne une interface **IWMPPlaylist** qui correspond à la sélection qui contient tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b3e59-117">Returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span><br/>               |
| [<span data-ttu-id="b3e59-118">**getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="b3e59-118">**getAttributeStringCollection**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | <span data-ttu-id="b3e59-119">Retourne une interface **IWMPStringCollection** qui représente le jeu de toutes les valeurs pour un attribut spécifié dans un type de média.</span><span class="sxs-lookup"><span data-stu-id="b3e59-119">Returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span><br/> |
| [<span data-ttu-id="b3e59-120">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="b3e59-120">**getByAlbum**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | <span data-ttu-id="b3e59-121">Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias à partir de l’album spécifié.</span><span class="sxs-lookup"><span data-stu-id="b3e59-121">Returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span><br/>                                |
| [<span data-ttu-id="b3e59-122">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="b3e59-122">**getByAttribute**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | <span data-ttu-id="b3e59-123">Retourne une interface **IWMPPlaylist** qui correspond à l’attribut spécifié ayant la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b3e59-123">Returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span><br/>                      |
| [<span data-ttu-id="b3e59-124">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="b3e59-124">**getByAuthor**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | <span data-ttu-id="b3e59-125">Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias par l’auteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="b3e59-125">Returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span><br/>                             |
| [<span data-ttu-id="b3e59-126">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="b3e59-126">**getByGenre**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | <span data-ttu-id="b3e59-127">Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias du genre spécifié.</span><span class="sxs-lookup"><span data-stu-id="b3e59-127">Returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span><br/>                                  |
| [<span data-ttu-id="b3e59-128">**getByName**</span><span class="sxs-lookup"><span data-stu-id="b3e59-128">**getByName**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | <span data-ttu-id="b3e59-129">Retourne une interface **IWMPPlaylist** qui fournit l’accès aux éléments multimédias avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="b3e59-129">Returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span><br/>                                 |
| [<span data-ttu-id="b3e59-130">**getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="b3e59-130">**getMediaAtom**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | <span data-ttu-id="b3e59-131">Retourne l’index d’un attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="b3e59-131">Returns the index of a specified attribute.</span></span><br/>                                                                                        |
| <span data-ttu-id="b3e59-132">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="b3e59-132">**isDeleted**</span></span>                                                                                                                | <span data-ttu-id="b3e59-133">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b3e59-133">No longer supported.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="b3e59-134">**Installez**</span><span class="sxs-lookup"><span data-stu-id="b3e59-134">**remove**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | <span data-ttu-id="b3e59-135">Supprime l’élément multimédia spécifié de la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="b3e59-135">Removes the specified media item from the media collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="b3e59-136">**setDeleted**</span><span class="sxs-lookup"><span data-stu-id="b3e59-136">**setDeleted**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | <span data-ttu-id="b3e59-137">Déplace l’élément multimédia spécifié vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="b3e59-137">Moves the specified media item to the deleted items folder.</span></span><br/>                                                                        |



 

<span data-ttu-id="b3e59-138">Procurez-vous une interface **IWMPMediaCollection** en utilisant les propriétés suivantes accessibles via l’objet ou l’interface suivant.</span><span class="sxs-lookup"><span data-stu-id="b3e59-138">Get an **IWMPMediaCollection** interface by using the following properties accessed through the following object or interface.</span></span>



| <span data-ttu-id="b3e59-139">Objet ou interface</span><span class="sxs-lookup"><span data-stu-id="b3e59-139">Object or interface</span></span>                                               | <span data-ttu-id="b3e59-140">Propriété</span><span class="sxs-lookup"><span data-stu-id="b3e59-140">Property</span></span>                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3e59-141">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="b3e59-141">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="b3e59-142">**mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="b3e59-142">**mediaCollection**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [<span data-ttu-id="b3e59-143">**IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="b3e59-143">**IWMPLibrary**</span></span>](iwmplibrary--vb-and-c.md)                      | [<span data-ttu-id="b3e59-144">**mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="b3e59-144">**mediaCollection**</span></span>](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="b3e59-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3e59-145">Requirements</span></span>



| <span data-ttu-id="b3e59-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3e59-146">Requirement</span></span> | <span data-ttu-id="b3e59-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3e59-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b3e59-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3e59-148">Header</span></span><br/> | <dl> <span data-ttu-id="b3e59-149"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3e59-149"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3e59-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3e59-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e59-151">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="b3e59-151">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="b3e59-152">**Interface IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="b3e59-152">**IWMPMediaCollection2 Interface**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b3e59-153">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b3e59-153">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b3e59-154">**Interface IWMPStringCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b3e59-154">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





