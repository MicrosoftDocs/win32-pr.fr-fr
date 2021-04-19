---
description: La méthode GetPinCount récupère le nombre de broches sur le filtre.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Méthode CTransformFilter. GetPinCount (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542694"
---
# <a name="ctransformfiltergetpincount-method"></a><span data-ttu-id="95a3c-103">Méthode CTransformFilter. GetPinCount</span><span class="sxs-lookup"><span data-stu-id="95a3c-103">CTransformFilter.GetPinCount method</span></span>

<span data-ttu-id="95a3c-104">La `GetPinCount` méthode récupère le nombre de broches sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="95a3c-104">The `GetPinCount` method retrieves the number of pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a3c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95a3c-105">Syntax</span></span>


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a><span data-ttu-id="95a3c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95a3c-106">Parameters</span></span>

<span data-ttu-id="95a3c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="95a3c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95a3c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95a3c-108">Return value</span></span>

<span data-ttu-id="95a3c-109">Retourne 2.</span><span class="sxs-lookup"><span data-stu-id="95a3c-109">Returns 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="95a3c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="95a3c-110">Remarks</span></span>

<span data-ttu-id="95a3c-111">Cette méthode remplace la méthode [**CBaseFilter :: GetPinCount**](cbasefilter-getpincount.md) .</span><span class="sxs-lookup"><span data-stu-id="95a3c-111">This method overrides the [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md) method.</span></span> <span data-ttu-id="95a3c-112">La classe **CTransformFilter** prend en charge exactement une broche d’entrée et une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="95a3c-112">The **CTransformFilter** class supports exactly one input pin and one output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a3c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95a3c-113">Requirements</span></span>



| <span data-ttu-id="95a3c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95a3c-114">Requirement</span></span> | <span data-ttu-id="95a3c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="95a3c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a3c-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="95a3c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="95a3c-117"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95a3c-117"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95a3c-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95a3c-118">Library</span></span><br/> | <dl> <span data-ttu-id="95a3c-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95a3c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a3c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95a3c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a3c-121">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="95a3c-121">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




