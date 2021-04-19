---
description: La méthode ResetEndOfStreamTimer annule la minuterie qui planifie les \_ notifications complètes ec.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Méthode CBaseRenderer. ResetEndOfStreamTimer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 734673c4e2bd6719179eca00f03a6c2f41061132
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539312"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a><span data-ttu-id="5d645-103">Méthode CBaseRenderer. ResetEndOfStreamTimer</span><span class="sxs-lookup"><span data-stu-id="5d645-103">CBaseRenderer.ResetEndOfStreamTimer method</span></span>

<span data-ttu-id="5d645-104">La `ResetEndOfStreamTimer` méthode annule la minuterie qui planifie les notifications [**\_ complètes EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="5d645-104">The `ResetEndOfStreamTimer` method cancels the timer that schedules [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d645-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d645-105">Syntax</span></span>


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a><span data-ttu-id="5d645-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d645-106">Parameters</span></span>

<span data-ttu-id="5d645-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5d645-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d645-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d645-108">Return value</span></span>

<span data-ttu-id="5d645-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5d645-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d645-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d645-110">Requirements</span></span>



| <span data-ttu-id="5d645-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d645-111">Requirement</span></span> | <span data-ttu-id="5d645-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d645-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d645-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d645-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5d645-114"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d645-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d645-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d645-115">Library</span></span><br/> | <dl> <span data-ttu-id="5d645-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5d645-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d645-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d645-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d645-118">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="5d645-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="5d645-119">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="5d645-119">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> <dt>

[<span data-ttu-id="5d645-120">**CBaseRenderer :: TimerCallback**</span><span class="sxs-lookup"><span data-stu-id="5d645-120">**CBaseRenderer::TimerCallback**</span></span>](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




