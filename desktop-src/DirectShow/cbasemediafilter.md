---
description: La classe CBaseMediaFilter implémente l’interface IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: CBaseMediaFilter, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528058"
---
# <a name="cbasemediafilter-class"></a><span data-ttu-id="f6d9c-103">CBaseMediaFilter, classe</span><span class="sxs-lookup"><span data-stu-id="f6d9c-103">CBaseMediaFilter class</span></span>

![cbasemediafilter](images/filter05.png)

<span data-ttu-id="f6d9c-105">La `CBaseMediaFilter` classe implémente l’interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) .</span><span class="sxs-lookup"><span data-stu-id="f6d9c-105">The `CBaseMediaFilter` class implements the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface.</span></span> <span data-ttu-id="f6d9c-106">Utilisez cette classe pour les serveurs de distribution de plug-in ou d’autres objets qui doivent prendre en charge **IMediaFilter** sans prendre en charge l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="f6d9c-106">Use this class for plug-in distributors or other objects that need to support **IMediaFilter** without supporting the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="f6d9c-107">N’utilisez pas cette classe pour les filtres.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-107">Do not use this class for filters.</span></span> <span data-ttu-id="f6d9c-108">Utilisez plutôt la classe [**CBaseFilter**](cbasefilter.md) , ou une classe de base dérivée de **CBaseFilter**.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-108">Instead, use the [**CBaseFilter**](cbasefilter.md) class, or a base class derived from **CBaseFilter**.</span></span>



