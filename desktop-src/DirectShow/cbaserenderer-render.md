---
description: La méthode Render restitue un exemple.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: CBaseRenderer. Render, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544128"
---
# <a name="cbaserendererrender-method"></a><span data-ttu-id="0a2b5-103">CBaseRenderer. Render, méthode</span><span class="sxs-lookup"><span data-stu-id="0a2b5-103">CBaseRenderer.Render method</span></span>

<span data-ttu-id="0a2b5-104">La `Render` méthode restitue un exemple.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-104">The `Render` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a2b5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a2b5-105">Syntax</span></span>


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="0a2b5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a2b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a2b5-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="0a2b5-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0a2b5-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a2b5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a2b5-109">Return value</span></span>

<span data-ttu-id="0a2b5-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a2b5-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0a2b5-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a2b5-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="0a2b5-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0a2b5-112">Return code</span></span>                                                                             | <span data-ttu-id="0a2b5-113">Description</span><span class="sxs-lookup"><span data-stu-id="0a2b5-113">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a2b5-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b5-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="0a2b5-115">Le filtre est arrêté, ou *pMediaSample* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-115">The filter is stopped, or *pMediaSample* is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="0a2b5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b5-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="0a2b5-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-117">Success.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="0a2b5-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0a2b5-118">Remarks</span></span>

<span data-ttu-id="0a2b5-119">Cette méthode appelle la méthode virtuelle pure [**CBaseRenderer ::D orendersample**](cbaserenderer-dorendersample.md), qui fait le vrai travail.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-119">This method calls the pure virtual method [**CBaseRenderer::DoRenderSample**](cbaserenderer-dorendersample.md), which does the real work.</span></span> <span data-ttu-id="0a2b5-120">La classe dérivée doit implémenter **DoRenderSample**.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-120">The derived class must implement **DoRenderSample**.</span></span>

<span data-ttu-id="0a2b5-121">Juste avant d’appeler **DoRenderSample**, cette méthode appelle la méthode [**CBaseRenderer :: OnRenderStart**](cbaserenderer-onrenderstart.md) .</span><span class="sxs-lookup"><span data-stu-id="0a2b5-121">Immediately before calling **DoRenderSample**, this method calls the [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md) method.</span></span> <span data-ttu-id="0a2b5-122">Immédiatement après, il appelle la méthode [**CBaseRenderer :: OnRenderEnd**](cbaserenderer-onrenderend.md) .</span><span class="sxs-lookup"><span data-stu-id="0a2b5-122">Immediately after, it calls the [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md) method.</span></span> <span data-ttu-id="0a2b5-123">La classe dérivée peut substituer ces deux méthodes en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-123">The derived class can override those two methods as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a2b5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a2b5-124">Requirements</span></span>



| <span data-ttu-id="0a2b5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a2b5-125">Requirement</span></span> | <span data-ttu-id="0a2b5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a2b5-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2b5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a2b5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0a2b5-128"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b5-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a2b5-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a2b5-129">Library</span></span><br/> | <dl> <span data-ttu-id="0a2b5-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b5-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a2b5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a2b5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a2b5-132">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="0a2b5-132">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




