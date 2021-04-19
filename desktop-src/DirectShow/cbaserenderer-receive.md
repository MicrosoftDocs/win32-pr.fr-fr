---
description: La méthode Receive reçoit l’exemple de support suivant dans le flux.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: CBaseRenderer. Receive, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537716"
---
# <a name="cbaserendererreceive-method"></a><span data-ttu-id="24c40-103">CBaseRenderer. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="24c40-103">CBaseRenderer.Receive method</span></span>

<span data-ttu-id="24c40-104">La `Receive` méthode reçoit l’échantillon de média suivant dans le flux.</span><span class="sxs-lookup"><span data-stu-id="24c40-104">The `Receive` method receives the next media sample in the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24c40-105">Syntax</span></span>


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="24c40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24c40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c40-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="24c40-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="24c40-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="24c40-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c40-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24c40-109">Return value</span></span>

<span data-ttu-id="24c40-110">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="24c40-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c40-111">Notes</span><span class="sxs-lookup"><span data-stu-id="24c40-111">Remarks</span></span>

<span data-ttu-id="24c40-112">La broche d’entrée appelle cette méthode lorsqu’elle reçoit un échantillon du filtre en amont.</span><span class="sxs-lookup"><span data-stu-id="24c40-112">The input pin calls this method when it receives a sample from the upstream filter.</span></span>

<span data-ttu-id="24c40-113">Si le filtre est en cours d’exécution, cette méthode effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="24c40-113">If the filter is running, this method performs the following steps:</span></span>

1.  <span data-ttu-id="24c40-114">Planifie l’exemple de rendu ([**CBaseRenderer ::P reparereceive**](cbaserenderer-preparereceive.md)).</span><span class="sxs-lookup"><span data-stu-id="24c40-114">Schedules the sample for rendering ([**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md)).</span></span>
2.  <span data-ttu-id="24c40-115">Attend l’heure planifiée ([**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span><span class="sxs-lookup"><span data-stu-id="24c40-115">Waits for the scheduled time ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span></span>
3.  <span data-ttu-id="24c40-116">Génère le rendu de l’exemple ([**CBaseRenderer :: Render**](cbaserenderer-render.md)).</span><span class="sxs-lookup"><span data-stu-id="24c40-116">Renders the sample ([**CBaseRenderer::Render**](cbaserenderer-render.md)).</span></span>
4.  <span data-ttu-id="24c40-117">Libère l’exemple ([**CBaseRenderer :: ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span><span class="sxs-lookup"><span data-stu-id="24c40-117">Releases the sample ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span></span>

<span data-ttu-id="24c40-118">Si le filtre est suspendu, la méthode effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="24c40-118">If the filter is paused, the method performs the following steps:</span></span>

1.  <span data-ttu-id="24c40-119">Notifie la classe dérivée qu’un exemple est disponible ([**CBaseRenderer :: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span><span class="sxs-lookup"><span data-stu-id="24c40-119">Notifies the derived class that a sample is available ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span></span>
2.  <span data-ttu-id="24c40-120">Attend l’heure planifiée.</span><span class="sxs-lookup"><span data-stu-id="24c40-120">Waits for the scheduled time.</span></span>
3.  <span data-ttu-id="24c40-121">Génère le rendu de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="24c40-121">Renders the sample.</span></span>
4.  <span data-ttu-id="24c40-122">Libère l’exemple.</span><span class="sxs-lookup"><span data-stu-id="24c40-122">Releases the sample.</span></span>

<span data-ttu-id="24c40-123">Pendant la suspension, la méthode attend à l’étape 2 jusqu’à ce que le filtre bascule vers un état d’exécution.</span><span class="sxs-lookup"><span data-stu-id="24c40-123">While paused, the method waits in step 2 until the filter switches to a running state.</span></span> <span data-ttu-id="24c40-124">À ce stade, le filtre planifie l’exemple.</span><span class="sxs-lookup"><span data-stu-id="24c40-124">At that point, the filter schedules the sample.</span></span>

<span data-ttu-id="24c40-125">Dans la classe de base, la méthode **OnReceiveFirstSample** n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="24c40-125">In the base class, the **OnReceiveFirstSample** method does nothing.</span></span> <span data-ttu-id="24c40-126">La classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="24c40-126">The derived class can override it.</span></span> <span data-ttu-id="24c40-127">Par exemple, lorsqu’un convertisseur vidéo est suspendu, il affiche le premier échantillon sous la forme d’une image continue.</span><span class="sxs-lookup"><span data-stu-id="24c40-127">For example, when a video renderer is paused, it displays the first sample as a still image.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c40-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24c40-128">Requirements</span></span>



| <span data-ttu-id="24c40-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24c40-129">Requirement</span></span> | <span data-ttu-id="24c40-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="24c40-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c40-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="24c40-131">Header</span></span><br/>  | <dl> <span data-ttu-id="24c40-132"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24c40-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24c40-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="24c40-133">Library</span></span><br/> | <dl> <span data-ttu-id="24c40-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="24c40-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c40-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24c40-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c40-136">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="24c40-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




