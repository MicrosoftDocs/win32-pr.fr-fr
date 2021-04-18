---
description: La méthode DeliverEndOfStream fournit une notification de fin de flux à la broche d’entrée connectée.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Méthode CBaseOutputPin. DeliverEndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540650"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a><span data-ttu-id="dfce9-103">Méthode CBaseOutputPin. DeliverEndOfStream</span><span class="sxs-lookup"><span data-stu-id="dfce9-103">CBaseOutputPin.DeliverEndOfStream method</span></span>

<span data-ttu-id="dfce9-104">La `DeliverEndOfStream` méthode fournit une notification de fin de flux à la broche d’entrée connectée.</span><span class="sxs-lookup"><span data-stu-id="dfce9-104">The `DeliverEndOfStream` method delivers an end-of-stream notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfce9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfce9-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="dfce9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfce9-106">Parameters</span></span>

<span data-ttu-id="dfce9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dfce9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfce9-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfce9-108">Return value</span></span>

<span data-ttu-id="dfce9-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dfce9-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dfce9-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dfce9-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="dfce9-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dfce9-111">Return code</span></span>                                                                                           | <span data-ttu-id="dfce9-112">Description</span><span class="sxs-lookup"><span data-stu-id="dfce9-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dfce9-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dfce9-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="dfce9-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="dfce9-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="dfce9-115"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="dfce9-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="dfce9-116">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="dfce9-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfce9-117">Notes</span><span class="sxs-lookup"><span data-stu-id="dfce9-117">Remarks</span></span>

<span data-ttu-id="dfce9-118">Cette méthode appelle la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dfce9-118">This method calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfce9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfce9-119">Requirements</span></span>



| <span data-ttu-id="dfce9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfce9-120">Requirement</span></span> | <span data-ttu-id="dfce9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfce9-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfce9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfce9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="dfce9-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfce9-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dfce9-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dfce9-124">Library</span></span><br/> | <dl> <span data-ttu-id="dfce9-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dfce9-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfce9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfce9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfce9-127">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="dfce9-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




