---
description: 'La méthode CurrentStartTime récupère l’heure de début du segment, définie par la méthode CBasePin :: NewSegment.'
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Méthode CBasePin. CurrentStartTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544496"
---
# <a name="cbasepincurrentstarttime-method"></a><span data-ttu-id="adcf2-103">Méthode CBasePin. CurrentStartTime</span><span class="sxs-lookup"><span data-stu-id="adcf2-103">CBasePin.CurrentStartTime method</span></span>

<span data-ttu-id="adcf2-104">La `CurrentStartTime` méthode récupère l’heure de début du segment, définie par la méthode [**CBasePin :: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="adcf2-104">The `CurrentStartTime` method retrieves the segment start time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="adcf2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adcf2-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a><span data-ttu-id="adcf2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adcf2-106">Parameters</span></span>

<span data-ttu-id="adcf2-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="adcf2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="adcf2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adcf2-108">Return value</span></span>

<span data-ttu-id="adcf2-109">Retourne la valeur de [**CBasePin :: m \_ tStart**](cbasepin-m-tstart.md).</span><span class="sxs-lookup"><span data-stu-id="adcf2-109">Returns the value of [**CBasePin::m\_tStart**](cbasepin-m-tstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="adcf2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adcf2-110">Requirements</span></span>



| <span data-ttu-id="adcf2-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adcf2-111">Requirement</span></span> | <span data-ttu-id="adcf2-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="adcf2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adcf2-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="adcf2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="adcf2-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adcf2-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="adcf2-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adcf2-115">Library</span></span><br/> | <dl> <span data-ttu-id="adcf2-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="adcf2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adcf2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adcf2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adcf2-118">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="adcf2-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




