---
description: La méthode Duration récupère la durée du flux.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: CPullPin. Duration, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526387"
---
# <a name="cpullpinduration-method"></a><span data-ttu-id="dc689-103">CPullPin. Duration, méthode</span><span class="sxs-lookup"><span data-stu-id="dc689-103">CPullPin.Duration method</span></span>

<span data-ttu-id="dc689-104">La `Duration` méthode récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="dc689-104">The `Duration` method retrieves the duration of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc689-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc689-105">Syntax</span></span>


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a><span data-ttu-id="dc689-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc689-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc689-107">*ptDuration*</span><span class="sxs-lookup"><span data-stu-id="dc689-107">*ptDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="dc689-108">Pointeur vers une variable qui reçoit la durée, en octets multiplié par 10 millions.</span><span class="sxs-lookup"><span data-stu-id="dc689-108">Pointer to a variable that receives the duration, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc689-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc689-109">Return value</span></span>

<span data-ttu-id="dc689-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dc689-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc689-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dc689-111">Remarks</span></span>

<span data-ttu-id="dc689-112">La durée est indéterminée jusqu’à ce que la méthode [**CPullPin :: Connect**](cpullpin-connect.md) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="dc689-112">The duration is indeterminate until the [**CPullPin::Connect**](cpullpin-connect.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc689-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc689-113">Requirements</span></span>



| <span data-ttu-id="dc689-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc689-114">Requirement</span></span> | <span data-ttu-id="dc689-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc689-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc689-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc689-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dc689-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc689-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="dc689-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dc689-118">Library</span></span><br/> | <dl> <span data-ttu-id="dc689-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dc689-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc689-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc689-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc689-121">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="dc689-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




