---
title: Interface IWMPMedia (VB et C) (WMP. h)
description: Fournit un moyen de définir et de récupérer les propriétés d’un élément multimédia. L’interface IWMPMedia expose les propriétés suivantes.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia (VB et C) interface Windows Media Player
- Interface IWMPMedia (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540619"
---
# <a name="iwmpmedia-vb-and-c-interface"></a><span data-ttu-id="00d17-105">Interface IWMPMedia (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="00d17-105">IWMPMedia (VB and C#) interface</span></span>

<span data-ttu-id="00d17-106">Fournit un moyen de définir et de récupérer les propriétés d’un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="00d17-106">Provides a way to set and retrieve the properties of a media item.</span></span>

<span data-ttu-id="00d17-107">L’interface **IWMPMedia** expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="00d17-107">The **IWMPMedia** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="00d17-108">Membres</span><span class="sxs-lookup"><span data-stu-id="00d17-108">Members</span></span>

<span data-ttu-id="00d17-109">L’interface **IWMPMedia (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00d17-109">The **IWMPMedia (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="00d17-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00d17-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="00d17-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00d17-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="00d17-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="00d17-112">Methods</span></span>

<span data-ttu-id="00d17-113">L’interface **IWMPMedia (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="00d17-113">The **IWMPMedia (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="00d17-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="00d17-114">Method</span></span>                                                                             | <span data-ttu-id="00d17-115">Description</span><span class="sxs-lookup"><span data-stu-id="00d17-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00d17-116">**getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="00d17-116">**getAttributeName**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | <span data-ttu-id="00d17-117">Retourne le nom de l’attribut correspondant à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="00d17-117">Returns the name of the attribute corresponding to the specified index.</span></span><br/>                            |
| [<span data-ttu-id="00d17-118">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="00d17-118">**getItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | <span data-ttu-id="00d17-119">Retourne la valeur de l’attribut spécifié pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="00d17-119">Returns the value of the specified attribute for the media item.</span></span><br/>                                   |
| [<span data-ttu-id="00d17-120">**getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="00d17-120">**getItemInfoByAtom**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | <span data-ttu-id="00d17-121">Retourne la valeur de l’attribut avec le numéro d’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="00d17-121">Returns the value of the attribute with the specified index number.</span></span><br/>                                |
| [<span data-ttu-id="00d17-122">**getMarkerName**</span><span class="sxs-lookup"><span data-stu-id="00d17-122">**getMarkerName**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | <span data-ttu-id="00d17-123">Retourne le nom du marqueur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="00d17-123">Returns the name of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="00d17-124">**getMarkerTime**</span><span class="sxs-lookup"><span data-stu-id="00d17-124">**getMarkerTime**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | <span data-ttu-id="00d17-125">Retourne l’heure du marqueur au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="00d17-125">Returns the time of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="00d17-126">**isMemberOf**</span><span class="sxs-lookup"><span data-stu-id="00d17-126">**isMemberOf**</span></span>](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | <span data-ttu-id="00d17-127">Retourne une valeur indiquant si l’élément multimédia spécifié est membre de la sélection spécifiée.</span><span class="sxs-lookup"><span data-stu-id="00d17-127">Returns a value indicating whether the specified media item is a member of the specified playlist.</span></span><br/> |
| [<span data-ttu-id="00d17-128">**isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="00d17-128">**isReadOnlyItem**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | <span data-ttu-id="00d17-129">Retourne une valeur indiquant si les attributs de l’élément multimédia spécifié peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="00d17-129">Returns a value indicating whether the attributes of the specified media item can be edited.</span></span><br/>       |
| [<span data-ttu-id="00d17-130">**setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="00d17-130">**setItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | <span data-ttu-id="00d17-131">Définit la valeur de l’attribut spécifié pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="00d17-131">Sets the value of the specified attribute for the media item.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="00d17-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00d17-132">Properties</span></span>

<span data-ttu-id="00d17-133">L’interface **IWMPMedia (VB et C#)** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="00d17-133">The **IWMPMedia (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="00d17-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="00d17-134">Property</span></span>                                                                                      | <span data-ttu-id="00d17-135">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="00d17-135">Access type</span></span>          | <span data-ttu-id="00d17-136">Description</span><span class="sxs-lookup"><span data-stu-id="00d17-136">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00d17-137">**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="00d17-137">**attributeCount**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | <span data-ttu-id="00d17-138">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-138">Read-only</span></span><br/> | <span data-ttu-id="00d17-139">Obtient le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="00d17-139">Gets the number of attributes that can be queried and/or set for the media item.</span></span><br/>                                                          |
| [<span data-ttu-id="00d17-140">**Macauley**</span><span class="sxs-lookup"><span data-stu-id="00d17-140">**duration**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | <span data-ttu-id="00d17-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-141">Read-only</span></span><br/> | <span data-ttu-id="00d17-142">Obtient la durée en secondes de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="00d17-142">Gets the duration in seconds of the current media item.</span></span><br/>                                                                                   |
| [<span data-ttu-id="00d17-143">**durationString**</span><span class="sxs-lookup"><span data-stu-id="00d17-143">**durationString**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | <span data-ttu-id="00d17-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-144">Read-only</span></span><br/> | <span data-ttu-id="00d17-145">Obtient une valeur indiquant la durée de l’élément multimédia actuel au format HH : MM : SS.</span><span class="sxs-lookup"><span data-stu-id="00d17-145">Gets a value indicating the duration of the current media item in HH:MM:SS format.</span></span><br/>                                                        |
| [<span data-ttu-id="00d17-146">**imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="00d17-146">**imageSourceHeight**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | <span data-ttu-id="00d17-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-147">Read-only</span></span><br/> | <span data-ttu-id="00d17-148">Obtient la hauteur, en pixels, de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="00d17-148">Gets the height of the current media item in pixels.</span></span><br/>                                                                                      |
| [<span data-ttu-id="00d17-149">**imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="00d17-149">**imageSourceWidth**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | <span data-ttu-id="00d17-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-150">Read-only</span></span><br/> | <span data-ttu-id="00d17-151">Obtient la largeur en pixels de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="00d17-151">Gets the width of the current media item in pixels.</span></span><br/>                                                                                       |
| [<span data-ttu-id="00d17-152">**isIdentical**</span><span class="sxs-lookup"><span data-stu-id="00d17-152">**isIdentical**</span></span>](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | <span data-ttu-id="00d17-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-153">Read-only</span></span><br/> | <span data-ttu-id="00d17-154">Obtient une valeur indiquant si l’élément multimédia spécifié est le même que celui actuel.</span><span class="sxs-lookup"><span data-stu-id="00d17-154">Gets a value indicating whether the specified media item is the same as the current one.</span></span> <span data-ttu-id="00d17-155">En C#, il s’agit de la méthode **\_ isIdentical** .</span><span class="sxs-lookup"><span data-stu-id="00d17-155">In C#, this is the **get\_isIdentical** method.</span></span><br/> |
| [<span data-ttu-id="00d17-156">**markerCount**</span><span class="sxs-lookup"><span data-stu-id="00d17-156">**markerCount**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | <span data-ttu-id="00d17-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-157">Read-only</span></span><br/> | <span data-ttu-id="00d17-158">Obtient le nombre de marqueurs dans l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="00d17-158">Gets the number of markers in the media item.</span></span><br/>                                                                                             |
| [<span data-ttu-id="00d17-159">**nomme**</span><span class="sxs-lookup"><span data-stu-id="00d17-159">**name**</span></span>](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | <span data-ttu-id="00d17-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-160">Read-only</span></span><br/> | <span data-ttu-id="00d17-161">Obtient ou définit le nom de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="00d17-161">Gets or sets the name of the media item.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="00d17-162">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="00d17-162">**sourceURL**</span></span>](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | <span data-ttu-id="00d17-163">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00d17-163">Read-only</span></span><br/> | <span data-ttu-id="00d17-164">Obtient l’URL de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="00d17-164">Gets the URL of the media item.</span></span><br/>                                                                                                           |



 

<span data-ttu-id="00d17-165">Procurez-vous une interface **IWMPMedia** en utilisant les propriétés ou méthodes suivantes accessibles via l’objet ou l’interface suivant.</span><span class="sxs-lookup"><span data-stu-id="00d17-165">Get an **IWMPMedia** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="00d17-166">Objet ou interface</span><span class="sxs-lookup"><span data-stu-id="00d17-166">Object or interface</span></span>                                               | <span data-ttu-id="00d17-167">Propriété ou méthode</span><span class="sxs-lookup"><span data-stu-id="00d17-167">Property or method</span></span>                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00d17-168">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="00d17-168">**IWMPControls**</span></span>](iwmpcontrols--vb-and-c.md)                    | [<span data-ttu-id="00d17-169">**CurrentItem**</span><span class="sxs-lookup"><span data-stu-id="00d17-169">**currentitem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [<span data-ttu-id="00d17-170">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="00d17-170">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="00d17-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="00d17-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [**newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="00d17-172">**IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="00d17-172">**IWMPPlaylist**</span></span>](iwmpplaylist--vb-and-c.md)                    | <span data-ttu-id="00d17-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (recevoir un \_ élément en C#)</span><span class="sxs-lookup"><span data-stu-id="00d17-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (get\_Item in C#)</span></span>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="00d17-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00d17-174">Requirements</span></span>



| <span data-ttu-id="00d17-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00d17-175">Requirement</span></span> | <span data-ttu-id="00d17-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="00d17-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="00d17-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="00d17-177">Header</span></span><br/> | <dl> <span data-ttu-id="00d17-178"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="00d17-178"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d17-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00d17-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d17-180">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="00d17-180">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="00d17-181">**Interface IWMPMedia2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="00d17-181">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00d17-182">**Interface IWMPMedia3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="00d17-182">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





