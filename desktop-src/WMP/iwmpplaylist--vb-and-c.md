---
title: IWMPPlaylist (VB et C), interface (Wmp.h)
description: Fournit des propriétés et des méthodes pour organiser, gérer et manipuler des éléments multimédias dans une sélection. L’interface IWMPPlaylist expose les propriétés suivantes.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- IWMPPlaylist (VB et C) interface Windows Media Player
- Interface IWMPPlaylist (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52090588905e2fd79b218abe939f78c1e38fc79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541622"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a><span data-ttu-id="07ec0-105">Interface IWMPPlaylist (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="07ec0-105">IWMPPlaylist (VB and C#) interface</span></span>

<span data-ttu-id="07ec0-106">Fournit des propriétés et des méthodes pour organiser, gérer et manipuler des éléments multimédias dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="07ec0-106">Provides properties and methods to organize, manage, and manipulate media items in a playlist.</span></span>

<span data-ttu-id="07ec0-107">L’interface **IWMPPlaylist** expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="07ec0-107">The **IWMPPlaylist** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="07ec0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="07ec0-108">Members</span></span>

<span data-ttu-id="07ec0-109">L’interface **IWMPPlaylist (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="07ec0-109">The **IWMPPlaylist (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="07ec0-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="07ec0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="07ec0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="07ec0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07ec0-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="07ec0-112">Methods</span></span>

<span data-ttu-id="07ec0-113">L’interface **IWMPPlaylist (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="07ec0-113">The **IWMPPlaylist (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="07ec0-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="07ec0-114">Method</span></span>                                                                       | <span data-ttu-id="07ec0-115">Description</span><span class="sxs-lookup"><span data-stu-id="07ec0-115">Description</span></span>                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="07ec0-116">**appendItem**</span><span class="sxs-lookup"><span data-stu-id="07ec0-116">**appendItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | <span data-ttu-id="07ec0-117">Ajoute un élément multimédia à la fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="07ec0-117">Adds a media item to the end of the playlist.</span></span><br/>                |
| [<span data-ttu-id="07ec0-118">**effacé**</span><span class="sxs-lookup"><span data-stu-id="07ec0-118">**clear**</span></span>](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | <span data-ttu-id="07ec0-119">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="07ec0-119">Reserved for future use.</span></span><br/>                                     |
| [<span data-ttu-id="07ec0-120">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="07ec0-120">**getItemInfo**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | <span data-ttu-id="07ec0-121">Retourne la valeur d’un attribut playlist spécifié par Name.</span><span class="sxs-lookup"><span data-stu-id="07ec0-121">Returns the value of a playlist attribute specified by name.</span></span><br/> |
| [<span data-ttu-id="07ec0-122">**insertItem**</span><span class="sxs-lookup"><span data-stu-id="07ec0-122">**insertItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | <span data-ttu-id="07ec0-123">Insère un élément multimédia à un emplacement spécifié dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="07ec0-123">Inserts a media item at a specified location in a playlist.</span></span><br/>  |
| [<span data-ttu-id="07ec0-124">**moveItem**</span><span class="sxs-lookup"><span data-stu-id="07ec0-124">**moveItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | <span data-ttu-id="07ec0-125">Modifie l’emplacement d’un élément multimédia dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="07ec0-125">Changes the location of a media item in the playlist.</span></span><br/>        |
| [<span data-ttu-id="07ec0-126">**removeItem**</span><span class="sxs-lookup"><span data-stu-id="07ec0-126">**removeItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | <span data-ttu-id="07ec0-127">Supprime l’élément multimédia spécifié de la sélection.</span><span class="sxs-lookup"><span data-stu-id="07ec0-127">Removes the specified media item from the playlist.</span></span><br/>          |
| [<span data-ttu-id="07ec0-128">**setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="07ec0-128">**setItemInfo**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | <span data-ttu-id="07ec0-129">Définit la valeur d’un attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="07ec0-129">Sets the value of a playlist attribute.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="07ec0-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="07ec0-130">Properties</span></span>

<span data-ttu-id="07ec0-131">L’interface **IWMPPlaylist (VB et C#)** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="07ec0-131">The **IWMPPlaylist (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="07ec0-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="07ec0-132">Property</span></span>                                                                                      | <span data-ttu-id="07ec0-133">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="07ec0-133">Access type</span></span>           | <span data-ttu-id="07ec0-134">Description</span><span class="sxs-lookup"><span data-stu-id="07ec0-134">Description</span></span>                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07ec0-135">**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="07ec0-135">**attributeCount**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | <span data-ttu-id="07ec0-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07ec0-136">Read-only</span></span><br/>  | <span data-ttu-id="07ec0-137">Obtient le nombre d’attributs associés à une sélection.</span><span class="sxs-lookup"><span data-stu-id="07ec0-137">Gets the number of attributes associated with a playlist.</span></span><br/>                                                                                |
| [<span data-ttu-id="07ec0-138">**attributeName**</span><span class="sxs-lookup"><span data-stu-id="07ec0-138">**attributeName**</span></span>](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | <span data-ttu-id="07ec0-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07ec0-139">Read-only</span></span><br/>  | <span data-ttu-id="07ec0-140">Obtient le nom d’un attribut de sélection spécifié par un index.</span><span class="sxs-lookup"><span data-stu-id="07ec0-140">Gets the name of a playlist attribute specified by an index.</span></span> <span data-ttu-id="07ec0-141">En C#, il s’agit de la méthode d’extraction de \_ AttributeName.</span><span class="sxs-lookup"><span data-stu-id="07ec0-141">In C# this is the get\_attributeName method.</span></span><br/>                               |
| [<span data-ttu-id="07ec0-142">**saut**</span><span class="sxs-lookup"><span data-stu-id="07ec0-142">**count**</span></span>](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | <span data-ttu-id="07ec0-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07ec0-143">Read-only</span></span><br/>  | <span data-ttu-id="07ec0-144">Obtient le nombre d’éléments multimédias dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="07ec0-144">Gets the number of media items in a playlist.</span></span><br/>                                                                                            |
| [<span data-ttu-id="07ec0-145">**isIdentical**</span><span class="sxs-lookup"><span data-stu-id="07ec0-145">**isIdentical**</span></span>](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | <span data-ttu-id="07ec0-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07ec0-146">Read-only</span></span><br/>  | <span data-ttu-id="07ec0-147">Obtient une valeur indiquant si la sélection spécifiée est identique à la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="07ec0-147">Gets a value indicating whether the specified playlist is identical to the current playlist.</span></span> <span data-ttu-id="07ec0-148">En C#, il s’agit de la \_ méthode isIdentical.</span><span class="sxs-lookup"><span data-stu-id="07ec0-148">In C# this is the get\_isIdentical method.</span></span><br/> |
| [<span data-ttu-id="07ec0-149">**Élément**</span><span class="sxs-lookup"><span data-stu-id="07ec0-149">**Item**</span></span>](iwmpplaylist-item--vb-and-c.md)<br/>                                        | <span data-ttu-id="07ec0-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="07ec0-150">Read-only</span></span><br/>  | <span data-ttu-id="07ec0-151">Obtient une interface pour l’élément multimédia à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="07ec0-151">Gets an interface to the media item at the specified index.</span></span> <span data-ttu-id="07ec0-152">En C#, il s’agit de la méthode d’extraction d' \_ élément.</span><span class="sxs-lookup"><span data-stu-id="07ec0-152">In C# this is the get\_Item method.</span></span><br/>                                         |
| [<span data-ttu-id="07ec0-153">**nomme**</span><span class="sxs-lookup"><span data-stu-id="07ec0-153">**name**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | <span data-ttu-id="07ec0-154">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="07ec0-154">Read/write</span></span><br/> | <span data-ttu-id="07ec0-155">Obtient ou définit le nom de la sélection.</span><span class="sxs-lookup"><span data-stu-id="07ec0-155">Gets or sets the name of the playlist.</span></span><br/>                                                                                                   |



 

<span data-ttu-id="07ec0-156">Procurez-vous une interface **IWMPPlaylist** en utilisant les propriétés ou méthodes suivantes accessibles via l’objet ou l’interface suivant.</span><span class="sxs-lookup"><span data-stu-id="07ec0-156">Get an **IWMPPlaylist** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="07ec0-157">Objet ou interface</span><span class="sxs-lookup"><span data-stu-id="07ec0-157">Object or interface</span></span>                                                | <span data-ttu-id="07ec0-158">Propriété ou méthode</span><span class="sxs-lookup"><span data-stu-id="07ec0-158">Property or method</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07ec0-159">**IWMPCdrom**</span><span class="sxs-lookup"><span data-stu-id="07ec0-159">**IWMPCdrom**</span></span>](iwmpcdrom--vb-and-c.md)                           | [<span data-ttu-id="07ec0-160">**Playlist**</span><span class="sxs-lookup"><span data-stu-id="07ec0-160">**Playlist**</span></span>](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="07ec0-161">**IWMPMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="07ec0-161">**IWMPMediaCollection**</span></span>](iwmpmediacollection--vb-and-c.md)       | <span data-ttu-id="07ec0-162">[**GetAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**GetByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)</span><span class="sxs-lookup"><span data-stu-id="07ec0-162">[**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)</span></span> |
| [<span data-ttu-id="07ec0-163">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="07ec0-163">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md)  | <span data-ttu-id="07ec0-164">[**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="07ec0-164">[**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [**newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="07ec0-165">**IWMPPlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="07ec0-165">**IWMPPlaylistArray**</span></span>](iwmpplaylistarray--vb-and-c.md)           | [<span data-ttu-id="07ec0-166">**Élément**</span><span class="sxs-lookup"><span data-stu-id="07ec0-166">**Item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="07ec0-167">**IWMPPlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="07ec0-167">**IWMPPlaylistCollection**</span></span>](iwmpplaylistcollection--vb-and-c.md) | [<span data-ttu-id="07ec0-168">**newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="07ec0-168">**newPlaylist**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="07ec0-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07ec0-169">Requirements</span></span>



| <span data-ttu-id="07ec0-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07ec0-170">Requirement</span></span> | <span data-ttu-id="07ec0-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="07ec0-171">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="07ec0-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="07ec0-172">Header</span></span><br/> | <dl> <span data-ttu-id="07ec0-173"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="07ec0-173"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07ec0-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07ec0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ec0-175">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="07ec0-175">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





