---
description: La méthode GetPrivateTime récupère le temps réel à partir de l’horloge.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Méthode CBaseReferenceClock. GetPrivateTime (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543311"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a><span data-ttu-id="bc6cc-103">Méthode CBaseReferenceClock. GetPrivateTime</span><span class="sxs-lookup"><span data-stu-id="bc6cc-103">CBaseReferenceClock.GetPrivateTime method</span></span>

<span data-ttu-id="bc6cc-104">La `GetPrivateTime` méthode récupère le temps réel à partir de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-104">The `GetPrivateTime` method retrieves the real time from the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc6cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc6cc-105">Syntax</span></span>


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a><span data-ttu-id="bc6cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc6cc-106">Parameters</span></span>

<span data-ttu-id="bc6cc-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc6cc-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc6cc-108">Return value</span></span>

<span data-ttu-id="bc6cc-109">Retourne l’heure actuelle de l’horloge, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-109">Returns the current clock time, in 100-nanosecond units.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc6cc-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bc6cc-110">Remarks</span></span>

<span data-ttu-id="bc6cc-111">Cette méthode retourne le temps réel signalé par l’horloge.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-111">This method returns the real time reported by the clock.</span></span> <span data-ttu-id="bc6cc-112">Les appelants externes utilisent la méthode [**CBaseReferenceClock :: getTime**](cbasereferenceclock-gettime.md) , qui appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-112">External callers use the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method, which calls this method.</span></span> <span data-ttu-id="bc6cc-113">Contrairement à la méthode **getTime** , l’horloge interne est autorisée à revenir en arrière.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-113">Unlike the **GetTime** method, the internal clock is allowed to go backward.</span></span> <span data-ttu-id="bc6cc-114">Si cela se produit, la méthode **getTime** continue à retourner la dernière fois qu’elle a rapporté, jusqu’à ce que la `GetPrivateTime` méthode détecte.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-114">If that happens, the **GetTime** method continues to return the last time that it reported, until the `GetPrivateTime` method catches up.</span></span>

<span data-ttu-id="bc6cc-115">Cette méthode retourne l’heure système.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-115">This method returns the system time.</span></span> <span data-ttu-id="bc6cc-116">Substituez cette méthode si votre horloge obtient l’heure d’une autre source.</span><span class="sxs-lookup"><span data-stu-id="bc6cc-116">Override this method if your clock gets the time from another source.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc6cc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc6cc-117">Requirements</span></span>



| <span data-ttu-id="bc6cc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc6cc-118">Requirement</span></span> | <span data-ttu-id="bc6cc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc6cc-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6cc-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc6cc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bc6cc-121"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc6cc-121"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bc6cc-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc6cc-122">Library</span></span><br/> | <dl> <span data-ttu-id="bc6cc-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bc6cc-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc6cc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc6cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6cc-125">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="bc6cc-125">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




