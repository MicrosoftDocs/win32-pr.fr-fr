---
description: La méthode AddAdvisePacket ajoute une demande de notification à la liste des demandes en attente.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Méthode CAMSchedule. AddAdvisePacket (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525508"
---
# <a name="camscheduleaddadvisepacket-method"></a><span data-ttu-id="e1fc4-103">Méthode CAMSchedule. AddAdvisePacket</span><span class="sxs-lookup"><span data-stu-id="e1fc4-103">CAMSchedule.AddAdvisePacket method</span></span>

<span data-ttu-id="e1fc4-104">La `AddAdvisePacket` méthode ajoute une demande de notification à la liste des demandes en attente.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-104">The `AddAdvisePacket` method adds an advise request to the list of pending requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1fc4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1fc4-105">Syntax</span></span>


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a><span data-ttu-id="e1fc4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1fc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1fc4-107">*time1* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="e1fc4-107">*time1* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fc4-108">Heure demandée pour la notification.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-108">Requested time for the advise.</span></span>

</dd> <dt>

<span data-ttu-id="e1fc4-109">*TIME2 ?* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="e1fc4-109">*time2* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fc4-110">Pour les demandes de notification périodiques, délai entre les notifications.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-110">For periodic advise requests, the time between notifications.</span></span> <span data-ttu-id="e1fc4-111">Ce paramètre est ignoré si *bPeriodic* a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-111">This parameter is ignored if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e1fc4-112">*hNotify*</span><span class="sxs-lookup"><span data-stu-id="e1fc4-112">*hNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="e1fc4-113">Handle vers un sémaphore si *bPeriodic* a la **valeur true** ou handle vers un événement si *bPeriodic* a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-113">Handle to a semaphore if *bPeriodic* is **TRUE**, or handle to an event if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e1fc4-114">*bPeriodic*</span><span class="sxs-lookup"><span data-stu-id="e1fc4-114">*bPeriodic*</span></span> 
</dt> <dd>

<span data-ttu-id="e1fc4-115">Valeur booléenne qui spécifie s’il faut ajouter une notification périodique ou une notification d’une seule capture.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-115">Boolean value that specifies whether to add a periodic notification or a one-shot notification.</span></span> <span data-ttu-id="e1fc4-116">Si la **valeur est true**, la notification est périodique ; le paramètre *TIME2 ?* spécifie le délai entre les notifications.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-116">If **TRUE**, the notification is periodic; the *time2* parameter specifies the time between notifications.</span></span> <span data-ttu-id="e1fc4-117">Si la **valeur est false**, la notification se produit une seule fois.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-117">If **FALSE**, the notification occurs only once.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1fc4-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1fc4-118">Return value</span></span>

<span data-ttu-id="e1fc4-119">Retourne un identificateur pour la demande de notification (le « cookie »).</span><span class="sxs-lookup"><span data-stu-id="e1fc4-119">Returns an identifier for the advise request (the "cookie").</span></span> <span data-ttu-id="e1fc4-120">Si la méthode échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="e1fc4-120">If the method fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1fc4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1fc4-121">Requirements</span></span>



| <span data-ttu-id="e1fc4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1fc4-122">Requirement</span></span> | <span data-ttu-id="e1fc4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1fc4-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1fc4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1fc4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e1fc4-125"><dt>Dsschedule. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1fc4-125"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="e1fc4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e1fc4-126">Library</span></span><br/> | <dl> <span data-ttu-id="e1fc4-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e1fc4-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1fc4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1fc4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1fc4-129">**CAMSchedule, classe**</span><span class="sxs-lookup"><span data-stu-id="e1fc4-129">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




