---
description: 'La méthode SetProperties spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon. Cette méthode implémente la méthode IMemAllocator :: SetProperties.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: CBaseAllocator. SetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535343"
---
# <a name="cbaseallocatorsetproperties-method"></a><span data-ttu-id="66c70-104">CBaseAllocator. SetProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="66c70-104">CBaseAllocator.SetProperties method</span></span>

<span data-ttu-id="66c70-105">La `SetProperties` méthode spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="66c70-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="66c70-106">Cette méthode implémente la méthode [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) .</span><span class="sxs-lookup"><span data-stu-id="66c70-106">This method implements the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c70-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66c70-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="66c70-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66c70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c70-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="66c70-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="66c70-110">Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient les exigences de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="66c70-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="66c70-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="66c70-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="66c70-112">Pointeur vers une structure de **\_ Propriétés Allocator** qui reçoit les propriétés de mémoire tampon réelles.</span><span class="sxs-lookup"><span data-stu-id="66c70-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66c70-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66c70-113">Return value</span></span>

<span data-ttu-id="66c70-114">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="66c70-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="66c70-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="66c70-115">Return code</span></span>                                                                                                 | <span data-ttu-id="66c70-116">Description</span><span class="sxs-lookup"><span data-stu-id="66c70-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="66c70-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66c70-117"><dt>**S\_OK**</dt></span></span> </dl>                        | <span data-ttu-id="66c70-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="66c70-118">Success.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="66c70-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="66c70-119"><dt>**E\_POINTER**</dt></span></span> </dl>                   | <span data-ttu-id="66c70-120">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="66c70-120">**NULL** pointer argument.</span></span><br/>                                 |
| <dl> <span data-ttu-id="66c70-121"><dt>**VFW \_ E \_ déjà \_ validé**</dt></span><span class="sxs-lookup"><span data-stu-id="66c70-121"><dt>**VFW\_E\_ALREADY\_COMMITTED**</dt></span></span> </dl>   | <span data-ttu-id="66c70-122">Impossible de modifier la mémoire allouée lorsque le filtre est actif.</span><span class="sxs-lookup"><span data-stu-id="66c70-122">Cannot change allocated memory while the filter is active.</span></span><br/> |
| <dl> <span data-ttu-id="66c70-123"><dt>**VFW \_ E \_ BADALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="66c70-123"><dt>**VFW\_E\_BADALIGN**</dt></span></span> </dl>             | <span data-ttu-id="66c70-124">Un alignement non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="66c70-124">An invalid alignment was specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="66c70-125"><dt>**\_ \_ mémoires tampons VFW E en \_ suspens**</dt></span><span class="sxs-lookup"><span data-stu-id="66c70-125"><dt>**VFW\_E\_BUFFERS\_OUTSTANDING**</dt></span></span> </dl> | <span data-ttu-id="66c70-126">Une ou plusieurs mémoires tampons sont toujours actives.</span><span class="sxs-lookup"><span data-stu-id="66c70-126">One or more buffers are still active.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="66c70-127">Notes</span><span class="sxs-lookup"><span data-stu-id="66c70-127">Remarks</span></span>

<span data-ttu-id="66c70-128">Cette méthode spécifie les spécifications de mémoire tampon, mais n’alloue pas de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="66c70-128">This method specifies the buffer requirements, but does not allocate any buffers.</span></span> <span data-ttu-id="66c70-129">Appelez la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) pour allouer des tampons.</span><span class="sxs-lookup"><span data-stu-id="66c70-129">Call the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method to allocate buffers.</span></span>

<span data-ttu-id="66c70-130">L’appelant alloue deux structures de propriétés d’allocateur \_ .</span><span class="sxs-lookup"><span data-stu-id="66c70-130">The caller allocates two ALLOCATOR\_PROPERTIES structures.</span></span> <span data-ttu-id="66c70-131">Le paramètre *pRequest* contient les exigences de mémoire tampon de l’appelant, y compris le nombre de mémoires tampons et la taille de chaque mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="66c70-131">The *pRequest* parameter contains the caller's buffer requirements, including the number of buffers and the size of each buffer.</span></span> <span data-ttu-id="66c70-132">Lorsque la méthode est retournée, le paramètre *pActual* contient les propriétés de mémoire tampon réelles, telles qu’elles sont définies par l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="66c70-132">When the method returns, the *pActual* parameter contains the actual buffer properties, as set by the allocator.</span></span> <span data-ttu-id="66c70-133">Dans la classe de base, en supposant que la méthode aboutisse, les propriétés réelles correspondent toujours aux propriétés demandées.</span><span class="sxs-lookup"><span data-stu-id="66c70-133">In the base class, assuming that the method succeeds, the actual properties always match the requested properties.</span></span> <span data-ttu-id="66c70-134">Les classes dérivées peuvent substituer ce comportement.</span><span class="sxs-lookup"><span data-stu-id="66c70-134">Derived classes might override this behavior.</span></span>

<span data-ttu-id="66c70-135">L’allocateur ne doit pas être validé et ne doit pas avoir de tampons en suspens.</span><span class="sxs-lookup"><span data-stu-id="66c70-135">The allocator must not be committed, and must not have outstanding buffers.</span></span> <span data-ttu-id="66c70-136">Dans la classe de base, l’alignement doit être égal à 1.</span><span class="sxs-lookup"><span data-stu-id="66c70-136">In the base class, the alignment must equal 1.</span></span> <span data-ttu-id="66c70-137">La classe [**CMemAllocator**](cmemallocator.md) remplace cette exigence.</span><span class="sxs-lookup"><span data-stu-id="66c70-137">The [**CMemAllocator**](cmemallocator.md) class overrides this requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="66c70-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66c70-138">Requirements</span></span>



| <span data-ttu-id="66c70-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66c70-139">Requirement</span></span> | <span data-ttu-id="66c70-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="66c70-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66c70-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="66c70-141">Header</span></span><br/>  | <dl> <span data-ttu-id="66c70-142"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66c70-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66c70-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66c70-143">Library</span></span><br/> | <dl> <span data-ttu-id="66c70-144"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66c70-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66c70-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66c70-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c70-146">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="66c70-146">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




