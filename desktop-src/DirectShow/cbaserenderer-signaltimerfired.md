---
description: La méthode SignalTimerFired efface l’identificateur de minuterie utilisé pour planifier le rendu.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Méthode CBaseRenderer. SignalTimerFired (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526671"
---
# <a name="cbaserenderersignaltimerfired-method"></a><span data-ttu-id="3a1d3-103">Méthode CBaseRenderer. SignalTimerFired</span><span class="sxs-lookup"><span data-stu-id="3a1d3-103">CBaseRenderer.SignalTimerFired method</span></span>

<span data-ttu-id="3a1d3-104">La `SignalTimerFired` méthode efface l’identificateur de minuterie utilisé pour planifier le rendu.</span><span class="sxs-lookup"><span data-stu-id="3a1d3-104">The `SignalTimerFired` method clears the timer identifier used to schedule rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a1d3-105">Syntax</span></span>


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a><span data-ttu-id="3a1d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a1d3-106">Parameters</span></span>

<span data-ttu-id="3a1d3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3a1d3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a1d3-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a1d3-108">Return value</span></span>

<span data-ttu-id="3a1d3-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3a1d3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a1d3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3a1d3-110">Remarks</span></span>

<span data-ttu-id="3a1d3-111">Le filtre appelle cette méthode lorsque le minuteur de rendu s’active (consultez [**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) ou lorsque la minuterie est annulée (consultez [**CBaseRenderer :: CancelNotification**](cbaserenderer-cancelnotification.md)).</span><span class="sxs-lookup"><span data-stu-id="3a1d3-111">The filter calls this method when the rendering timer activates (see [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) or when the timer is canceled (see [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)).</span></span> <span data-ttu-id="3a1d3-112">La méthode réinitialise la variable de membre [**CBaseRenderer :: m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) à zéro.</span><span class="sxs-lookup"><span data-stu-id="3a1d3-112">The method resets the [**CBaseRenderer::m\_dwAdvise**](cbaserenderer-m-dwadvise.md) member variable to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1d3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a1d3-113">Requirements</span></span>



| <span data-ttu-id="3a1d3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a1d3-114">Requirement</span></span> | <span data-ttu-id="3a1d3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a1d3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1d3-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a1d3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3a1d3-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d3-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a1d3-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a1d3-118">Library</span></span><br/> | <dl> <span data-ttu-id="3a1d3-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1d3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a1d3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1d3-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="3a1d3-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




