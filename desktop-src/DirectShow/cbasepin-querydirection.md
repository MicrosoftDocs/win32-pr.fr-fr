---
description: 'La méthode QueryDirection récupère la direction du code confidentiel (entrée ou sortie). Cette méthode implémente la méthode IPin :: QueryDirection.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Méthode CBasePin. QueryDirection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543801"
---
# <a name="cbasepinquerydirection-method"></a><span data-ttu-id="2e4d0-104">Méthode CBasePin. QueryDirection</span><span class="sxs-lookup"><span data-stu-id="2e4d0-104">CBasePin.QueryDirection method</span></span>

<span data-ttu-id="2e4d0-105">La `QueryDirection` méthode récupère la direction du code confidentiel (entrée ou sortie).</span><span class="sxs-lookup"><span data-stu-id="2e4d0-105">The `QueryDirection` method retrieves the direction of the pin (input or output).</span></span> <span data-ttu-id="2e4d0-106">Cette méthode implémente la méthode [**IPIN :: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .</span><span class="sxs-lookup"><span data-stu-id="2e4d0-106">This method implements the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4d0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e4d0-107">Syntax</span></span>


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a><span data-ttu-id="2e4d0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e4d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e4d0-109">*pPinDir*</span><span class="sxs-lookup"><span data-stu-id="2e4d0-109">*pPinDir*</span></span> 
</dt> <dd>

<span data-ttu-id="2e4d0-110">Pointeur vers une variable qui reçoit un membre du type énuméré de [**\_ direction de l’épinglage**](/windows/win32/api/strmif/ne-strmif-pin_direction) .</span><span class="sxs-lookup"><span data-stu-id="2e4d0-110">Pointer to a variable that receives a member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e4d0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e4d0-111">Return value</span></span>

<span data-ttu-id="2e4d0-112">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="2e4d0-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e4d0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e4d0-113">Requirements</span></span>



| <span data-ttu-id="2e4d0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e4d0-114">Requirement</span></span> | <span data-ttu-id="2e4d0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e4d0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4d0-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e4d0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2e4d0-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e4d0-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2e4d0-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2e4d0-118">Library</span></span><br/> | <dl> <span data-ttu-id="2e4d0-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2e4d0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e4d0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e4d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e4d0-121">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="2e4d0-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




