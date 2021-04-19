---
description: 'La méthode GetPin récupère un code confidentiel. Cette méthode implémente la méthode CBaseFilter :: GetPin virtuelle pure.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Méthode CSource. GetPin (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542534"
---
# <a name="csourcegetpin-method"></a><span data-ttu-id="d27ee-104">Méthode CSource. GetPin</span><span class="sxs-lookup"><span data-stu-id="d27ee-104">CSource.GetPin method</span></span>

<span data-ttu-id="d27ee-105">La `GetPin` méthode récupère un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="d27ee-105">The `GetPin` method retrieves a pin.</span></span> <span data-ttu-id="d27ee-106">Cette méthode implémente la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="d27ee-106">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27ee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d27ee-107">Syntax</span></span>


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="d27ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d27ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27ee-109">*n*</span><span class="sxs-lookup"><span data-stu-id="d27ee-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="d27ee-110">Numéro du code confidentiel spécifié.</span><span class="sxs-lookup"><span data-stu-id="d27ee-110">Number of the specified pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27ee-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d27ee-111">Return value</span></span>

<span data-ttu-id="d27ee-112">Retourne le pointeur vers l’objet [**CBasePin**](cbasepin.md) qui implémente le code confidentiel, ou **null** si l’index est hors limites.</span><span class="sxs-lookup"><span data-stu-id="d27ee-112">Returns the pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the index is out of range.</span></span>

## <a name="requirements"></a><span data-ttu-id="d27ee-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d27ee-113">Requirements</span></span>



| <span data-ttu-id="d27ee-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d27ee-114">Requirement</span></span> | <span data-ttu-id="d27ee-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d27ee-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d27ee-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d27ee-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d27ee-117"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d27ee-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d27ee-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d27ee-118">Library</span></span><br/> | <dl> <span data-ttu-id="d27ee-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d27ee-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d27ee-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d27ee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27ee-121">**CSource, classe**</span><span class="sxs-lookup"><span data-stu-id="d27ee-121">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




