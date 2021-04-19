---
description: La méthode DeliverNewSegment fournit une notification de nouveau segment à la broche d’entrée connectée.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Méthode CBaseOutputPin. DeliverNewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541707"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a><span data-ttu-id="a6e71-103">Méthode CBaseOutputPin. DeliverNewSegment</span><span class="sxs-lookup"><span data-stu-id="a6e71-103">CBaseOutputPin.DeliverNewSegment method</span></span>

<span data-ttu-id="a6e71-104">La `DeliverNewSegment` méthode fournit une notification de nouveau segment à la broche d’entrée connectée.</span><span class="sxs-lookup"><span data-stu-id="a6e71-104">The `DeliverNewSegment` method delivers a new-segment notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6e71-105">Syntax</span></span>


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="a6e71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6e71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6e71-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="a6e71-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e71-108">Position du média de départ du segment, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="a6e71-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="a6e71-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="a6e71-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e71-110">Position du média de fin du segment, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="a6e71-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="a6e71-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="a6e71-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="a6e71-112">Taux auquel ce segment doit être traité, sous la forme d’un pourcentage du taux d’origine.</span><span class="sxs-lookup"><span data-stu-id="a6e71-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6e71-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6e71-113">Return value</span></span>

<span data-ttu-id="a6e71-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6e71-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a6e71-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6e71-115">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="a6e71-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a6e71-116">Return code</span></span>                                                                                           | <span data-ttu-id="a6e71-117">Description</span><span class="sxs-lookup"><span data-stu-id="a6e71-117">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a6e71-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6e71-118"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a6e71-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="a6e71-119">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="a6e71-120"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="a6e71-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a6e71-121">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="a6e71-121">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6e71-122">Notes</span><span class="sxs-lookup"><span data-stu-id="a6e71-122">Remarks</span></span>

<span data-ttu-id="a6e71-123">Cette méthode appelle la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a6e71-123">This method calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6e71-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6e71-124">Requirements</span></span>



| <span data-ttu-id="a6e71-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6e71-125">Requirement</span></span> | <span data-ttu-id="a6e71-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6e71-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e71-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6e71-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a6e71-128"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6e71-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a6e71-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a6e71-129">Library</span></span><br/> | <dl> <span data-ttu-id="a6e71-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a6e71-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6e71-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6e71-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6e71-132">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="a6e71-132">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




