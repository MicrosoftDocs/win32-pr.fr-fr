---
description: La méthode EndOfStream est appelée une fois que l’objet remet le dernier échantillon. La classe dérivée doit implémenter cette méthode.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Méthode CPullPin. EndOfStream (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543285"
---
# <a name="cpullpinendofstream-method"></a><span data-ttu-id="f8c24-104">Méthode CPullPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="f8c24-104">CPullPin.EndOfStream method</span></span>

<span data-ttu-id="f8c24-105">La `EndOfStream` méthode est appelée une fois que l’objet remet le dernier échantillon.</span><span class="sxs-lookup"><span data-stu-id="f8c24-105">The `EndOfStream` method is called after the object delivers the last sample.</span></span> <span data-ttu-id="f8c24-106">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f8c24-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c24-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8c24-107">Syntax</span></span>


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a><span data-ttu-id="f8c24-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8c24-108">Parameters</span></span>

<span data-ttu-id="f8c24-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f8c24-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8c24-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8c24-110">Return value</span></span>

<span data-ttu-id="f8c24-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8c24-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c24-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f8c24-112">Remarks</span></span>

<span data-ttu-id="f8c24-113">Utilisez cette méthode pour appeler [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur chaque broche d’entrée en aval qui reçoit les données de cet objet.</span><span class="sxs-lookup"><span data-stu-id="f8c24-113">Use this method to call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="f8c24-114">Si la ou les broches de sortie de votre filtre dérivent de [**CBaseOutputPin**](cbaseoutputpin.md), appelez la méthode [**CBaseOutputPin ::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="f8c24-114">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c24-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8c24-115">Requirements</span></span>



| <span data-ttu-id="f8c24-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8c24-116">Requirement</span></span> | <span data-ttu-id="f8c24-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8c24-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c24-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8c24-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f8c24-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8c24-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="f8c24-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8c24-120">Library</span></span><br/> | <dl> <span data-ttu-id="f8c24-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f8c24-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8c24-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8c24-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c24-123">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="f8c24-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




