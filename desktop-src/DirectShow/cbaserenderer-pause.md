---
description: La méthode pause interrompt le filtre.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: CBaseRenderer. pause, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544057"
---
# <a name="cbaserendererpause-method"></a><span data-ttu-id="3c2c3-103">CBaseRenderer. pause, méthode</span><span class="sxs-lookup"><span data-stu-id="3c2c3-103">CBaseRenderer.Pause method</span></span>

<span data-ttu-id="3c2c3-104">La `Pause` méthode suspend le filtre.</span><span class="sxs-lookup"><span data-stu-id="3c2c3-104">The `Pause` method pauses the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c2c3-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="3c2c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c2c3-106">Parameters</span></span>

<span data-ttu-id="3c2c3-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3c2c3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c2c3-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c2c3-108">Return value</span></span>

<span data-ttu-id="3c2c3-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c2c3-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3c2c3-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c2c3-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="3c2c3-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3c2c3-111">Return code</span></span>                                                                             | <span data-ttu-id="3c2c3-112">Description</span><span class="sxs-lookup"><span data-stu-id="3c2c3-112">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="3c2c3-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2c3-113"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3c2c3-114">La transition est terminée.</span><span class="sxs-lookup"><span data-stu-id="3c2c3-114">The transition is complete.</span></span><br/> |
| <dl> <span data-ttu-id="3c2c3-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2c3-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3c2c3-116">La transition n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="3c2c3-116">Transition is not complete.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c2c3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3c2c3-117">Remarks</span></span>

<span data-ttu-id="3c2c3-118">Cette méthode remplace la méthode [**CBaseFilter ::P ause**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2c3-118">This method overrides the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="3c2c3-119">Il permet d'effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c2c3-119">It performs the following steps:</span></span>

-   <span data-ttu-id="3c2c3-120">Appelle la méthode **CBaseFilter ::P ause** .</span><span class="sxs-lookup"><span data-stu-id="3c2c3-120">Calls the **CBaseFilter::Pause** method.</span></span>
-   <span data-ttu-id="3c2c3-121">Valide l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="3c2c3-121">Commits the allocator.</span></span> <span data-ttu-id="3c2c3-122">(Consultez [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span><span class="sxs-lookup"><span data-stu-id="3c2c3-122">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="3c2c3-123">Si l’état précédent a été arrêté, le filtre libère tout échantillon qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="3c2c3-123">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="3c2c3-124">(L’exemple n’est plus valide.)</span><span class="sxs-lookup"><span data-stu-id="3c2c3-124">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="3c2c3-125">Appelle la méthode [**CBaseRenderer :: CompleteStateChange**](cbaserenderer-completestatechange.md) et retourne la valeur.</span><span class="sxs-lookup"><span data-stu-id="3c2c3-125">Calls the [**CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) method and returns the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2c3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c2c3-126">Requirements</span></span>



| <span data-ttu-id="3c2c3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c2c3-127">Requirement</span></span> | <span data-ttu-id="3c2c3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c2c3-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2c3-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c2c3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3c2c3-130"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c2c3-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c2c3-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c2c3-131">Library</span></span><br/> | <dl> <span data-ttu-id="3c2c3-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3c2c3-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2c3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c2c3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2c3-134">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="3c2c3-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




