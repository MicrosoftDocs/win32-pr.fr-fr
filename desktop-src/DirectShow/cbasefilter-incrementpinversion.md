---
description: La méthode IncremementPinVersion incrémente le numéro de version sur le jeu de broches.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Méthode CBaseFilter. IncrementPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541447"
---
# <a name="cbasefilterincrementpinversion-method"></a><span data-ttu-id="d40ec-103">Méthode CBaseFilter. IncrementPinVersion</span><span class="sxs-lookup"><span data-stu-id="d40ec-103">CBaseFilter.IncrementPinVersion method</span></span>

<span data-ttu-id="d40ec-104">La `IncremementPinVersion` méthode incrémente le numéro de version sur le jeu de broches.</span><span class="sxs-lookup"><span data-stu-id="d40ec-104">The `IncremementPinVersion` method increments the version number on the set of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="d40ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d40ec-105">Syntax</span></span>


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="d40ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d40ec-106">Parameters</span></span>

<span data-ttu-id="d40ec-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d40ec-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d40ec-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d40ec-108">Return value</span></span>

<span data-ttu-id="d40ec-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d40ec-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d40ec-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d40ec-110">Remarks</span></span>

<span data-ttu-id="d40ec-111">Cette méthode incrémente la variable membre [**CBaseFilter :: m \_ PinVersion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="d40ec-111">This method increments the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span> <span data-ttu-id="d40ec-112">Si le filtre crée ou détruit dynamiquement des codes confidentiels, appelez cette méthode chaque fois que les codes confidentiels changent.</span><span class="sxs-lookup"><span data-stu-id="d40ec-112">If the filter dynamically creates or destroys pins, call this method whenever the pins change.</span></span>

## <a name="requirements"></a><span data-ttu-id="d40ec-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d40ec-113">Requirements</span></span>



| <span data-ttu-id="d40ec-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d40ec-114">Requirement</span></span> | <span data-ttu-id="d40ec-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d40ec-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d40ec-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d40ec-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d40ec-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d40ec-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d40ec-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d40ec-118">Library</span></span><br/> | <dl> <span data-ttu-id="d40ec-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d40ec-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d40ec-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d40ec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d40ec-121">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="d40ec-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="d40ec-122">**CBaseFilter::GetPinVersion**</span><span class="sxs-lookup"><span data-stu-id="d40ec-122">**CBaseFilter::GetPinVersion**</span></span>](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




