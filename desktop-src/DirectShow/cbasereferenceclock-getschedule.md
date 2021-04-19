---
description: La méthode GetSchedule récupère un pointeur vers l’objet de planification de l’horloge.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: Méthode CBaseReferenceClock. GetSchedule (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a37cdb3e18f3ab71b144af071233aee5a6a3a93d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528460"
---
# <a name="cbasereferenceclockgetschedule-method"></a><span data-ttu-id="44554-103">Méthode CBaseReferenceClock. GetSchedule</span><span class="sxs-lookup"><span data-stu-id="44554-103">CBaseReferenceClock.GetSchedule method</span></span>

<span data-ttu-id="44554-104">La `GetSchedule` méthode récupère un pointeur vers l’objet de planification de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="44554-104">The `GetSchedule` method retrieves a pointer to the clock's scheduling object.</span></span>

## <a name="syntax"></a><span data-ttu-id="44554-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44554-105">Syntax</span></span>


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a><span data-ttu-id="44554-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44554-106">Parameters</span></span>

<span data-ttu-id="44554-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="44554-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44554-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44554-108">Return value</span></span>

<span data-ttu-id="44554-109">Retourne la variable de membre [**CBaseReferenceClock :: m \_ pSchedule**](cbasereferenceclock-m-pschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="44554-109">Returns the [**CBaseReferenceClock::m\_pSchedule**](cbasereferenceclock-m-pschedule.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="44554-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44554-110">Requirements</span></span>



| <span data-ttu-id="44554-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44554-111">Requirement</span></span> | <span data-ttu-id="44554-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="44554-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44554-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="44554-113">Header</span></span><br/>  | <dl> <span data-ttu-id="44554-114"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44554-114"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="44554-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="44554-115">Library</span></span><br/> | <dl> <span data-ttu-id="44554-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="44554-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44554-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44554-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44554-118">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="44554-118">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




