---
description: La méthode Advise répartit toutes les demandes planifiées pour une heure spécifiée ou antérieure.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: CAMSchedule. Advise, méthode (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543808"
---
# <a name="camscheduleadvise-method"></a><span data-ttu-id="63d79-103">CAMSchedule. Advise, méthode</span><span class="sxs-lookup"><span data-stu-id="63d79-103">CAMSchedule.Advise method</span></span>

<span data-ttu-id="63d79-104">La `Advise` méthode distribue toutes les demandes planifiées pour une heure spécifiée ou antérieure.</span><span class="sxs-lookup"><span data-stu-id="63d79-104">The `Advise` method dispatches all requests that are scheduled for a specified time or earlier.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d79-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63d79-105">Syntax</span></span>


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a><span data-ttu-id="63d79-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63d79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d79-107">*rtTime* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="63d79-107">*rtTime* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="63d79-108">Valeur qui spécifie le temps de référence actuel.</span><span class="sxs-lookup"><span data-stu-id="63d79-108">Value that specifies the current reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d79-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63d79-109">Return value</span></span>

<span data-ttu-id="63d79-110">Retourne le temps de référence de la prochaine demande de notification planifiée, ou le \_ temps maximal s’il n’y en a aucun.</span><span class="sxs-lookup"><span data-stu-id="63d79-110">Returns the reference time of the next scheduled advise request, or MAX\_TIME if there are none left.</span></span>

## <a name="remarks"></a><span data-ttu-id="63d79-111">Notes</span><span class="sxs-lookup"><span data-stu-id="63d79-111">Remarks</span></span>

<span data-ttu-id="63d79-112">Quand l’horloge appelle cette méthode, elle spécifie le temps de référence actuel.</span><span class="sxs-lookup"><span data-stu-id="63d79-112">When the clock calls this method, it specifies the current reference time.</span></span> <span data-ttu-id="63d79-113">Le planificateur détermine les demandes de notification qui ont expiré, le cas échéant, et les distribue.</span><span class="sxs-lookup"><span data-stu-id="63d79-113">The scheduler determines which advise requests have expired, if any, and dispatches them.</span></span> <span data-ttu-id="63d79-114">Si une demande d’une seule capture expire, le planificateur la supprime.</span><span class="sxs-lookup"><span data-stu-id="63d79-114">If a one-shot request expires, the scheduler deletes it.</span></span> <span data-ttu-id="63d79-115">En cas d’expiration d’une demande périodique, le planificateur la replanifie pour la prochaine notification.</span><span class="sxs-lookup"><span data-stu-id="63d79-115">If a periodic request expires, the scheduler re-schedules it for the next advise time.</span></span> <span data-ttu-id="63d79-116">La méthode retourne l’heure de la demande en attente suivante.</span><span class="sxs-lookup"><span data-stu-id="63d79-116">The method returns the time of the next pending request.</span></span>

<span data-ttu-id="63d79-117">Pour distribuer une demande de notification, le planificateur signale l’événement ou le sémaphore donné dans le paramètre *hNotify* de la méthode [**CAMSchedule :: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="63d79-117">To dispatch an advise request, the scheduler signals the event or semaphore given in the *hNotify* parameter of the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d79-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63d79-118">Requirements</span></span>



| <span data-ttu-id="63d79-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63d79-119">Requirement</span></span> | <span data-ttu-id="63d79-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="63d79-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d79-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="63d79-121">Header</span></span><br/>  | <dl> <span data-ttu-id="63d79-122"><dt>Dsschedule. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63d79-122"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="63d79-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63d79-123">Library</span></span><br/> | <dl> <span data-ttu-id="63d79-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63d79-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63d79-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63d79-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d79-126">**CAMSchedule, classe**</span><span class="sxs-lookup"><span data-stu-id="63d79-126">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




