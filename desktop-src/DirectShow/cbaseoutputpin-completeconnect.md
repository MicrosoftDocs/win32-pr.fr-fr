---
description: La méthode CompleteConnect effectue une connexion à une broche d’entrée.
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Méthode CBaseOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4614e8531a21d88a1c2f4cfd75fcbe05a9210f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543820"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="4729f-103">Méthode CBaseOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="4729f-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="4729f-104">La `CompleteConnect` méthode termine une connexion à une broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4729f-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="4729f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4729f-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="4729f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4729f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4729f-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="4729f-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="4729f-108">Pointeur vers la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4729f-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4729f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4729f-109">Return value</span></span>

<span data-ttu-id="4729f-110">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4729f-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4729f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4729f-111">Remarks</span></span>

<span data-ttu-id="4729f-112">Cette méthode remplace la méthode [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="4729f-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="4729f-113">Elle appelle la méthode [**DecideAllocator**](cbaseoutputpin-decideallocator.md) , qui sélectionne l’allocateur de mémoire à utiliser pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="4729f-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="4729f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4729f-114">Requirements</span></span>



| <span data-ttu-id="4729f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4729f-115">Requirement</span></span> | <span data-ttu-id="4729f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4729f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4729f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="4729f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4729f-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4729f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4729f-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4729f-119">Library</span></span><br/> | <dl> <span data-ttu-id="4729f-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4729f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4729f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4729f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4729f-122">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="4729f-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




