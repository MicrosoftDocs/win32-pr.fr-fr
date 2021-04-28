---
description: 'Méthode CBaseFilter. GetPinCount : la méthode GetPinCount récupère le nombre de broches.'
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Méthode CBaseFilter. GetPinCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099787"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="d630c-103">Méthode CBaseFilter. GetPinCount</span><span class="sxs-lookup"><span data-stu-id="d630c-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="d630c-104">La `GetPinCount` méthode récupère le nombre de broches.</span><span class="sxs-lookup"><span data-stu-id="d630c-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="d630c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d630c-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="d630c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d630c-106">Parameters</span></span>

<span data-ttu-id="d630c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d630c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d630c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d630c-108">Return value</span></span>

<span data-ttu-id="d630c-109">Retourne le nombre de broches.</span><span class="sxs-lookup"><span data-stu-id="d630c-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="d630c-110">Notes </span><span class="sxs-lookup"><span data-stu-id="d630c-110">Remarks</span></span>

<span data-ttu-id="d630c-111">La classe dérivée doit implémenter cette méthode virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="d630c-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="d630c-112">Retourne le nombre de codes confidentiels actuellement disponibles sur ce filtre.</span><span class="sxs-lookup"><span data-stu-id="d630c-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="d630c-113">Les filtres peuvent créer ou détruire dynamiquement des broches.</span><span class="sxs-lookup"><span data-stu-id="d630c-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="d630c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d630c-114">Requirements</span></span>



| <span data-ttu-id="d630c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d630c-115">Requirement</span></span> | <span data-ttu-id="d630c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d630c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d630c-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d630c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d630c-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d630c-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d630c-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d630c-119">Library</span></span><br/> | <dl> <span data-ttu-id="d630c-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d630c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d630c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d630c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d630c-122">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="d630c-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




