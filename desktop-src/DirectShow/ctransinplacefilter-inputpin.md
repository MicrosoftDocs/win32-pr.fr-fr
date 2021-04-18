---
description: La méthode InputPin récupère un pointeur vers la broche d’entrée du filtre.
ms.assetid: 533a962e-225d-4f10-a9c3-1464bea512ba
title: Méthode CTransInPlaceFilter. InputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.InputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b92775eca87a88659326aa5b34eb0c15109ed8a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532995"
---
# <a name="ctransinplacefilterinputpin-method"></a><span data-ttu-id="60728-103">Méthode CTransInPlaceFilter. InputPin</span><span class="sxs-lookup"><span data-stu-id="60728-103">CTransInPlaceFilter.InputPin method</span></span>

<span data-ttu-id="60728-104">La `InputPin` méthode récupère un pointeur vers la broche d’entrée du filtre.</span><span class="sxs-lookup"><span data-stu-id="60728-104">The `InputPin` method retrieves a pointer to the filter's input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="60728-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60728-105">Syntax</span></span>


```C++
CTransInPlaceInputPin* InputPin();
```



## <a name="parameters"></a><span data-ttu-id="60728-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60728-106">Parameters</span></span>

<span data-ttu-id="60728-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="60728-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60728-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60728-108">Return value</span></span>

<span data-ttu-id="60728-109">Retourne la variable de membre [**CTransformFilter :: m \_ pInput**](ctransformfilter-m-pinput.md) .</span><span class="sxs-lookup"><span data-stu-id="60728-109">Returns the [**CTransformFilter::m\_pInput**](ctransformfilter-m-pinput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="60728-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60728-110">Requirements</span></span>



| <span data-ttu-id="60728-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60728-111">Requirement</span></span> | <span data-ttu-id="60728-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="60728-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60728-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="60728-113">Header</span></span><br/>  | <dl> <span data-ttu-id="60728-114"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60728-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="60728-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="60728-115">Library</span></span><br/> | <dl> <span data-ttu-id="60728-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60728-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60728-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60728-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60728-118">**CTransInPlaceFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="60728-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




