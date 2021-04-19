---
description: 'La méthode Receive reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval. Cette méthode remplace la méthode CTransformFilter :: Receive.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: CVideoTransformFilter. Receive, méthode (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541138"
---
# <a name="cvideotransformfilterreceive-method"></a><span data-ttu-id="d5647-104">CVideoTransformFilter. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="d5647-104">CVideoTransformFilter.Receive method</span></span>

<span data-ttu-id="d5647-105">La `Receive` méthode reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval.</span><span class="sxs-lookup"><span data-stu-id="d5647-105">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> <span data-ttu-id="d5647-106">Cette méthode remplace la méthode [**CTransformFilter :: Receive**](ctransformfilter-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="d5647-106">This method overrides the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5647-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5647-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="d5647-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5647-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5647-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="d5647-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d5647-110">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) sur l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d5647-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5647-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5647-111">Return value</span></span>

<span data-ttu-id="d5647-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5647-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d5647-113">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5647-113">Possible values include the following:</span></span>



| <span data-ttu-id="d5647-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d5647-114">Return code</span></span>                                                                             | <span data-ttu-id="d5647-115">Description</span><span class="sxs-lookup"><span data-stu-id="d5647-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="d5647-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d5647-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d5647-117">Le filtre amont doit cesser d’envoyer des exemples.</span><span class="sxs-lookup"><span data-stu-id="d5647-117">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="d5647-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5647-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d5647-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d5647-119">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="d5647-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d5647-120">Remarks</span></span>

<span data-ttu-id="d5647-121">Cette méthode appelle [**CVideoTransformFilter :: ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) pour déterminer si elle doit remettre cet exemple ou simplement la supprimer.</span><span class="sxs-lookup"><span data-stu-id="d5647-121">This method calls [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) to determine whether it should deliver this sample or simply discard it.</span></span> <span data-ttu-id="d5647-122">Si **ShouldSkipFrame** retourne **false** (indiquant que l’exemple doit être remis), la méthode effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5647-122">If **ShouldSkipFrame** returns **FALSE** (indicating the sample should be delivered), the method does the following:</span></span>

1.  <span data-ttu-id="d5647-123">Appelle [**CTransformFilter :: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) pour préparer l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="d5647-123">Calls [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) to prepare the output sample</span></span>
2.  <span data-ttu-id="d5647-124">Appelle [**CTransformFilter :: Transform**](ctransformfilter-transform.md) pour traiter l’exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d5647-124">Calls [**CTransformFilter::Transform**](ctransformfilter-transform.md) to process the input sample.</span></span> <span data-ttu-id="d5647-125">Cette méthode est virtuelle pure et doit être implémentée dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="d5647-125">This method is pure virtual, and must be implemented in the derived class.</span></span>
3.  <span data-ttu-id="d5647-126">Appelle [**CBaseOutputPin ::D eliver**](cbaseoutputpin-deliver.md) pour fournir l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5647-126">Calls [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) to deliver the output sample.</span></span>

<span data-ttu-id="d5647-127">En outre, cette méthode recherche les modifications de format sur l’exemple d’entrée ou de sortie, en appelant [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="d5647-127">Also, this method checks for format changes on the input or output sample, by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="d5647-128">En cas de modification du format, la méthode définit le type de connexion sur le code confidentiel correspondant.</span><span class="sxs-lookup"><span data-stu-id="d5647-128">If there is a format change, the method sets the connection type on the corresponding pin.</span></span> <span data-ttu-id="d5647-129">Avant de définir le nouveau type, il appelle **StopStreaming**.</span><span class="sxs-lookup"><span data-stu-id="d5647-129">Before it sets the new type, it calls **StopStreaming**.</span></span> <span data-ttu-id="d5647-130">Une fois le nouveau type défini, il appelle **StartStreaming**.</span><span class="sxs-lookup"><span data-stu-id="d5647-130">After it sets the new type, it calls **StartStreaming**.</span></span> <span data-ttu-id="d5647-131">La classe dérivée peut utiliser ces méthodes pour mettre à jour son état interne.</span><span class="sxs-lookup"><span data-stu-id="d5647-131">The derived class can use these methods to update its internal state.</span></span> <span data-ttu-id="d5647-132">La classe dérivée peut également avoir besoin de vérifier le nouveau format dans sa méthode **Transform** .</span><span class="sxs-lookup"><span data-stu-id="d5647-132">The derived class might also need to check for the new format in its **Transform** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5647-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5647-133">Requirements</span></span>



| <span data-ttu-id="d5647-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5647-134">Requirement</span></span> | <span data-ttu-id="d5647-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5647-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5647-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5647-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d5647-137"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5647-137"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d5647-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5647-138">Library</span></span><br/> | <dl> <span data-ttu-id="d5647-139"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d5647-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5647-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5647-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5647-141">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="d5647-141">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




