---
description: 'Méthode CDynamicOutputPin. CompleteConnect : la méthode CompleteConnect effectue une connexion à une broche d’entrée.'
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
ms.openlocfilehash: 5fa15c84b9d9e0b686e17110c656b74161687705
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095737"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="9e857-103">Méthode CDynamicOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="9e857-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="9e857-104">La `CompleteConnect` méthode termine une connexion à une broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9e857-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e857-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e857-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="9e857-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e857-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="9e857-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="9e857-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9e857-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e857-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9e857-109">Return value</span></span>

<span data-ttu-id="9e857-110">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="9e857-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e857-111">Notes </span><span class="sxs-lookup"><span data-stu-id="9e857-111">Remarks</span></span>

<span data-ttu-id="9e857-112">Cette méthode remplace la méthode [**CBaseOutputPin :: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="9e857-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="9e857-113">Pour prendre en charge les reconnexions dynamiques, cette méthode valide l’allocateur si le filtre est actif.</span><span class="sxs-lookup"><span data-stu-id="9e857-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="9e857-114">Dans la classe de base, les connexions peuvent se produire uniquement lorsque le filtre est arrêté, de sorte que l’allocateur est toujours validé dans la méthode [**CBaseOutputPin :: active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="9e857-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e857-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e857-115">Requirements</span></span>



| <span data-ttu-id="9e857-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e857-116">Requirement</span></span> | <span data-ttu-id="9e857-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e857-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e857-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e857-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9e857-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e857-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9e857-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9e857-120">Library</span></span><br/> | <dl> <span data-ttu-id="9e857-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9e857-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e857-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e857-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e857-123">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="9e857-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




