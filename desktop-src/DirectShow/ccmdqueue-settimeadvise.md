---
description: La méthode SetTimeAdvise configure un événement de minuterie avec l’horloge de référence.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Méthode CCmdQueue. SetTimeAdvise (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528594"
---
# <a name="ccmdqueuesettimeadvise-method"></a><span data-ttu-id="40084-103">Méthode CCmdQueue. SetTimeAdvise</span><span class="sxs-lookup"><span data-stu-id="40084-103">CCmdQueue.SetTimeAdvise method</span></span>

<span data-ttu-id="40084-104">La `SetTimeAdvise` méthode configure un événement de minuterie avec l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="40084-104">The `SetTimeAdvise` method sets up a timer event with the reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="40084-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40084-105">Syntax</span></span>


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a><span data-ttu-id="40084-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40084-106">Parameters</span></span>

<span data-ttu-id="40084-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="40084-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40084-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40084-108">Return value</span></span>

<span data-ttu-id="40084-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="40084-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40084-110">Notes</span><span class="sxs-lookup"><span data-stu-id="40084-110">Remarks</span></span>

<span data-ttu-id="40084-111">Cette fonction membre appelle la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) pour configurer une notification pour l’heure la plus ancienne dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="40084-111">This member function calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method to set up a notification for the earliest time required in the queue.</span></span> <span data-ttu-id="40084-112">Les commandes à durée de présentation différées sont toujours vérifiées.</span><span class="sxs-lookup"><span data-stu-id="40084-112">Presentation-time commands that are deferred are always checked.</span></span> <span data-ttu-id="40084-113">Si le graphique de filtre est en mode d’exécution, les commandes différées utilisant le temps de flux sont également vérifiées.</span><span class="sxs-lookup"><span data-stu-id="40084-113">If the filter graph is in running mode, deferred commands using stream time are also checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="40084-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40084-114">Requirements</span></span>



| <span data-ttu-id="40084-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40084-115">Requirement</span></span> | <span data-ttu-id="40084-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="40084-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40084-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="40084-117">Header</span></span><br/>  | <dl> <span data-ttu-id="40084-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40084-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40084-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40084-119">Library</span></span><br/> | <dl> <span data-ttu-id="40084-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="40084-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40084-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40084-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40084-122">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="40084-122">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




