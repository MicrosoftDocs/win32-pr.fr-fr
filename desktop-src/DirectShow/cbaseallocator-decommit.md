---
description: La méthode de dévalidation annule l’allocation. Cette méthode implémente la méthode IMemAllocator ::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: CBaseAllocator. decommit, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542594"
---
# <a name="cbaseallocatordecommit-method"></a><span data-ttu-id="c93dd-104">CBaseAllocator. decommit, méthode</span><span class="sxs-lookup"><span data-stu-id="c93dd-104">CBaseAllocator.Decommit method</span></span>

<span data-ttu-id="c93dd-105">La `Decommit` méthode annule la validation de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="c93dd-105">The `Decommit` method decommits the allocator.</span></span> <span data-ttu-id="c93dd-106">Cette méthode implémente la méthode [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .</span><span class="sxs-lookup"><span data-stu-id="c93dd-106">This method implements the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93dd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c93dd-107">Syntax</span></span>


```C++
HRESULT Decommit();
```



## <a name="parameters"></a><span data-ttu-id="c93dd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c93dd-108">Parameters</span></span>

<span data-ttu-id="c93dd-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c93dd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c93dd-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c93dd-110">Return value</span></span>

<span data-ttu-id="c93dd-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c93dd-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c93dd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c93dd-112">Remarks</span></span>

<span data-ttu-id="c93dd-113">Une fois cette méthode appelée, les appels à la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) échouent.</span><span class="sxs-lookup"><span data-stu-id="c93dd-113">After this method is called, calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method will fail.</span></span> <span data-ttu-id="c93dd-114">À mesure que des exemples sont publiés, ils sont retournés à la liste libre.</span><span class="sxs-lookup"><span data-stu-id="c93dd-114">As samples are released, they get returned to the free list.</span></span> <span data-ttu-id="c93dd-115">Lorsque le dernier échantillon est retourné, l’allocateur appelle la méthode [**CBaseAllocator :: Free**](cbaseallocator-free.md) , qui libère la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="c93dd-115">When the last sample is returned, the allocator calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method, which releases the allocated memory.</span></span> <span data-ttu-id="c93dd-116">(Dans la classe de base, **Free** est une méthode virtuelle pure.)</span><span class="sxs-lookup"><span data-stu-id="c93dd-116">(In the base class, **Free** is a pure virtual method.)</span></span>

<span data-ttu-id="c93dd-117">De plus, cette méthode libère tous les threads qui sont bloqués sur les appels **GetBuffer** .</span><span class="sxs-lookup"><span data-stu-id="c93dd-117">In addition, this method releases any threads that are blocked on **GetBuffer** calls.</span></span> <span data-ttu-id="c93dd-118">Les appels à **GetBuffer** échouent.</span><span class="sxs-lookup"><span data-stu-id="c93dd-118">The calls to **GetBuffer** fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93dd-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c93dd-119">Requirements</span></span>



| <span data-ttu-id="c93dd-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c93dd-120">Requirement</span></span> | <span data-ttu-id="c93dd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c93dd-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93dd-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c93dd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c93dd-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c93dd-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c93dd-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c93dd-124">Library</span></span><br/> | <dl> <span data-ttu-id="c93dd-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c93dd-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93dd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c93dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93dd-127">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="c93dd-127">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




