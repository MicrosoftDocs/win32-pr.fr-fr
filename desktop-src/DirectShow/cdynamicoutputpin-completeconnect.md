---
description: La méthode CompleteConnect effectue une connexion à une broche d’entrée.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Méthode CDynamicOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31afa592701b881d39ab4948514aacfe50b345b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540696"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="d5161-103">Méthode CDynamicOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="d5161-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="d5161-104">La `CompleteConnect` méthode termine une connexion à une broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d5161-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5161-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5161-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="d5161-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5161-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5161-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="d5161-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="d5161-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d5161-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5161-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5161-109">Return value</span></span>

<span data-ttu-id="d5161-110">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="d5161-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5161-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d5161-111">Remarks</span></span>

<span data-ttu-id="d5161-112">Cette méthode remplace la méthode [**CBaseOutputPin :: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="d5161-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="d5161-113">Pour prendre en charge les reconnexions dynamiques, cette méthode valide l’allocateur si le filtre est actif.</span><span class="sxs-lookup"><span data-stu-id="d5161-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="d5161-114">Dans la classe de base, les connexions peuvent se produire uniquement lorsque le filtre est arrêté, de sorte que l’allocateur est toujours validé dans la méthode [**CBaseOutputPin :: active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="d5161-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5161-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5161-115">Requirements</span></span>



| <span data-ttu-id="d5161-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5161-116">Requirement</span></span> | <span data-ttu-id="d5161-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5161-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5161-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5161-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d5161-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5161-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5161-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5161-120">Library</span></span><br/> | <dl> <span data-ttu-id="d5161-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d5161-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5161-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5161-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5161-123">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="d5161-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




