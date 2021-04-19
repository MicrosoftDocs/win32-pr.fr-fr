---
description: La méthode Allocator récupère un pointeur vers l’allocateur de mémoire.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: CRendererInputPin. Allocator, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541146"
---
# <a name="crendererinputpinallocator-method"></a><span data-ttu-id="1c40d-103">CRendererInputPin. Allocator, méthode</span><span class="sxs-lookup"><span data-stu-id="1c40d-103">CRendererInputPin.Allocator method</span></span>

<span data-ttu-id="1c40d-104">La `Allocator` méthode récupère un pointeur vers l’allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1c40d-104">The `Allocator` method retrieves a pointer to the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c40d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c40d-105">Syntax</span></span>


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a><span data-ttu-id="1c40d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c40d-106">Parameters</span></span>

<span data-ttu-id="1c40d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c40d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c40d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c40d-108">Return value</span></span>

<span data-ttu-id="1c40d-109">Retourne un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="1c40d-109">Returns a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c40d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1c40d-110">Remarks</span></span>

<span data-ttu-id="1c40d-111">Cette méthode retourne la variable de membre [**CBaseInputPin :: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="1c40d-111">This method returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span> <span data-ttu-id="1c40d-112">La méthode n’incrémente pas le nombre de références sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="1c40d-112">The method does not increment the reference count on the interface.</span></span> <span data-ttu-id="1c40d-113">Cette méthode est strictement une méthode d’accesseur.</span><span class="sxs-lookup"><span data-stu-id="1c40d-113">This method is strictly an accessor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c40d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c40d-114">Requirements</span></span>



| <span data-ttu-id="1c40d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c40d-115">Requirement</span></span> | <span data-ttu-id="1c40d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c40d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c40d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c40d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1c40d-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c40d-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c40d-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1c40d-119">Library</span></span><br/> | <dl> <span data-ttu-id="1c40d-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c40d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c40d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c40d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c40d-122">**CRendererInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="1c40d-122">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




