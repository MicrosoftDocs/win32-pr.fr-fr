---
description: La méthode GetRealState récupère l’état du filtre.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Méthode CBaseRenderer. GetRealState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541320"
---
# <a name="cbaserenderergetrealstate-method"></a><span data-ttu-id="6ec5e-103">Méthode CBaseRenderer. GetRealState</span><span class="sxs-lookup"><span data-stu-id="6ec5e-103">CBaseRenderer.GetRealState method</span></span>

<span data-ttu-id="6ec5e-104">La `GetRealState` méthode récupère l’état du filtre.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-104">The `GetRealState` method retrieves the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec5e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ec5e-105">Syntax</span></span>


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a><span data-ttu-id="6ec5e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ec5e-106">Parameters</span></span>

<span data-ttu-id="6ec5e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ec5e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ec5e-108">Return value</span></span>

<span data-ttu-id="6ec5e-109">Retourne la valeur de l' [**\_ État CBaseFilter :: m**](cbasefilter-m-state.md).</span><span class="sxs-lookup"><span data-stu-id="6ec5e-109">Returns the value of [**CBaseFilter::m\_State**](cbasefilter-m-state.md).</span></span> <span data-ttu-id="6ec5e-110">La valeur est un membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="6ec5e-110">The value is a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec5e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6ec5e-111">Remarks</span></span>

<span data-ttu-id="6ec5e-112">Cette méthode offre une alternative plus simple à la méthode [**CBaseRenderer :: GetState**](cbaserenderer-getstate.md) , à des fins d’utilisation interne.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-112">This method provides a simpler alternative to the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method, for internal use.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec5e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ec5e-113">Requirements</span></span>



| <span data-ttu-id="6ec5e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ec5e-114">Requirement</span></span> | <span data-ttu-id="6ec5e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ec5e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec5e-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ec5e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6ec5e-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ec5e-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ec5e-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ec5e-118">Library</span></span><br/> | <dl> <span data-ttu-id="6ec5e-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ec5e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ec5e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ec5e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec5e-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="6ec5e-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




