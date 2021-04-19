---
description: La méthode GetNextAdviseTime récupère l’heure de la demande de notification suivante.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Méthode CAMSchedule. GetNextAdviseTime (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528865"
---
# <a name="camschedulegetnextadvisetime-method"></a><span data-ttu-id="cac2b-103">Méthode CAMSchedule. GetNextAdviseTime</span><span class="sxs-lookup"><span data-stu-id="cac2b-103">CAMSchedule.GetNextAdviseTime method</span></span>

<span data-ttu-id="cac2b-104">La `GetNextAdviseTime` méthode récupère l’heure de la demande de notification suivante.</span><span class="sxs-lookup"><span data-stu-id="cac2b-104">The `GetNextAdviseTime` method retrieves the time of the next advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cac2b-105">Syntax</span></span>


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a><span data-ttu-id="cac2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cac2b-106">Parameters</span></span>

<span data-ttu-id="cac2b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cac2b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cac2b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cac2b-108">Return value</span></span>

<span data-ttu-id="cac2b-109">Retourne le temps de référence de la demande d’avis suivante ou la \_ durée maximale pendant laquelle aucune demande n’est planifiée.</span><span class="sxs-lookup"><span data-stu-id="cac2b-109">Returns the reference time of the next advise request, or MAX\_TIME no requests are scheduled.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac2b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cac2b-110">Requirements</span></span>



| <span data-ttu-id="cac2b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cac2b-111">Requirement</span></span> | <span data-ttu-id="cac2b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cac2b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac2b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="cac2b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="cac2b-114"><dt>Dsschedule. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cac2b-114"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="cac2b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cac2b-115">Library</span></span><br/> | <dl> <span data-ttu-id="cac2b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cac2b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac2b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cac2b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac2b-118">**CAMSchedule, classe**</span><span class="sxs-lookup"><span data-stu-id="cac2b-118">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




