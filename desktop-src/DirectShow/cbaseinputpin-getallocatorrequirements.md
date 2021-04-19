---
description: La méthode GetAllocatorRequirements récupère les propriétés Allocator demandées par la broche d’entrée.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Méthode CBaseInputPin. GetAllocatorRequirements (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523526"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a><span data-ttu-id="b5d5a-103">Méthode CBaseInputPin. GetAllocatorRequirements</span><span class="sxs-lookup"><span data-stu-id="b5d5a-103">CBaseInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="b5d5a-104">La `GetAllocatorRequirements` méthode récupère les propriétés Allocator demandées par la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b5d5a-104">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d5a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5d5a-105">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="b5d5a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5d5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d5a-107">*pProps*</span><span class="sxs-lookup"><span data-stu-id="b5d5a-107">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="b5d5a-108">Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , qui est remplie avec les spécifications.</span><span class="sxs-lookup"><span data-stu-id="b5d5a-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d5a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5d5a-109">Return value</span></span>

<span data-ttu-id="b5d5a-110">Retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="b5d5a-110">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5d5a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b5d5a-111">Remarks</span></span>

<span data-ttu-id="b5d5a-112">Lorsqu’une broche de sortie Initialise un allocateur de mémoire, elle peut appeler cette méthode pour déterminer si la broche d’entrée a des exigences de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b5d5a-112">When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements.</span></span> <span data-ttu-id="b5d5a-113">Pour plus d’informations, consultez [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="b5d5a-113">For more information, see [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="b5d5a-114">L’implémentation de cette méthode est facultative.</span><span class="sxs-lookup"><span data-stu-id="b5d5a-114">Implementing this method is optional.</span></span> <span data-ttu-id="b5d5a-115">Si le filtre a des exigences spécifiques en matière d’alignement ou de préfixe, substituez cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b5d5a-115">If the filter has specific alignment or prefix requirements, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d5a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5d5a-116">Requirements</span></span>



| <span data-ttu-id="b5d5a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5d5a-117">Requirement</span></span> | <span data-ttu-id="b5d5a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5d5a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d5a-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5d5a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b5d5a-120"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5d5a-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b5d5a-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5d5a-121">Library</span></span><br/> | <dl> <span data-ttu-id="b5d5a-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b5d5a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d5a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5d5a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d5a-124">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="b5d5a-124">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




