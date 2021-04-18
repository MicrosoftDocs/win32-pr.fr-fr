---
description: La méthode InitAllocator crée un allocateur de mémoire.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.Iniméthode tAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540649"
---
# <a name="cbaseoutputpininitallocator-method"></a><span data-ttu-id="6618b-103">CBaseOutputPin.Iniméthode tAllocator</span><span class="sxs-lookup"><span data-stu-id="6618b-103">CBaseOutputPin.InitAllocator method</span></span>

<span data-ttu-id="6618b-104">La `InitAllocator` méthode crée un allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="6618b-104">The `InitAllocator` method creates a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="6618b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6618b-105">Syntax</span></span>


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="6618b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6618b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6618b-107">*ppAlloc*</span><span class="sxs-lookup"><span data-stu-id="6618b-107">*ppAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="6618b-108">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="6618b-108">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6618b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6618b-109">Return value</span></span>

<span data-ttu-id="6618b-110">Retourne S \_ OK en cas de réussite, ou un code d’erreur de la fonction **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="6618b-110">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="6618b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6618b-111">Remarks</span></span>

<span data-ttu-id="6618b-112">Si la broche d’entrée ne fournit pas d’allocateur de mémoire, la méthode [**CBaseOutputPin ::D ecideallocator**](cbaseoutputpin-decideallocator.md) appelle cette méthode pour créer un allocateur.</span><span class="sxs-lookup"><span data-stu-id="6618b-112">If the input pin does not provide a memory allocator, the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls this method to create an allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="6618b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6618b-113">Requirements</span></span>



| <span data-ttu-id="6618b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6618b-114">Requirement</span></span> | <span data-ttu-id="6618b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6618b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6618b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6618b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6618b-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6618b-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6618b-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6618b-118">Library</span></span><br/> | <dl> <span data-ttu-id="6618b-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6618b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6618b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6618b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6618b-121">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="6618b-121">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




