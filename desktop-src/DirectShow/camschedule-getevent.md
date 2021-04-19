---
description: La méthode GetEvent récupère un handle d’événement, qui est utilisé pour signaler une modification de l’heure suivante de l’avis.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Méthode CAMSchedule. GetEvent (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525487"
---
# <a name="camschedulegetevent-method"></a><span data-ttu-id="f0e87-103">Méthode CAMSchedule. GetEvent</span><span class="sxs-lookup"><span data-stu-id="f0e87-103">CAMSchedule.GetEvent method</span></span>

<span data-ttu-id="f0e87-104">La `GetEvent` méthode récupère un handle d’événement, qui est utilisé pour signaler une modification de l’heure suivante de l’avis.</span><span class="sxs-lookup"><span data-stu-id="f0e87-104">The `GetEvent` method retrieves an event handle, which is used to signal a change in the next advise time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e87-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0e87-105">Syntax</span></span>


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a><span data-ttu-id="f0e87-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0e87-106">Parameters</span></span>

<span data-ttu-id="f0e87-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f0e87-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0e87-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0e87-108">Return value</span></span>

<span data-ttu-id="f0e87-109">Retourne un handle pour un événement.</span><span class="sxs-lookup"><span data-stu-id="f0e87-109">Returns a handle to an event.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0e87-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f0e87-110">Remarks</span></span>

<span data-ttu-id="f0e87-111">Si l’heure suivante de l’avis change en d’autres termes, si une nouvelle demande de notification est ajoutée au début de la liste, le planificateur signale cet événement.</span><span class="sxs-lookup"><span data-stu-id="f0e87-111">If the next advise time changes in other words, if a new advise request is added to the front of the list the scheduler signals this event.</span></span> <span data-ttu-id="f0e87-112">L’horloge doit appeler la méthode [**CAMSchedule :: Advise**](camschedule-advise.md) pour déterminer l’heure de l’avis suivante.</span><span class="sxs-lookup"><span data-stu-id="f0e87-112">The clock should call the [**CAMSchedule::Advise**](camschedule-advise.md) method to determine the next advise time.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e87-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0e87-113">Requirements</span></span>



| <span data-ttu-id="f0e87-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0e87-114">Requirement</span></span> | <span data-ttu-id="f0e87-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0e87-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e87-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0e87-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f0e87-117"><dt>Dsschedule. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0e87-117"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="f0e87-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0e87-118">Library</span></span><br/> | <dl> <span data-ttu-id="f0e87-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f0e87-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0e87-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0e87-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e87-121">**CAMSchedule, classe**</span><span class="sxs-lookup"><span data-stu-id="f0e87-121">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




