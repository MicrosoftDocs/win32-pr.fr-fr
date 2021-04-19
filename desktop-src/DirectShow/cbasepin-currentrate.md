---
description: 'La méthode CurrentRate récupère la vitesse du segment, définie par la méthode CBasePin :: NewSegment.'
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: Méthode CBasePin. CurrentRate (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: adffcc02aad4c5516a8e92c247e47b7dbf389d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545347"
---
# <a name="cbasepincurrentrate-method"></a><span data-ttu-id="20aac-103">Méthode CBasePin. CurrentRate</span><span class="sxs-lookup"><span data-stu-id="20aac-103">CBasePin.CurrentRate method</span></span>

<span data-ttu-id="20aac-104">La `CurrentRate` méthode récupère la vitesse du segment, définie par la méthode [**CBasePin :: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="20aac-104">The `CurrentRate` method retrieves the segment rate, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20aac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20aac-105">Syntax</span></span>


```C++
double CurrentRate();
```



## <a name="parameters"></a><span data-ttu-id="20aac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20aac-106">Parameters</span></span>

<span data-ttu-id="20aac-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="20aac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20aac-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20aac-108">Return value</span></span>

<span data-ttu-id="20aac-109">Retourne la valeur de [**CBasePin :: m \_ dRate**](cbasepin-m-drate.md).</span><span class="sxs-lookup"><span data-stu-id="20aac-109">Returns the value of [**CBasePin::m\_dRate**](cbasepin-m-drate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20aac-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20aac-110">Requirements</span></span>



| <span data-ttu-id="20aac-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20aac-111">Requirement</span></span> | <span data-ttu-id="20aac-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="20aac-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20aac-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="20aac-113">Header</span></span><br/>  | <dl> <span data-ttu-id="20aac-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20aac-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="20aac-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20aac-115">Library</span></span><br/> | <dl> <span data-ttu-id="20aac-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="20aac-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20aac-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20aac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20aac-118">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="20aac-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




