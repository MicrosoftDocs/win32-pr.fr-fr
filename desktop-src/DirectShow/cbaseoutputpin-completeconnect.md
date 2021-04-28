---
description: 'Méthode CBaseOutputPin. CompleteConnect : la méthode CompleteConnect effectue une connexion à une broche d’entrée.'
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
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099537"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="fe2e4-103">Méthode CBaseOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="fe2e4-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="fe2e4-104">La `CompleteConnect` méthode termine une connexion à une broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fe2e4-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe2e4-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="fe2e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe2e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe2e4-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="fe2e4-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="fe2e4-108">Pointeur vers la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fe2e4-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe2e4-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fe2e4-109">Return value</span></span>

<span data-ttu-id="fe2e4-110">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="fe2e4-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe2e4-111">Notes </span><span class="sxs-lookup"><span data-stu-id="fe2e4-111">Remarks</span></span>

<span data-ttu-id="fe2e4-112">Cette méthode remplace la méthode [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="fe2e4-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="fe2e4-113">Elle appelle la méthode [**DecideAllocator**](cbaseoutputpin-decideallocator.md) , qui sélectionne l’allocateur de mémoire à utiliser pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="fe2e4-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe2e4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe2e4-114">Requirements</span></span>



| <span data-ttu-id="fe2e4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe2e4-115">Requirement</span></span> | <span data-ttu-id="fe2e4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe2e4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2e4-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe2e4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fe2e4-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe2e4-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fe2e4-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fe2e4-119">Library</span></span><br/> | <dl> <span data-ttu-id="fe2e4-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fe2e4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe2e4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe2e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2e4-122">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="fe2e4-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




