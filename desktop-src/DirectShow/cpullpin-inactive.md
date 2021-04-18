---
description: La méthode inactive arrête le thread de travail qui extrait les données de la broche de sortie. Cette méthode annule également l’allocation.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: CPullPin. inactive, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533171"
---
# <a name="cpullpininactive-method"></a><span data-ttu-id="8d5c2-104">CPullPin. inactive, méthode</span><span class="sxs-lookup"><span data-stu-id="8d5c2-104">CPullPin.Inactive method</span></span>

<span data-ttu-id="8d5c2-105">La `Inactive` méthode arrête le thread de travail qui extrait les données de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-105">The `Inactive` method shuts down the worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="8d5c2-106">Cette méthode annule également l’allocation.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-106">This method also decommits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d5c2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d5c2-107">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="8d5c2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d5c2-108">Parameters</span></span>

<span data-ttu-id="8d5c2-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d5c2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d5c2-110">Return value</span></span>

<span data-ttu-id="8d5c2-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5c2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8d5c2-112">Remarks</span></span>

<span data-ttu-id="8d5c2-113">Appelez cette méthode lorsque le filtre propriétaire devient inactif.</span><span class="sxs-lookup"><span data-stu-id="8d5c2-113">Call this method when the owning filter becomes inactive.</span></span> <span data-ttu-id="8d5c2-114">(Si votre broche d’entrée dérive de [**CBasePin**](cbasepin.md), remplacez la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) .)</span><span class="sxs-lookup"><span data-stu-id="8d5c2-114">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Inactive**](cbasepin-inactive.md) method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5c2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d5c2-115">Requirements</span></span>



| <span data-ttu-id="8d5c2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d5c2-116">Requirement</span></span> | <span data-ttu-id="8d5c2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d5c2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5c2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d5c2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8d5c2-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d5c2-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="8d5c2-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d5c2-120">Library</span></span><br/> | <dl> <span data-ttu-id="8d5c2-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8d5c2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d5c2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d5c2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d5c2-123">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="8d5c2-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




