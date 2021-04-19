---
description: La méthode pause interrompt le filtre. Cette méthode implémente la méthode IMediaFilter ::P ause.
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: CBaseFilter. pause, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a90e78084f2320d0df7da806b6138571c9a5bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529981"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="5e6c4-104">CBaseFilter. pause, méthode</span><span class="sxs-lookup"><span data-stu-id="5e6c4-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="5e6c4-105">La `Pause` méthode suspend le filtre.</span><span class="sxs-lookup"><span data-stu-id="5e6c4-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="5e6c4-106">Cette méthode implémente la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="5e6c4-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6c4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e6c4-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="5e6c4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e6c4-108">Parameters</span></span>

<span data-ttu-id="5e6c4-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5e6c4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e6c4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e6c4-110">Return value</span></span>

<span data-ttu-id="5e6c4-111">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="5e6c4-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e6c4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5e6c4-112">Remarks</span></span>

<span data-ttu-id="5e6c4-113">Cette méthode appelle la méthode [**CBasePin :: active**](cbasepin-active.md) sur chacune des broches connectées du filtre.</span><span class="sxs-lookup"><span data-stu-id="5e6c4-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e6c4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e6c4-114">Requirements</span></span>



| <span data-ttu-id="5e6c4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e6c4-115">Requirement</span></span> | <span data-ttu-id="5e6c4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e6c4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e6c4-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e6c4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5e6c4-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e6c4-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5e6c4-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5e6c4-119">Library</span></span><br/> | <dl> <span data-ttu-id="5e6c4-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5e6c4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e6c4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e6c4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6c4-122">**CBaseFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="5e6c4-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




