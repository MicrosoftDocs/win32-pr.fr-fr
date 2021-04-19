---
description: La méthode ScheduleSample planifie un exemple de rendu.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Méthode CBaseRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527332"
---
# <a name="cbaserendererschedulesample-method"></a><span data-ttu-id="ec073-103">Méthode CBaseRenderer. ScheduleSample</span><span class="sxs-lookup"><span data-stu-id="ec073-103">CBaseRenderer.ScheduleSample method</span></span>

<span data-ttu-id="ec073-104">La `ScheduleSample` méthode planifie un exemple de rendu.</span><span class="sxs-lookup"><span data-stu-id="ec073-104">The `ScheduleSample` method schedules a sample for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec073-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec073-105">Syntax</span></span>


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="ec073-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec073-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec073-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="ec073-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ec073-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="ec073-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec073-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec073-109">Return value</span></span>

<span data-ttu-id="ec073-110">Retourne la **valeur true** si l’exemple a été planifié, ou **false** si l’exemple a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="ec073-110">Returns **TRUE** if the sample was scheduled, or **FALSE** if the sample was dropped.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec073-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ec073-111">Remarks</span></span>

<span data-ttu-id="ec073-112">Cette méthode détermine d’abord si l’exemple doit être rendu immédiatement, rendu dans le futur ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="ec073-112">This method first determines whether the sample should be rendered immediately, rendered in the future, or dropped.</span></span> <span data-ttu-id="ec073-113">(Pour ce faire, elle appelle la méthode [**CBaseRenderer :: GetSampleTimes**](cbaserenderer-getsampletimes.md) .) Si l’exemple doit être rendu immédiatement, la méthode signale l’événement [**CBaseRenderer :: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="ec073-113">(To do so, it calls the [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method.) If the sample should be rendered immediately, the method signals the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span> <span data-ttu-id="ec073-114">Si l’exemple doit être rendu à l’avenir, la méthode appelle la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) pour la planification.</span><span class="sxs-lookup"><span data-stu-id="ec073-114">If the sample should be rendered in the future, the method calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method for scheduling.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec073-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec073-115">Requirements</span></span>



| <span data-ttu-id="ec073-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec073-116">Requirement</span></span> | <span data-ttu-id="ec073-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec073-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec073-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec073-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ec073-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec073-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec073-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ec073-120">Library</span></span><br/> | <dl> <span data-ttu-id="ec073-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec073-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec073-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec073-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec073-123">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="ec073-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




