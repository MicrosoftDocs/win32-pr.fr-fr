---
description: La méthode ThrottleWait insère un point d’attente après chaque image.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Méthode CBaseVideoRenderer. ThrottleWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7408cfb011fa0fbbb223b6757ddb10ff9cbd357b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542233"
---
# <a name="cbasevideorendererthrottlewait-method"></a><span data-ttu-id="0256b-103">Méthode CBaseVideoRenderer. ThrottleWait</span><span class="sxs-lookup"><span data-stu-id="0256b-103">CBaseVideoRenderer.ThrottleWait method</span></span>

<span data-ttu-id="0256b-104">La `ThrottleWait` méthode insère un point d’attente après chaque image.</span><span class="sxs-lookup"><span data-stu-id="0256b-104">The `ThrottleWait` method inserts a wait period after each frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="0256b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0256b-105">Syntax</span></span>


```C++
void ThrottleWait();
```



## <a name="parameters"></a><span data-ttu-id="0256b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0256b-106">Parameters</span></span>

<span data-ttu-id="0256b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0256b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0256b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0256b-108">Return value</span></span>

<span data-ttu-id="0256b-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0256b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0256b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0256b-110">Remarks</span></span>

<span data-ttu-id="0256b-111">Cette fonction membre attend pendant une période de temps obtenue à partir du membre de données **m \_ trThrottle** .</span><span class="sxs-lookup"><span data-stu-id="0256b-111">This member function waits for a time period obtained from the **m\_trThrottle** data member.</span></span>

## <a name="requirements"></a><span data-ttu-id="0256b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0256b-112">Requirements</span></span>



| <span data-ttu-id="0256b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0256b-113">Requirement</span></span> | <span data-ttu-id="0256b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0256b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0256b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="0256b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0256b-116"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0256b-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0256b-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0256b-117">Library</span></span><br/> | <dl> <span data-ttu-id="0256b-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0256b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0256b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0256b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0256b-120">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="0256b-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




