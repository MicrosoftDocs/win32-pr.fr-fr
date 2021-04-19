---
description: La méthode PrepareReceive prépare le filtre pour le rendu d’un exemple.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Méthode CBaseRenderer. PrepareReceive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530032"
---
# <a name="cbaserendererpreparereceive-method"></a><span data-ttu-id="e31c2-103">Méthode CBaseRenderer. PrepareReceive</span><span class="sxs-lookup"><span data-stu-id="e31c2-103">CBaseRenderer.PrepareReceive method</span></span>

<span data-ttu-id="e31c2-104">La `PrepareReceive` méthode prépare le filtre pour restituer un exemple.</span><span class="sxs-lookup"><span data-stu-id="e31c2-104">The `PrepareReceive` method prepares the filter to render a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e31c2-105">Syntax</span></span>


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="e31c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e31c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31c2-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="e31c2-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e31c2-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e31c2-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31c2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e31c2-109">Return value</span></span>

<span data-ttu-id="e31c2-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e31c2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e31c2-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e31c2-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e31c2-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e31c2-112">Return code</span></span>                                                                                             | <span data-ttu-id="e31c2-113">Description</span><span class="sxs-lookup"><span data-stu-id="e31c2-113">Description</span></span>                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="e31c2-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e31c2-114"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="e31c2-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e31c2-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="e31c2-116"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="e31c2-116"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="e31c2-117">Échec.</span><span class="sxs-lookup"><span data-stu-id="e31c2-117">Failed.</span></span><br/>                         |
| <dl> <span data-ttu-id="e31c2-118"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="e31c2-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="e31c2-119">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="e31c2-119">Unexpected error.</span></span><br/>               |
| <dl> <span data-ttu-id="e31c2-120"><dt>**exemple de VFW \_ E \_ \_ rejeté**</dt></span><span class="sxs-lookup"><span data-stu-id="e31c2-120"><dt>**VFW\_E\_SAMPLE\_REJECTED**</dt></span></span> </dl> | <span data-ttu-id="e31c2-121">Le filtre supprime cet exemple.</span><span class="sxs-lookup"><span data-stu-id="e31c2-121">Filter is dropping this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e31c2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e31c2-122">Remarks</span></span>

<span data-ttu-id="e31c2-123">Le filtre appelle cette méthode à l’intérieur de la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) , avant d’afficher un exemple.</span><span class="sxs-lookup"><span data-stu-id="e31c2-123">The filter calls this method from inside the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, before it renders a sample.</span></span> <span data-ttu-id="e31c2-124">Si le filtre est en cours d’exécution, cette méthode planifie l’exemple de rendu.</span><span class="sxs-lookup"><span data-stu-id="e31c2-124">If the filter is running, this method schedules the sample for rendering.</span></span>

<span data-ttu-id="e31c2-125">Si le filtre a déjà un échantillon en attente, ou si la fin du flux a déjà été atteinte, la méthode retourne E \_ inattendue.</span><span class="sxs-lookup"><span data-stu-id="e31c2-125">If the filter already has a pending sample, or if the end-of-stream was already reached, the method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="e31c2-126">Le filtre en amont ne sérialise peut-être pas correctement ses appels de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="e31c2-126">Possibly the upstream filter is not serializing its streaming calls correctly.</span></span>

<span data-ttu-id="e31c2-127">Si l’algorithme de planification détermine que l’exemple doit être supprimé (voir [**CBaseRenderer :: ScheduleSample**](cbaserenderer-schedulesample.md)), la méthode retourne un échantillon de VFW \_ E \_ \_ rejeté.</span><span class="sxs-lookup"><span data-stu-id="e31c2-127">If the scheduling algorithm determines that the sample should be dropped (see [**CBaseRenderer::ScheduleSample**](cbaserenderer-schedulesample.md)), the method returns VFW\_E\_SAMPLE\_REJECTED.</span></span> <span data-ttu-id="e31c2-128">Toutefois, la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de la broche d’entrée ne transmet pas ce code d’erreur au filtre en amont, car la suppression d’un exemple n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="e31c2-128">However, the input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method does not pass this error code to the upstream filter, because dropping a sample is not an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31c2-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e31c2-129">Requirements</span></span>



| <span data-ttu-id="e31c2-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e31c2-130">Requirement</span></span> | <span data-ttu-id="e31c2-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e31c2-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31c2-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e31c2-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e31c2-133"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e31c2-133"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e31c2-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e31c2-134">Library</span></span><br/> | <dl> <span data-ttu-id="e31c2-135"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e31c2-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31c2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e31c2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31c2-137">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="e31c2-137">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




