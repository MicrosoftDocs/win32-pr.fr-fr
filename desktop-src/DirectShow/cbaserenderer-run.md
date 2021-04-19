---
description: La méthode Run exécute le filtre.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: CBaseRenderer. Run, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525655"
---
# <a name="cbaserendererrun-method"></a><span data-ttu-id="0968b-103">CBaseRenderer. Run, méthode</span><span class="sxs-lookup"><span data-stu-id="0968b-103">CBaseRenderer.Run method</span></span>

<span data-ttu-id="0968b-104">La `Run` méthode exécute le filtre.</span><span class="sxs-lookup"><span data-stu-id="0968b-104">The `Run` method runs the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0968b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0968b-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="0968b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0968b-106">Parameters</span></span>

<span data-ttu-id="0968b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0968b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0968b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0968b-108">Return value</span></span>

<span data-ttu-id="0968b-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0968b-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0968b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0968b-110">Remarks</span></span>

<span data-ttu-id="0968b-111">Cette méthode remplace la méthode [**CBaseFilter :: Run**](cbasefilter-run.md) .</span><span class="sxs-lookup"><span data-stu-id="0968b-111">This method overrides the [**CBaseFilter::Run**](cbasefilter-run.md) method.</span></span> <span data-ttu-id="0968b-112">Il effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0968b-112">It performs the following actions:</span></span>

-   <span data-ttu-id="0968b-113">Appelle la méthode **CBaseFilter :: Run** .</span><span class="sxs-lookup"><span data-stu-id="0968b-113">Calls the **CBaseFilter::Run** method.</span></span>
-   <span data-ttu-id="0968b-114">Valide l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="0968b-114">Commits the allocator.</span></span> <span data-ttu-id="0968b-115">(Consultez [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span><span class="sxs-lookup"><span data-stu-id="0968b-115">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="0968b-116">Si l’état précédent a été arrêté, le filtre libère tout échantillon qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="0968b-116">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="0968b-117">(L’exemple n’est plus valide.)</span><span class="sxs-lookup"><span data-stu-id="0968b-117">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="0968b-118">Appelle la méthode [**CBaseRenderer :: StartStreaming**](cbaserenderer-startstreaming.md) et retourne le résultat.</span><span class="sxs-lookup"><span data-stu-id="0968b-118">Calls the [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method and returns the result.</span></span> <span data-ttu-id="0968b-119">Si un échantillon est en attente, la méthode **StartStreaming** le planifie pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="0968b-119">If a sample is pending, the **StartStreaming** method schedules it for rendering.</span></span>

<span data-ttu-id="0968b-120">Si le filtre n’est pas connecté, il publie immédiatement un événement [**EC \_ Complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="0968b-120">If the filter is not connected, it posts an [**EC\_COMPLETE**](ec-complete.md) event immediately.</span></span>

## <a name="requirements"></a><span data-ttu-id="0968b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0968b-121">Requirements</span></span>



| <span data-ttu-id="0968b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0968b-122">Requirement</span></span> | <span data-ttu-id="0968b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0968b-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0968b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0968b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0968b-125"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0968b-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0968b-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0968b-126">Library</span></span><br/> | <dl> <span data-ttu-id="0968b-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0968b-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0968b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0968b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0968b-129">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="0968b-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




