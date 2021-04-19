---
description: 'La méthode NewSegment avertit le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment. Cette méthode implémente la méthode IPin :: NewSegment.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Méthode CTransformInputPin. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537105"
---
# <a name="ctransforminputpinnewsegment-method"></a><span data-ttu-id="01325-104">Méthode CTransformInputPin. NewSegment</span><span class="sxs-lookup"><span data-stu-id="01325-104">CTransformInputPin.NewSegment method</span></span>

<span data-ttu-id="01325-105">La `NewSegment` méthode notifie le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment.</span><span class="sxs-lookup"><span data-stu-id="01325-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="01325-106">Cette méthode implémente la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="01325-106">This method implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="01325-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01325-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="01325-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01325-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01325-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="01325-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="01325-110">Heure de début du segment.</span><span class="sxs-lookup"><span data-stu-id="01325-110">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="01325-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="01325-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="01325-112">Heure d’arrêt du segment.</span><span class="sxs-lookup"><span data-stu-id="01325-112">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="01325-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="01325-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="01325-114">Taux du segment.</span><span class="sxs-lookup"><span data-stu-id="01325-114">Rate of the segment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01325-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01325-115">Return value</span></span>

<span data-ttu-id="01325-116">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01325-116">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01325-117">Notes</span><span class="sxs-lookup"><span data-stu-id="01325-117">Remarks</span></span>

<span data-ttu-id="01325-118">Cette méthode remplace la méthode [**CBasePin :: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="01325-118">This method overrides the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span> <span data-ttu-id="01325-119">Elle appelle la méthode [**CTransformFilter :: NewSegment**](ctransformfilter-newsegment.md) du filtre pour remettre l’appel en aval.</span><span class="sxs-lookup"><span data-stu-id="01325-119">It calls the filter's [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="01325-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01325-120">Requirements</span></span>



| <span data-ttu-id="01325-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01325-121">Requirement</span></span> | <span data-ttu-id="01325-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="01325-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01325-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="01325-123">Header</span></span><br/>  | <dl> <span data-ttu-id="01325-124"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01325-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="01325-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01325-125">Library</span></span><br/> | <dl> <span data-ttu-id="01325-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="01325-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




