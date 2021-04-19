---
description: 'La méthode Run exécute l’objet. Cette méthode implémente la méthode IMediaFilter :: Run.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: CBaseMediaFilter. Run, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528634"
---
# <a name="cbasemediafilterrun-method"></a><span data-ttu-id="9d7c4-104">CBaseMediaFilter. Run, méthode</span><span class="sxs-lookup"><span data-stu-id="9d7c4-104">CBaseMediaFilter.Run method</span></span>

<span data-ttu-id="9d7c4-105">La `Run` méthode exécute l’objet.</span><span class="sxs-lookup"><span data-stu-id="9d7c4-105">The `Run` method runs the object.</span></span> <span data-ttu-id="9d7c4-106">Cette méthode implémente la méthode [**IMediaFilter :: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="9d7c4-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d7c4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d7c4-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="9d7c4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d7c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d7c4-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="9d7c4-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="9d7c4-110">Temps de référence correspondant au temps de flux 0.</span><span class="sxs-lookup"><span data-stu-id="9d7c4-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d7c4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d7c4-111">Return value</span></span>

<span data-ttu-id="9d7c4-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9d7c4-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d7c4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9d7c4-113">Remarks</span></span>

<span data-ttu-id="9d7c4-114">Si l’objet est arrêté, cette méthode suspend l’objet en appelant la méthode [**CBaseMediaFilter ::P ause**](cbasemediafilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="9d7c4-114">If the object is stopped, this method pauses the object by calling the [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md) method.</span></span> <span data-ttu-id="9d7c4-115">Il définit ensuite la variable de membre d' [**\_ État CBaseMediaFilter :: m**](cbasemediafilter-m-state.md) sur State \_ Running.</span><span class="sxs-lookup"><span data-stu-id="9d7c4-115">It then sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="9d7c4-116">Le temps de flux est calculé comme le temps de référence actuel moins *tStart*.</span><span class="sxs-lookup"><span data-stu-id="9d7c4-116">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="9d7c4-117">Un échantillon de média avec un horodatage de zéro doit être affiché au moment du *tStart*.</span><span class="sxs-lookup"><span data-stu-id="9d7c4-117">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d7c4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d7c4-118">Requirements</span></span>



| <span data-ttu-id="9d7c4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d7c4-119">Requirement</span></span> | <span data-ttu-id="9d7c4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d7c4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7c4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d7c4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9d7c4-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d7c4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9d7c4-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d7c4-123">Library</span></span><br/> | <dl> <span data-ttu-id="9d7c4-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9d7c4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d7c4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d7c4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d7c4-126">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="9d7c4-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




