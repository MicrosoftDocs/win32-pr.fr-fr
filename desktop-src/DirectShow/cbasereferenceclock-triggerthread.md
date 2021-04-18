---
description: La méthode TriggerThread sort le thread de travail qui gère la planification.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Méthode CBaseReferenceClock. TriggerThread (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543310"
---
# <a name="cbasereferenceclocktriggerthread-method"></a><span data-ttu-id="713af-103">Méthode CBaseReferenceClock. TriggerThread</span><span class="sxs-lookup"><span data-stu-id="713af-103">CBaseReferenceClock.TriggerThread method</span></span>

<span data-ttu-id="713af-104">La `TriggerThread` méthode sort du thread de travail qui gère la planification.</span><span class="sxs-lookup"><span data-stu-id="713af-104">The `TriggerThread` method wakes up the worker thread that handles scheduling.</span></span>

## <a name="syntax"></a><span data-ttu-id="713af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="713af-105">Syntax</span></span>


```C++
void TriggerThread();
```



## <a name="parameters"></a><span data-ttu-id="713af-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="713af-106">Parameters</span></span>

<span data-ttu-id="713af-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="713af-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="713af-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="713af-108">Return value</span></span>

<span data-ttu-id="713af-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="713af-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="713af-110">Notes</span><span class="sxs-lookup"><span data-stu-id="713af-110">Remarks</span></span>

<span data-ttu-id="713af-111">L’horloge utilise un thread de travail qui appelle la méthode [**CAMSchedule :: Advise**](camschedule-advise.md) aux moments opportuns.</span><span class="sxs-lookup"><span data-stu-id="713af-111">The clock uses a worker thread that calls the [**CAMSchedule::Advise**](camschedule-advise.md) method at appropriate times.</span></span> <span data-ttu-id="713af-112">La classe dérivée peut appeler `TriggerThread` pour réveiller le thread.</span><span class="sxs-lookup"><span data-stu-id="713af-112">The derived class can call `TriggerThread` to wake up the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="713af-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="713af-113">Requirements</span></span>



| <span data-ttu-id="713af-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="713af-114">Requirement</span></span> | <span data-ttu-id="713af-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="713af-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="713af-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="713af-116">Header</span></span><br/>  | <dl> <span data-ttu-id="713af-117"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="713af-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="713af-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="713af-118">Library</span></span><br/> | <dl> <span data-ttu-id="713af-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="713af-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="713af-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="713af-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="713af-121">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="713af-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




