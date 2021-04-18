---
description: La méthode check vérifie si l’événement est défini, sans blocage.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: CAMEvent. Check, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536259"
---
# <a name="cameventcheck-method"></a><span data-ttu-id="51220-103">CAMEvent. Check, méthode</span><span class="sxs-lookup"><span data-stu-id="51220-103">CAMEvent.Check method</span></span>

<span data-ttu-id="51220-104">La `Check` méthode vérifie si l’événement est défini, sans blocage.</span><span class="sxs-lookup"><span data-stu-id="51220-104">The `Check` method checks whether the event is set, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="51220-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51220-105">Syntax</span></span>


```C++
BOOL Check();
```



## <a name="parameters"></a><span data-ttu-id="51220-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51220-106">Parameters</span></span>

<span data-ttu-id="51220-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="51220-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="51220-108">Notes</span><span class="sxs-lookup"><span data-stu-id="51220-108">Remarks</span></span>

<span data-ttu-id="51220-109">Retourne la **valeur true** si l’événement est défini, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="51220-109">Returns **TRUE** if the event is set, or **FALSE** otherwise.</span></span> <span data-ttu-id="51220-110">Cette méthode appelle la méthode [**CAMEvent :: wait**](camevent-wait.md) avec un délai d’attente de zéro.</span><span class="sxs-lookup"><span data-stu-id="51220-110">This method calls the [**CAMEvent::Wait**](camevent-wait.md) method with a time-out of zero.</span></span> <span data-ttu-id="51220-111">Si l’objet est un événement à réinitialisation automatique, cette méthode réinitialise l’événement.</span><span class="sxs-lookup"><span data-stu-id="51220-111">If the object is an auto-reset event, this method resets the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="51220-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51220-112">Requirements</span></span>



| <span data-ttu-id="51220-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51220-113">Requirement</span></span> | <span data-ttu-id="51220-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="51220-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51220-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="51220-115">Header</span></span><br/>  | <dl> <span data-ttu-id="51220-116"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51220-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="51220-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51220-117">Library</span></span><br/> | <dl> <span data-ttu-id="51220-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="51220-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51220-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51220-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51220-120">**CAMEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="51220-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




