---
description: 'La méthode Run exécute le filtre. Cette méthode implémente la méthode IMediaFilter :: Run.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: CBaseFilter. Run, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535943"
---
# <a name="cbasefilterrun-method"></a><span data-ttu-id="e1ce0-104">CBaseFilter. Run, méthode</span><span class="sxs-lookup"><span data-stu-id="e1ce0-104">CBaseFilter.Run method</span></span>

<span data-ttu-id="e1ce0-105">La `Run` méthode exécute le filtre.</span><span class="sxs-lookup"><span data-stu-id="e1ce0-105">The `Run` method runs the filter.</span></span> <span data-ttu-id="e1ce0-106">Cette méthode implémente la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="e1ce0-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ce0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1ce0-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="e1ce0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1ce0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ce0-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="e1ce0-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="e1ce0-110">Temps de référence correspondant au temps de flux 0.</span><span class="sxs-lookup"><span data-stu-id="e1ce0-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1ce0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1ce0-111">Return value</span></span>

<span data-ttu-id="e1ce0-112">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e1ce0-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1ce0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e1ce0-113">Remarks</span></span>

<span data-ttu-id="e1ce0-114">Si le filtre est arrêté, cette méthode suspend le filtre en appelant la méthode [**CBaseFilter ::P ause**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ce0-114">If the filter is stopped, this method pauses the filter by calling the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="e1ce0-115">Il appelle ensuite la méthode [**CBasePin :: Run**](cbasepin-run.md) sur chacune des broches connectées du filtre.</span><span class="sxs-lookup"><span data-stu-id="e1ce0-115">It then calls the [**CBasePin::Run**](cbasepin-run.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="e1ce0-116">Enfin, il définit la variable de membre d' [**\_ État CBaseFilter :: m**](cbasefilter-m-state.md) sur State \_ Running.</span><span class="sxs-lookup"><span data-stu-id="e1ce0-116">Finally, it sets the [**CBaseFilter::m\_State**](cbasefilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="e1ce0-117">Le temps de flux est calculé comme le temps de référence actuel moins *tStart*.</span><span class="sxs-lookup"><span data-stu-id="e1ce0-117">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="e1ce0-118">Un échantillon de média avec un horodatage de zéro doit être affiché au moment du *tStart*.</span><span class="sxs-lookup"><span data-stu-id="e1ce0-118">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ce0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1ce0-119">Requirements</span></span>



| <span data-ttu-id="e1ce0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1ce0-120">Requirement</span></span> | <span data-ttu-id="e1ce0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1ce0-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ce0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1ce0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e1ce0-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1ce0-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e1ce0-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e1ce0-124">Library</span></span><br/> | <dl> <span data-ttu-id="e1ce0-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e1ce0-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ce0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1ce0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ce0-127">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="e1ce0-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




