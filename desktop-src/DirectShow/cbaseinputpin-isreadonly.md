---
description: Interroge si l’allocateur utilise des exemples de supports en lecture seule.
ms.assetid: 2cb692da-f030-4265-afe4-b1608b51fd47
title: CBaseInputPin. IsReadOnly, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93d1e7930631328a277ce7332f483ee264b2d525
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545590"
---
# <a name="cbaseinputpinisreadonly-method"></a><span data-ttu-id="338f3-103">CBaseInputPin. IsReadOnly, méthode</span><span class="sxs-lookup"><span data-stu-id="338f3-103">CBaseInputPin.IsReadOnly method</span></span>

<span data-ttu-id="338f3-104">Interroge si l’allocateur utilise des exemples de supports en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="338f3-104">Queries whether the allocator uses read-only media samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="338f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="338f3-105">Syntax</span></span>


```C++
BOOL IsReadOnly();
```



## <a name="parameters"></a><span data-ttu-id="338f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="338f3-106">Parameters</span></span>

<span data-ttu-id="338f3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="338f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="338f3-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="338f3-108">Return value</span></span>

<span data-ttu-id="338f3-109">Retourne la valeur de la variable membre [**CBaseInputPin :: m \_ bReadOnly**](cbaseinputpin-m-breadonly.md) .</span><span class="sxs-lookup"><span data-stu-id="338f3-109">Returns the value of the [**CBaseInputPin::m\_bReadOnly**](cbaseinputpin-m-breadonly.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="338f3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="338f3-110">Requirements</span></span>



| <span data-ttu-id="338f3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="338f3-111">Requirement</span></span> | <span data-ttu-id="338f3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="338f3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="338f3-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="338f3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="338f3-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="338f3-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="338f3-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="338f3-115">Library</span></span><br/> | <dl> <span data-ttu-id="338f3-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="338f3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="338f3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="338f3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338f3-118">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="338f3-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