| <span data-ttu-id="f6d9c-109">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="f6d9c-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="f6d9c-110">Description</span><span class="sxs-lookup"><span data-stu-id="f6d9c-110">Description</span></span>                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f6d9c-111">**\_État m**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-111">**m\_State**</span></span>](cbasemediafilter-m-state.md)                     | <span data-ttu-id="f6d9c-112">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-112">Current state of the object.</span></span>                                 |
| [<span data-ttu-id="f6d9c-113">**m \_ pClock**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-113">**m\_pClock**</span></span>](cbasemediafilter-m-pclock.md)                   | <span data-ttu-id="f6d9c-114">Pointeur vers l’horloge de référence de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-114">Pointer to the object's reference clock.</span></span>                     |
| [<span data-ttu-id="f6d9c-115">**m \_ tStart**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-115">**m\_tStart**</span></span>](cbasemediafilter-m-tstart.md)                   | <span data-ttu-id="f6d9c-116">Temps de référence qui correspond au temps de flux 0.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-116">Reference time that corresponds to stream time 0.</span></span>            |
| [<span data-ttu-id="f6d9c-117">**m \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-117">**m\_clsid**</span></span>](cbasemediafilter-m-clsid.md)                     | <span data-ttu-id="f6d9c-118">Identificateur de classe (CLSID) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-118">Class identifier (CLSID) of the object.</span></span>                      |
| [<span data-ttu-id="f6d9c-119">**m \_ pLock**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-119">**m\_pLock**</span></span>](cbasemediafilter-m-plock.md)                     | <span data-ttu-id="f6d9c-120">Pointeur vers une section critique.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-120">Pointer to a critical section.</span></span>                               |
| <span data-ttu-id="f6d9c-121">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="f6d9c-121">Public Methods</span></span>                                                   | <span data-ttu-id="f6d9c-122">Description</span><span class="sxs-lookup"><span data-stu-id="f6d9c-122">Description</span></span>                                                  |
| [<span data-ttu-id="f6d9c-123">**CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-123">**CBaseMediaFilter**</span></span>](cbasemediafilter-cbasemediafilter.md)    | <span data-ttu-id="f6d9c-124">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-124">Constructor method.</span></span>                                          |
| [<span data-ttu-id="f6d9c-125">**~ CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-125">**~ CBaseMediaFilter**</span></span>](cbasemediafilter--cbasemediafilter.md) | <span data-ttu-id="f6d9c-126">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-126">Destructor method.</span></span> <span data-ttu-id="f6d9c-127">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-127">Virtual.</span></span>                                  |
| [<span data-ttu-id="f6d9c-128">**StreamTime**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-128">**StreamTime**</span></span>](cbasemediafilter-streamtime.md)                | <span data-ttu-id="f6d9c-129">Récupère le temps de flux actuel.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-129">Retrieves the current stream time.</span></span> <span data-ttu-id="f6d9c-130">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-130">Virtual.</span></span>                  |
| [<span data-ttu-id="f6d9c-131">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-131">**IsActive**</span></span>](cbasemediafilter-isactive.md)                    | <span data-ttu-id="f6d9c-132">Détermine si l’objet est actif (en cours d’exécution ou en pause).</span><span class="sxs-lookup"><span data-stu-id="f6d9c-132">Determines whether the object is active (running or paused).</span></span> |
| <span data-ttu-id="f6d9c-133">IPersist, méthodes</span><span class="sxs-lookup"><span data-stu-id="f6d9c-133">IPersist Methods</span></span>                                                 | <span data-ttu-id="f6d9c-134">Description</span><span class="sxs-lookup"><span data-stu-id="f6d9c-134">Description</span></span>                                                  |
| [<span data-ttu-id="f6d9c-135">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-135">**GetClassID**</span></span>](cbasemediafilter-getclassid.md)                | <span data-ttu-id="f6d9c-136">Récupère l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-136">Retrieves the class identifier.</span></span>                              |
| <span data-ttu-id="f6d9c-137">Méthodes IMediaFilter</span><span class="sxs-lookup"><span data-stu-id="f6d9c-137">IMediaFilter Methods</span></span>                                             | <span data-ttu-id="f6d9c-138">Description</span><span class="sxs-lookup"><span data-stu-id="f6d9c-138">Description</span></span>                                                  |
| [<span data-ttu-id="f6d9c-139">**GetState**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-139">**GetState**</span></span>](cbasemediafilter-getstate.md)                    | <span data-ttu-id="f6d9c-140">Récupère l’état de l’objet (en cours d’exécution, arrêté ou suspendu).</span><span class="sxs-lookup"><span data-stu-id="f6d9c-140">Retrieves the object's state (running, stopped, or paused).</span></span>  |
| [<span data-ttu-id="f6d9c-141">**SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-141">**SetSyncSource**</span></span>](cbasemediafilter-setsyncsource.md)          | <span data-ttu-id="f6d9c-142">Définit une horloge de référence pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-142">Sets a reference clock for the object.</span></span>                       |
| [<span data-ttu-id="f6d9c-143">**GetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-143">**GetSyncSource**</span></span>](cbasemediafilter-getsyncsource.md)          | <span data-ttu-id="f6d9c-144">Récupère l’horloge de référence utilisée par l’objet.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-144">Retrieves the reference clock that the object is using.</span></span>      |
| [<span data-ttu-id="f6d9c-145">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-145">**Stop**</span></span>](cbasemediafilter-stop.md)                            | <span data-ttu-id="f6d9c-146">Arrête l’objet.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-146">Stops the object.</span></span>                                            |
| [<span data-ttu-id="f6d9c-147">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-147">**Pause**</span></span>](cbasemediafilter-pause.md)                          | <span data-ttu-id="f6d9c-148">Suspend l’objet.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-148">Pauses the object.</span></span>                                           |
| [<span data-ttu-id="f6d9c-149">**Utilisez**</span><span class="sxs-lookup"><span data-stu-id="f6d9c-149">**Run**</span></span>](cbasemediafilter-run.md)                              | <span data-ttu-id="f6d9c-150">Exécute l’objet.</span><span class="sxs-lookup"><span data-stu-id="f6d9c-150">Runs the object.</span></span>                                             |



 

## <a name="requirements"></a><span data-ttu-id="f6d9c-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6d9c-151">Requirements</span></span>



| <span data-ttu-id="f6d9c-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6d9c-152">Requirement</span></span> | <span data-ttu-id="f6d9c-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6d9c-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d9c-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6d9c-154">Header</span></span><br/>  | <dl> <span data-ttu-id="f6d9c-155"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6d9c-155"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f6d9c-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f6d9c-156">Library</span></span><br/> | <dl> <span data-ttu-id="f6d9c-157"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f6d9c-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




