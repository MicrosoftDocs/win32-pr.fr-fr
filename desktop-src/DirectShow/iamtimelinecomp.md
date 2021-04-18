---
description: L’interface IAMTimelineComp insère ou récupère des pistes virtuelles sur une composition dans les services d’édition DirectShow (DES). Une composition est une collection de couches qui agit comme une seule piste composite.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Interface IAMTimelineComp (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540101"
---
# <a name="iamtimelinecomp-interface"></a><span data-ttu-id="c2fdf-103">Interface IAMTimelineComp</span><span class="sxs-lookup"><span data-stu-id="c2fdf-103">IAMTimelineComp interface</span></span>

> [!Note]  
> <span data-ttu-id="c2fdf-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-104">\[Deprecated.</span></span> <span data-ttu-id="c2fdf-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2fdf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c2fdf-106">L’interface **IAMTimelineComp** insère ou récupère des pistes virtuelles sur une composition dans les [services d’édition DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="c2fdf-106">The **IAMTimelineComp** interface inserts or retrieves virtual tracks on a composition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="c2fdf-107">Une composition est une collection de couches qui agit comme une seule *piste* composite. Par exemple, une composition qui contient deux pistes avec une transition entre elles agit comme une seule piste avec la transition précomposée.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-107">A composition is a collection of layers that acts as a single, composited *track*. For example, a composition that contains two tracks with a transition between them acts as a single track with the transition precomposited.</span></span> <span data-ttu-id="c2fdf-108">Une composition doit contenir un média d’un seul type (audio ou vidéo), mais cette limitation n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-108">A composition should contain media of only one type (such as audio or video), but this limitation is not enforced.</span></span> <span data-ttu-id="c2fdf-109">Une *piste virtuelle* est un objet qui peut résider dans une composition, y compris des pistes et d’autres compositions.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-109">A *virtual track* is any object that can reside in a composition, including tracks and other compositions.</span></span>

<span data-ttu-id="c2fdf-110">Les nœuds les plus haut dans la chronologie sont des *groupes*.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-110">The topmost nodes in the timeline are *groups*.</span></span> <span data-ttu-id="c2fdf-111">Les groupes implémentent à la fois l' `IAMTimelineComp` interface et l’interface [**IAMTimelineGroup**](iamtimelinegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="c2fdf-111">Groups implement both the `IAMTimelineComp` interface and the [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="c2fdf-112">Pour créer un objet de composition, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec la chronologie valeur de \_ \_ type principal \_ composite.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-112">To create a composition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_COMPOSITE.</span></span> <span data-ttu-id="c2fdf-113">Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l' `IAMTimelineComp` interface.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineComp` interface.</span></span> <span data-ttu-id="c2fdf-114">Pour plus d’informations, consultez [le modèle de chronologie](the-timeline-model.md) et [construction d’une chronologie](constructing-a-timeline.md).</span><span class="sxs-lookup"><span data-stu-id="c2fdf-114">For more information, see [The Timeline Model](the-timeline-model.md) and [Constructing a Timeline](constructing-a-timeline.md).</span></span>

## <a name="members"></a><span data-ttu-id="c2fdf-115">Membres</span><span class="sxs-lookup"><span data-stu-id="c2fdf-115">Members</span></span>

<span data-ttu-id="c2fdf-116">L’interface **IAMTimelineComp** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c2fdf-116">The **IAMTimelineComp** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c2fdf-117">**IAMTimelineComp** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c2fdf-117">**IAMTimelineComp** also has these types of members:</span></span>

-   [<span data-ttu-id="c2fdf-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c2fdf-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c2fdf-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c2fdf-119">Methods</span></span>

<span data-ttu-id="c2fdf-120">L’interface **IAMTimelineComp** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-120">The **IAMTimelineComp** interface has these methods.</span></span>



| <span data-ttu-id="c2fdf-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="c2fdf-121">Method</span></span>                                                                       | <span data-ttu-id="c2fdf-122">Description</span><span class="sxs-lookup"><span data-stu-id="c2fdf-122">Description</span></span>                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2fdf-123">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="c2fdf-123">**GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)                     | <span data-ttu-id="c2fdf-124">Récupère le nombre d’objets d’un type donné contenus dans cette composition et toutes ses pistes virtuelles, de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-124">Retrieves the number of objects of a given type contained in this composition and all of its virtual tracks, recursively.</span></span><br/>                      |
| [<span data-ttu-id="c2fdf-125">**GetNextVTrack**</span><span class="sxs-lookup"><span data-stu-id="c2fdf-125">**GetNextVTrack**</span></span>](iamtimelinecomp-getnextvtrack.md)                       | <span data-ttu-id="c2fdf-126">Récupère la piste virtuelle suivante après une piste virtuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-126">Retrieves the next virtual track after a specified virtual track.</span></span><br/>                                                                              |
| [<span data-ttu-id="c2fdf-127">**GetRecursiveLayerOfType**</span><span class="sxs-lookup"><span data-stu-id="c2fdf-127">**GetRecursiveLayerOfType**</span></span>](iamtimelinecomp-getrecursivelayeroftype.md)   | <span data-ttu-id="c2fdf-128">Effectue un classement à profondeur prioritaire des pistes virtuelles contenues dans cette composition, et récupère la *n* ième piste virtuelle à partir de ce classement.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-128">Performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span><br/> |
| [<span data-ttu-id="c2fdf-129">**GetRecursiveLayerOfTypeI**</span><span class="sxs-lookup"><span data-stu-id="c2fdf-129">**GetRecursiveLayerOfTypeI**</span></span>](iamtimelinecomp-getrecursivelayeroftypei.md) | <span data-ttu-id="c2fdf-130">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-130">Not supported.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="c2fdf-131">**GetVTrack**</span><span class="sxs-lookup"><span data-stu-id="c2fdf-131">**GetVTrack**</span></span>](iamtimelinecomp-getvtrack.md)                               | <span data-ttu-id="c2fdf-132">Récupère la piste virtuelle à la priorité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-132">Retrieves the virtual track at the specified priority.</span></span><br/>                                                                                         |
| [<span data-ttu-id="c2fdf-133">**VTrackGetCount**</span><span class="sxs-lookup"><span data-stu-id="c2fdf-133">**VTrackGetCount**</span></span>](iamtimelinecomp-vtrackgetcount.md)                     | <span data-ttu-id="c2fdf-134">Récupère le nombre de pistes virtuelles contenues dans la composition.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-134">Retrieves the number of virtual tracks contained in the composition.</span></span><br/>                                                                           |
| [<span data-ttu-id="c2fdf-135">**VTrackInsBefore**</span><span class="sxs-lookup"><span data-stu-id="c2fdf-135">**VTrackInsBefore**</span></span>](iamtimelinecomp-vtrackinsbefore.md)                   | <span data-ttu-id="c2fdf-136">Insère une piste virtuelle dans la composition à la priorité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-136">Inserts a virtual track into the composition at the specified priority.</span></span><br/>                                                                        |
| [<span data-ttu-id="c2fdf-137">**VTrackSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="c2fdf-137">**VTrackSwapPriorities**</span></span>](iamtimelinecomp-vtrackswappriorities.md)         | <span data-ttu-id="c2fdf-138">Change les niveaux de priorité de deux pistes.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-138">Switches the priority levels of two tracks.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="c2fdf-139">Notes</span><span class="sxs-lookup"><span data-stu-id="c2fdf-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2fdf-140">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c2fdf-141">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c2fdf-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c2fdf-142">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c2fdf-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2fdf-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2fdf-143">Requirements</span></span>



| <span data-ttu-id="c2fdf-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2fdf-144">Requirement</span></span> | <span data-ttu-id="c2fdf-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2fdf-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2fdf-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2fdf-146">Header</span></span><br/>  | <dl> <span data-ttu-id="c2fdf-147"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2fdf-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c2fdf-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2fdf-148">Library</span></span><br/> | <dl> <span data-ttu-id="c2fdf-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2fdf-149"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
