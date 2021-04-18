---
description: 'La méthode GetBuffer récupère un exemple de support qui contient une mémoire tampon. Cette méthode implémente la méthode IMemAllocator :: GetBuffer.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Méthode CBaseAllocator. GetBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526414"
---
# <a name="cbaseallocatorgetbuffer-method"></a><span data-ttu-id="6e4b7-104">Méthode CBaseAllocator. GetBuffer</span><span class="sxs-lookup"><span data-stu-id="6e4b7-104">CBaseAllocator.GetBuffer method</span></span>

<span data-ttu-id="6e4b7-105">La `GetBuffer` méthode récupère un exemple de média qui contient une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-105">The `GetBuffer` method retrieves a media sample that contains a buffer.</span></span> <span data-ttu-id="6e4b7-106">Cette méthode implémente la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="6e4b7-106">This method implements the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4b7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e4b7-107">Syntax</span></span>


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6e4b7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e4b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e4b7-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="6e4b7-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="6e4b7-110">Reçoit un pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-110">Receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="6e4b7-111">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-111">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="6e4b7-112">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="6e4b7-112">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6e4b7-113">Pointeur vers l’heure de début de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-113">Pointer to the start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="6e4b7-114">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="6e4b7-114">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6e4b7-115">Pointeur vers l’heure de fin de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-115">Pointer to the end time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="6e4b7-116">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6e4b7-116">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="6e4b7-117">Combinaison d’opérations de bits de zéro ou plusieurs indicateurs.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-117">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="6e4b7-118">La classe de base prend en charge l’indicateur suivant.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-118">The base class supports the following flag.</span></span>



| <span data-ttu-id="6e4b7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e4b7-119">Value</span></span>                                                                                                                                                          | <span data-ttu-id="6e4b7-120">Signification</span><span class="sxs-lookup"><span data-stu-id="6e4b7-120">Meaning</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <span data-ttu-id="6e4b7-121"><dt>**AM \_ GBF \_ NOWAIT**</dt></span><span class="sxs-lookup"><span data-stu-id="6e4b7-121"><dt>**AM\_GBF\_NOWAIT**</dt></span></span> </dl> | <span data-ttu-id="6e4b7-122">N’attendez pas qu’une mémoire tampon devienne disponible.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-122">Do not wait for a buffer to become available.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e4b7-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e4b7-123">Return value</span></span>

<span data-ttu-id="6e4b7-124">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-124">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="6e4b7-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6e4b7-125">Return code</span></span>                                                                                           | <span data-ttu-id="6e4b7-126">Description</span><span class="sxs-lookup"><span data-stu-id="6e4b7-126">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="6e4b7-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6e4b7-127"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="6e4b7-128">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-128">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="6e4b7-129"><dt>**VFW \_ E \_ non \_ validé**</dt></span><span class="sxs-lookup"><span data-stu-id="6e4b7-129"><dt>**VFW\_E\_NOT\_COMMITTED**</dt></span></span> </dl> | <span data-ttu-id="6e4b7-130">Allocator n’a pas été validé.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-130">Allocator was not committed.</span></span><br/> |
| <dl> <span data-ttu-id="6e4b7-131"><dt>**\_ \_ délai d’expiration VFW E**</dt></span><span class="sxs-lookup"><span data-stu-id="6e4b7-131"><dt>**VFW\_E\_TIMEOUT**</dt></span></span> </dl>        | <span data-ttu-id="6e4b7-132">Expiration du délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-132">Timed out.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="6e4b7-133">Notes</span><span class="sxs-lookup"><span data-stu-id="6e4b7-133">Remarks</span></span>

<span data-ttu-id="6e4b7-134">À moins que l’appelant ne spécifie l’indicateur **am \_ GBF \_ NOWAIT** dans *dwFlags*, cette méthode se bloque jusqu’à ce que l’exemple suivant soit disponible.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-134">Unless the caller specifies the **AM\_GBF\_NOWAIT** flag in *dwFlags*, this method blocks until the next sample is available.</span></span>

<span data-ttu-id="6e4b7-135">L’exemple de média récupéré possède un pointeur valide vers la mémoire tampon allouée.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-135">The retrieved media sample has a valid pointer to the allocated buffer.</span></span> <span data-ttu-id="6e4b7-136">L’appelant est chargé de définir d’autres propriétés sur l’exemple, telles que les horodatages, les heures de média ou la propriété de point de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-136">The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property.</span></span> <span data-ttu-id="6e4b7-137">Pour plus d’informations, consultez [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span><span class="sxs-lookup"><span data-stu-id="6e4b7-137">For more information, see [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span></span>

<span data-ttu-id="6e4b7-138">Dans la classe de base, les paramètres *pStartTime* et *pEndTime* sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-138">In the base class, the *pStartTime* and *pEndTime* parameters are ignored.</span></span> <span data-ttu-id="6e4b7-139">Les classes dérivées peuvent utiliser ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-139">Derived classes can use these values.</span></span> <span data-ttu-id="6e4b7-140">Par exemple, l’allocateur pour le filtre de [convertisseur vidéo](video-renderer-filter.md) utilise ces valeurs pour synchroniser le basculement entre les surfaces DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-140">For example, the allocator for the [Video Renderer](video-renderer-filter.md) filter uses these values to synchronize switching between DirectDraw surfaces.</span></span>

<span data-ttu-id="6e4b7-141">Si la méthode doit attendre un échantillon, elle incrémente le nombre d’objets en attente ([**CBaseAllocator :: m \_ lCount**](cbaseallocator-m-lcount.md)) et appelle la fonction [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) sur le sémaphore ([**CBaseAllocator :: m \_ hSem**](cbaseallocator-m-hsem.md)).</span><span class="sxs-lookup"><span data-stu-id="6e4b7-141">If the method needs to wait on a sample, it increments the count of waiting objects ([**CBaseAllocator::m\_lCount**](cbaseallocator-m-lcount.md)) and the calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function on the semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)).</span></span> <span data-ttu-id="6e4b7-142">Quand un exemple est disponible, il appelle la méthode [**CBaseAllocator :: ReleaseBuffer**](cbaseallocator-releasebuffer.md) sur l’allocateur, ce qui augmente le nombre de sémaphores par **m \_ lCount** (libérant ainsi les threads en attente) et définit **m \_ lCount** sur zéro.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-142">When a sample becomes available, it calls the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method on the allocator, which increases the semaphore count by **m\_lCount** (thereby releasing the waiting threads) and sets **m\_lCount** back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e4b7-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e4b7-143">Requirements</span></span>



| <span data-ttu-id="6e4b7-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e4b7-144">Requirement</span></span> | <span data-ttu-id="6e4b7-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e4b7-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e4b7-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e4b7-146">Header</span></span><br/>  | <dl> <span data-ttu-id="6e4b7-147"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e4b7-147"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6e4b7-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6e4b7-148">Library</span></span><br/> | <dl> <span data-ttu-id="6e4b7-149"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6e4b7-149"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e4b7-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e4b7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e4b7-151">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="6e4b7-151">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

