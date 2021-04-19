---
description: La méthode WaitForRenderTime attend l’heure de présentation de l’exemple actuel.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Méthode CBaseRenderer. WaitForRenderTime (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537350"
---
# <a name="cbaserendererwaitforrendertime-method"></a><span data-ttu-id="557ea-103">Méthode CBaseRenderer. WaitForRenderTime</span><span class="sxs-lookup"><span data-stu-id="557ea-103">CBaseRenderer.WaitForRenderTime method</span></span>

<span data-ttu-id="557ea-104">La `WaitForRenderTime` méthode attend l’heure de présentation de l’exemple actuel.</span><span class="sxs-lookup"><span data-stu-id="557ea-104">The `WaitForRenderTime` method waits for the current sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="557ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="557ea-105">Syntax</span></span>


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a><span data-ttu-id="557ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="557ea-106">Parameters</span></span>

<span data-ttu-id="557ea-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="557ea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="557ea-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="557ea-108">Return value</span></span>

<span data-ttu-id="557ea-109">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="557ea-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="557ea-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="557ea-110">Return code</span></span>                                                                                           | <span data-ttu-id="557ea-111">Description</span><span class="sxs-lookup"><span data-stu-id="557ea-111">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="557ea-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="557ea-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="557ea-113">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="557ea-113">Success.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="557ea-114"><dt>**\_État VFW \_ E \_ modifié**</dt></span><span class="sxs-lookup"><span data-stu-id="557ea-114"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="557ea-115">L’état du filtre a changé avant l’heure de la présentation.</span><span class="sxs-lookup"><span data-stu-id="557ea-115">The filter state changed before the presentation time arrived.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="557ea-116">Notes</span><span class="sxs-lookup"><span data-stu-id="557ea-116">Remarks</span></span>

<span data-ttu-id="557ea-117">Cette méthode attend jusqu’à ce que l’un des éléments suivants se produise :</span><span class="sxs-lookup"><span data-stu-id="557ea-117">This method waits until one of the following occurs:</span></span>

-   <span data-ttu-id="557ea-118">L’heure de présentation de l’exemple arrive, point où l’exemple peut être rendu.</span><span class="sxs-lookup"><span data-stu-id="557ea-118">The sample's presentation time arrives, at which point the sample can be rendered.</span></span>
-   <span data-ttu-id="557ea-119">Le filtre s’arrête ou commence à vider les données.</span><span class="sxs-lookup"><span data-stu-id="557ea-119">The filter stops or begins flushing data.</span></span>

<span data-ttu-id="557ea-120">Si l’heure de présentation arrive, l’événement [**CBaseRenderer :: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) est signalé.</span><span class="sxs-lookup"><span data-stu-id="557ea-120">If the presentation time arrives, the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event is signaled.</span></span> <span data-ttu-id="557ea-121">Si l’état change, l’événement [**CBaseRenderer :: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) est signalé.</span><span class="sxs-lookup"><span data-stu-id="557ea-121">If the state changes, the [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md) event is signaled.</span></span> <span data-ttu-id="557ea-122">Cette méthode attend les deux événements.</span><span class="sxs-lookup"><span data-stu-id="557ea-122">This method waits on both events.</span></span> <span data-ttu-id="557ea-123">La classe dérivée peut substituer cette méthode pour attendre des événements supplémentaires, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="557ea-123">The derived class can override this method to wait on additional events, if necessary.</span></span>

<span data-ttu-id="557ea-124">Cette méthode appelle la méthode [**CBaseRenderer :: OnWaitStart**](cbaserenderer-onwaitstart.md) lorsque l’attente commence, et la méthode [**CBaseRenderer :: OnWaitEnd**](cbaserenderer-onwaitend.md) quand l’attente est terminée.</span><span class="sxs-lookup"><span data-stu-id="557ea-124">This method calls the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method when the wait begins, and the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method when the wait is done.</span></span> <span data-ttu-id="557ea-125">Aucune de ces méthodes ne fait quoi que ce soit dans la classe de base, mais la classe dérivée peut les substituer.</span><span class="sxs-lookup"><span data-stu-id="557ea-125">Neither method does anything in the base class, but the derived class can override them.</span></span>

## <a name="requirements"></a><span data-ttu-id="557ea-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="557ea-126">Requirements</span></span>



| <span data-ttu-id="557ea-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="557ea-127">Requirement</span></span> | <span data-ttu-id="557ea-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="557ea-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="557ea-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="557ea-129">Header</span></span><br/>  | <dl> <span data-ttu-id="557ea-130"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="557ea-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="557ea-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="557ea-131">Library</span></span><br/> | <dl> <span data-ttu-id="557ea-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="557ea-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="557ea-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="557ea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="557ea-134">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="557ea-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




