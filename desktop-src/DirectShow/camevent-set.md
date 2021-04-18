---
description: La méthode Set signale l’événement.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: CAMEvent. Set, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528949"
---
# <a name="cameventset-method"></a><span data-ttu-id="9482e-103">CAMEvent. Set, méthode</span><span class="sxs-lookup"><span data-stu-id="9482e-103">CAMEvent.Set method</span></span>

<span data-ttu-id="9482e-104">La `Set` méthode signale l’événement.</span><span class="sxs-lookup"><span data-stu-id="9482e-104">The `Set` method signals the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="9482e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9482e-105">Syntax</span></span>


```C++
void Set();
```



## <a name="parameters"></a><span data-ttu-id="9482e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9482e-106">Parameters</span></span>

<span data-ttu-id="9482e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9482e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9482e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9482e-108">Return value</span></span>

<span data-ttu-id="9482e-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9482e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9482e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9482e-110">Remarks</span></span>

<span data-ttu-id="9482e-111">Le comportement varie selon que l’objet est un événement de réinitialisation automatique ou un événement de réinitialisation manuelle :</span><span class="sxs-lookup"><span data-stu-id="9482e-111">The behavior depends on whether the object is an auto-reset event or a manual-reset event:</span></span>

-   <span data-ttu-id="9482e-112">**Réinitialisation automatique**: si des threads attendent cet événement, un thread est libéré et l’événement est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="9482e-112">**Auto-reset**: If any threads are waiting on this event, one thread is released and the event is reset.</span></span> <span data-ttu-id="9482e-113">Si aucun thread n’attend cet événement, l’événement reste signalé.</span><span class="sxs-lookup"><span data-stu-id="9482e-113">If no threads are waiting on this event, the event remains signaled.</span></span>
-   <span data-ttu-id="9482e-114">**Réinitialisation manuelle**: tous les threads en attente de cet événement sont libérés.</span><span class="sxs-lookup"><span data-stu-id="9482e-114">**Manual-reset**: All the threads waiting on this event are released.</span></span> <span data-ttu-id="9482e-115">L’événement reste signalé.</span><span class="sxs-lookup"><span data-stu-id="9482e-115">The event remains signaled.</span></span>

## <a name="requirements"></a><span data-ttu-id="9482e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9482e-116">Requirements</span></span>



| <span data-ttu-id="9482e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9482e-117">Requirement</span></span> | <span data-ttu-id="9482e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9482e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9482e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="9482e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9482e-120"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9482e-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9482e-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9482e-121">Library</span></span><br/> | <dl> <span data-ttu-id="9482e-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9482e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9482e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9482e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9482e-124">**CAMEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="9482e-124">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




