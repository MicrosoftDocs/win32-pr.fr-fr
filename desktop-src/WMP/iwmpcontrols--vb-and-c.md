---
title: Interface IWMPControls (VB et C) (WMP. h)
description: Fournit un moyen de manipuler la lecture d’un élément multimédia en représentant les contrôles de transport du lecteur Windows Media, tels que lecture, arrêt et pause. l’interface IWMPControls expose les propriétés suivantes.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- IWMPControls (VB et C) interface Windows Media Player
- Interface IWMPControls (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541123"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a><span data-ttu-id="50a3b-105">Interface IWMPControls (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="50a3b-105">IWMPControls (VB and C#) interface</span></span>

<span data-ttu-id="50a3b-106">Fournit un moyen de manipuler la lecture d’un élément multimédia en représentant les contrôles de transport du lecteur Windows Media, tels que lecture, arrêt et pause.</span><span class="sxs-lookup"><span data-stu-id="50a3b-106">Provides a way to manipulate the playback of a media item by representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>

<span data-ttu-id="50a3b-107">L’interface **IWMPControls** expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="50a3b-107">The **IWMPControls** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="50a3b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="50a3b-108">Members</span></span>

<span data-ttu-id="50a3b-109">L’interface **IWMPControls (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="50a3b-109">The **IWMPControls (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="50a3b-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="50a3b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="50a3b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50a3b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="50a3b-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="50a3b-112">Methods</span></span>

<span data-ttu-id="50a3b-113">L’interface **IWMPControls (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="50a3b-113">The **IWMPControls (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="50a3b-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="50a3b-114">Method</span></span>                                                                       | <span data-ttu-id="50a3b-115">Description</span><span class="sxs-lookup"><span data-stu-id="50a3b-115">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50a3b-116">**fastForward**</span><span class="sxs-lookup"><span data-stu-id="50a3b-116">**fastForward**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | <span data-ttu-id="50a3b-117">Démarre la lecture rapide de l’élément multimédia dans le sens avant.</span><span class="sxs-lookup"><span data-stu-id="50a3b-117">Starts fast play of the media item in the forward direction.</span></span><br/>                     |
| [<span data-ttu-id="50a3b-118">**fastReverse**</span><span class="sxs-lookup"><span data-stu-id="50a3b-118">**fastReverse**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | <span data-ttu-id="50a3b-119">Démarre la lecture rapide de l’élément multimédia dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="50a3b-119">Starts fast play of the media item in the reverse direction.</span></span><br/>                     |
| [<span data-ttu-id="50a3b-120">**Situé**</span><span class="sxs-lookup"><span data-stu-id="50a3b-120">**next**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | <span data-ttu-id="50a3b-121">Définit l’élément suivant dans la sélection en tant qu’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="50a3b-121">Sets the next item in the playlist as the current item.</span></span><br/>                          |
| [<span data-ttu-id="50a3b-122">**suspen**</span><span class="sxs-lookup"><span data-stu-id="50a3b-122">**pause**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | <span data-ttu-id="50a3b-123">Suspend la lecture de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="50a3b-123">Pauses playback of the media item.</span></span><br/>                                               |
| [<span data-ttu-id="50a3b-124">**répétition**</span><span class="sxs-lookup"><span data-stu-id="50a3b-124">**play**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | <span data-ttu-id="50a3b-125">Commence la lecture de l’élément multimédia en cours ou reprend la lecture d’un élément suspendu.</span><span class="sxs-lookup"><span data-stu-id="50a3b-125">Begins playback of the current media item, or resumes playback of a paused item.</span></span><br/> |
| [<span data-ttu-id="50a3b-126">**playItem**</span><span class="sxs-lookup"><span data-stu-id="50a3b-126">**playItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | <span data-ttu-id="50a3b-127">Lit l’élément multimédia spécifié.</span><span class="sxs-lookup"><span data-stu-id="50a3b-127">Plays the specified media item.</span></span><br/>                                                  |
| [<span data-ttu-id="50a3b-128">**premier**</span><span class="sxs-lookup"><span data-stu-id="50a3b-128">**previous**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | <span data-ttu-id="50a3b-129">Définit l’élément précédent dans la sélection en tant qu’élément actuel.</span><span class="sxs-lookup"><span data-stu-id="50a3b-129">Sets the previous item in the playlist as the current item.</span></span><br/>                      |
| [<span data-ttu-id="50a3b-130">**erreur**</span><span class="sxs-lookup"><span data-stu-id="50a3b-130">**stop**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | <span data-ttu-id="50a3b-131">Arrête la lecture de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="50a3b-131">Stops playback of the media item.</span></span><br/>                                                |



 

### <a name="properties"></a><span data-ttu-id="50a3b-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50a3b-132">Properties</span></span>

<span data-ttu-id="50a3b-133">L’interface **IWMPControls (VB et C#)** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="50a3b-133">The **IWMPControls (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="50a3b-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="50a3b-134">Property</span></span>                                                                                                    | <span data-ttu-id="50a3b-135">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="50a3b-135">Access type</span></span>           | <span data-ttu-id="50a3b-136">Description</span><span class="sxs-lookup"><span data-stu-id="50a3b-136">Description</span></span>                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50a3b-137">**currentItem**</span><span class="sxs-lookup"><span data-stu-id="50a3b-137">**currentItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | <span data-ttu-id="50a3b-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50a3b-138">Read/write</span></span><br/> | <span data-ttu-id="50a3b-139">Obtient ou définit l’élément multimédia actuel dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="50a3b-139">Gets or sets the current media item in a playlist.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="50a3b-140">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="50a3b-140">**currentMarker**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | <span data-ttu-id="50a3b-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50a3b-141">Read/write</span></span><br/> | <span data-ttu-id="50a3b-142">Obtient ou définit le numéro de marqueur actuel.</span><span class="sxs-lookup"><span data-stu-id="50a3b-142">Gets or sets the current marker number.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="50a3b-143">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="50a3b-143">**currentPosition**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | <span data-ttu-id="50a3b-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50a3b-144">Read/write</span></span><br/> | <span data-ttu-id="50a3b-145">Obtient ou définit la position actuelle dans l’élément multimédia, en secondes, à partir du début.</span><span class="sxs-lookup"><span data-stu-id="50a3b-145">Gets or sets the current position in the media item in seconds from the beginning.</span></span><br/>                                                                                    |
| [<span data-ttu-id="50a3b-146">**currentPositionString**</span><span class="sxs-lookup"><span data-stu-id="50a3b-146">**currentPositionString**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | <span data-ttu-id="50a3b-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50a3b-147">Read-only</span></span><br/>  | <span data-ttu-id="50a3b-148">Obtient la position actuelle dans l’élément multimédia en tant que **System. String**.</span><span class="sxs-lookup"><span data-stu-id="50a3b-148">Gets the current position in the media item as a **System.String**.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="50a3b-149">**isAvailable**</span><span class="sxs-lookup"><span data-stu-id="50a3b-149">**isAvailable**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | <span data-ttu-id="50a3b-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50a3b-150">Read-only</span></span><br/>  | <span data-ttu-id="50a3b-151">Obtient une valeur indiquant si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="50a3b-151">Gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span> <span data-ttu-id="50a3b-152">En C#, il s’agit de la méthode d' **extraction de \_ isAvailable** .</span><span class="sxs-lookup"><span data-stu-id="50a3b-152">In C#, this is the **get\_isAvailable** method.</span></span><br/> |



 

<span data-ttu-id="50a3b-153">Procurez-vous une interface **IWMPControls** à l’aide de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="50a3b-153">Get an **IWMPControls** interface by using the following property.</span></span>



| <span data-ttu-id="50a3b-154">Object</span><span class="sxs-lookup"><span data-stu-id="50a3b-154">Object</span></span>                                                                   | <span data-ttu-id="50a3b-155">Propriété</span><span class="sxs-lookup"><span data-stu-id="50a3b-155">Property</span></span>                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="50a3b-156">Objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="50a3b-156">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="50a3b-157">**Ctlcontrols**</span><span class="sxs-lookup"><span data-stu-id="50a3b-157">**Ctlcontrols**</span></span>](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="50a3b-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50a3b-158">Requirements</span></span>



| <span data-ttu-id="50a3b-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50a3b-159">Requirement</span></span> | <span data-ttu-id="50a3b-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="50a3b-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="50a3b-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="50a3b-161">Header</span></span><br/> | <dl> <span data-ttu-id="50a3b-162"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a3b-162"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50a3b-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50a3b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50a3b-164">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="50a3b-164">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="50a3b-165">**Interface IWMPControls2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="50a3b-165">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="50a3b-166">**Interface IWMPControls3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="50a3b-166">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





