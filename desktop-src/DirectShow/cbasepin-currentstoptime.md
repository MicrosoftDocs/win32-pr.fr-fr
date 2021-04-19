---
description: 'La méthode CurrentStopTime récupère l’heure d’arrêt du segment, définie par la méthode CBasePin :: NewSegment.'
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Méthode CBasePin. CurrentStopTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542593"
---
# <a name="cbasepincurrentstoptime-method"></a><span data-ttu-id="a953a-103">Méthode CBasePin. CurrentStopTime</span><span class="sxs-lookup"><span data-stu-id="a953a-103">CBasePin.CurrentStopTime method</span></span>

<span data-ttu-id="a953a-104">La `CurrentStopTime` méthode récupère l’heure d’arrêt du segment, définie par la méthode [**CBasePin :: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="a953a-104">The `CurrentStopTime` method retrieves the segment stop time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a953a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a953a-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a><span data-ttu-id="a953a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a953a-106">Parameters</span></span>

<span data-ttu-id="a953a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a953a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a953a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a953a-108">Return value</span></span>

<span data-ttu-id="a953a-109">Retourne la valeur de [**CBasePin :: m \_ tStop**](cbasepin-m-tstop.md).</span><span class="sxs-lookup"><span data-stu-id="a953a-109">Returns the value of [**CBasePin::m\_tStop**](cbasepin-m-tstop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a953a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a953a-110">Requirements</span></span>



| <span data-ttu-id="a953a-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a953a-111">Requirement</span></span> | <span data-ttu-id="a953a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a953a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a953a-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="a953a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a953a-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a953a-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a953a-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a953a-115">Library</span></span><br/> | <dl> <span data-ttu-id="a953a-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a953a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a953a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a953a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a953a-118">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="a953a-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




