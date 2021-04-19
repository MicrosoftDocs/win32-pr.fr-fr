---
description: La méthode OnReceiveFirstSample est appelée quand le filtre reçoit un exemple en pause.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Méthode CBaseRenderer. OnReceiveFirstSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525656"
---
# <a name="cbaserendereronreceivefirstsample-method"></a><span data-ttu-id="f97a1-103">Méthode CBaseRenderer. OnReceiveFirstSample</span><span class="sxs-lookup"><span data-stu-id="f97a1-103">CBaseRenderer.OnReceiveFirstSample method</span></span>

<span data-ttu-id="f97a1-104">La `OnReceiveFirstSample` méthode est appelée lorsque le filtre reçoit un exemple en pause.</span><span class="sxs-lookup"><span data-stu-id="f97a1-104">The `OnReceiveFirstSample` method is called when the filter receives a sample while paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="f97a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f97a1-105">Syntax</span></span>


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="f97a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f97a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f97a1-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="f97a1-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f97a1-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="f97a1-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f97a1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f97a1-109">Return value</span></span>

<span data-ttu-id="f97a1-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f97a1-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f97a1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f97a1-111">Remarks</span></span>

<span data-ttu-id="f97a1-112">La méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f97a1-112">The [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method calls this method.</span></span> <span data-ttu-id="f97a1-113">Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="f97a1-113">It does nothing in the base class, but the derived class can override it.</span></span> <span data-ttu-id="f97a1-114">Cette méthode est principalement destinée aux convertisseurs vidéo.</span><span class="sxs-lookup"><span data-stu-id="f97a1-114">This method is intended primarily for video renderers.</span></span> <span data-ttu-id="f97a1-115">Lorsqu’un convertisseur vidéo est suspendu, il affiche généralement le premier échantillon sous la forme d’une image continue.</span><span class="sxs-lookup"><span data-stu-id="f97a1-115">When a video renderer is paused, it typically displays the first sample as a still image.</span></span>

<span data-ttu-id="f97a1-116">Si vous recherchez le graphique en pause, cette méthode est également appelée.</span><span class="sxs-lookup"><span data-stu-id="f97a1-116">Seeking the graph while paused also causes this method to be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f97a1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f97a1-117">Requirements</span></span>



| <span data-ttu-id="f97a1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f97a1-118">Requirement</span></span> | <span data-ttu-id="f97a1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f97a1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f97a1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f97a1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f97a1-121"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f97a1-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f97a1-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f97a1-122">Library</span></span><br/> | <dl> <span data-ttu-id="f97a1-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f97a1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f97a1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f97a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f97a1-125">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="f97a1-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




