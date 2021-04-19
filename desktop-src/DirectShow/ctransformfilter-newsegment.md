---
description: La méthode NewSegment avertit le filtre que les exemples de supports reçus après cet appel sont regroupés en tant que segment.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Méthode CTransformFilter. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543877"
---
# <a name="ctransformfilternewsegment-method"></a><span data-ttu-id="6a313-103">Méthode CTransformFilter. NewSegment</span><span class="sxs-lookup"><span data-stu-id="6a313-103">CTransformFilter.NewSegment method</span></span>

<span data-ttu-id="6a313-104">La `NewSegment` méthode notifie le filtre que les exemples de supports reçus après cet appel sont regroupés en tant que segment.</span><span class="sxs-lookup"><span data-stu-id="6a313-104">The `NewSegment` method notifies the filter that media samples received after this call are grouped as a segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a313-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a313-105">Syntax</span></span>


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="6a313-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a313-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a313-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="6a313-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6a313-108">Heure de début du segment, par rapport à la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="6a313-108">Start time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="6a313-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="6a313-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="6a313-110">Heure d’arrêt du segment, par rapport à la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="6a313-110">Stop time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="6a313-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="6a313-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="6a313-112">Vitesse à laquelle le segment doit être traité.</span><span class="sxs-lookup"><span data-stu-id="6a313-112">Rate at which the segment should be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a313-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a313-113">Return value</span></span>

<span data-ttu-id="6a313-114">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a313-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a313-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6a313-115">Remarks</span></span>

<span data-ttu-id="6a313-116">La méthode [**CTransformInputPin :: NewSegment**](ctransforminputpin-newsegment.md) du code confidentiel d’entrée appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6a313-116">The input pin's [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) method calls this method.</span></span> <span data-ttu-id="6a313-117">Cette méthode remet l' `NewSegment` appel à la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="6a313-117">This method delivers the `NewSegment` call to the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a313-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a313-118">Requirements</span></span>



| <span data-ttu-id="6a313-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a313-119">Requirement</span></span> | <span data-ttu-id="6a313-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a313-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a313-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a313-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6a313-122"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a313-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6a313-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a313-123">Library</span></span><br/> | <dl> <span data-ttu-id="6a313-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6a313-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a313-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a313-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a313-126">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="6a313-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




