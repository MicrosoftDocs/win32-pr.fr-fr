---
description: La méthode GetSampleTimes récupère les horodatages d’un exemple.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Méthode CBaseRenderer. GetSampleTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523520"
---
# <a name="cbaserenderergetsampletimes-method"></a><span data-ttu-id="b5cdd-103">Méthode CBaseRenderer. GetSampleTimes</span><span class="sxs-lookup"><span data-stu-id="b5cdd-103">CBaseRenderer.GetSampleTimes method</span></span>

<span data-ttu-id="b5cdd-104">La `GetSampleTimes` méthode récupère les horodatages d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-104">The `GetSampleTimes` method retrieves the time stamps from a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cdd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5cdd-105">Syntax</span></span>


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="b5cdd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5cdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cdd-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="b5cdd-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b5cdd-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b5cdd-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="b5cdd-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="b5cdd-110">Pointeur vers une variable qui reçoit l’heure de début.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-110">Pointer to a variable that receives the start time.</span></span>

</dd> <dt>

<span data-ttu-id="b5cdd-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="b5cdd-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="b5cdd-112">Pointeur vers une variable qui reçoit l’heure de fin.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-112">Pointer to a variable that receives the end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cdd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5cdd-113">Return value</span></span>

<span data-ttu-id="b5cdd-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5cdd-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b5cdd-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b5cdd-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b5cdd-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b5cdd-116">Return code</span></span>                                                                                                    | <span data-ttu-id="b5cdd-117">Description</span><span class="sxs-lookup"><span data-stu-id="b5cdd-117">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5cdd-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b5cdd-118"><dt>**S\_OK**</dt></span></span> </dl>                           | <span data-ttu-id="b5cdd-119">L’exemple doit être rendu immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="b5cdd-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b5cdd-120"><dt>**S\_FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="b5cdd-121">L’exemple doit être planifié pour le rendu, en fonction des horodatages.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="b5cdd-122"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="b5cdd-122"><dt>**E\_FAIL**</dt></span></span> </dl>                         | <span data-ttu-id="b5cdd-123">Ne rendez pas cet exemple.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-123">Do not render this sample.</span></span><br/>                                              |
| <dl> <span data-ttu-id="b5cdd-124"><dt>**VFW \_ E \_ heure de début \_ \_ après la \_ fin**</dt></span><span class="sxs-lookup"><span data-stu-id="b5cdd-124"><dt>**VFW\_E\_START\_TIME\_AFTER\_END**</dt></span></span> </dl> | <span data-ttu-id="b5cdd-125">Horodatage incorrect : l’heure de fin est antérieure à l’heure de début.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-125">Bad time stamp: The end time is earlier than the start time.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="b5cdd-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b5cdd-126">Remarks</span></span>

<span data-ttu-id="b5cdd-127">Le filtre appelle cette méthode pour déterminer comment il doit gérer un exemple.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-127">The filter calls this method to determine how it should handle a sample.</span></span> <span data-ttu-id="b5cdd-128">Si la valeur de retour est \_ OK, le filtre restitue l’exemple immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-128">If the return value is S\_OK, the filter renders the sample immediately.</span></span> <span data-ttu-id="b5cdd-129">Si la valeur de retour est \_ false, le filtre planifie l’exemple de rendu en fonction des horodatages.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-129">If the return value is S\_FALSE, the filter schedules the sample for rendering, based on the time stamps.</span></span> <span data-ttu-id="b5cdd-130">Si la valeur de retour est un code d’erreur, le filtre rejette l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-130">If the return value is an error code, the filter rejects the sample.</span></span>

<span data-ttu-id="b5cdd-131">Cette méthode retourne S \_ OK si l’exemple n’a pas de datage ou si le filtre n’a pas d’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-131">This method returns S\_OK if the sample has no time stamps, or if the filter does not have a reference clock.</span></span> <span data-ttu-id="b5cdd-132">Sinon, elle retourne la valeur de la méthode [**CBaseRenderer :: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) .</span><span class="sxs-lookup"><span data-stu-id="b5cdd-132">Otherwise, it returns the value of the [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) method.</span></span> <span data-ttu-id="b5cdd-133">Dans la classe de base, **ShouldDrawSampleNow** retourne toujours S \_ false.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-133">In the base class, **ShouldDrawSampleNow** always returns S\_FALSE.</span></span> <span data-ttu-id="b5cdd-134">La classe dérivée peut substituer ce comportement.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-134">The derived class can override this behavior.</span></span> <span data-ttu-id="b5cdd-135">Par exemple, si la classe dérivée implémente la gestion du contrôle de qualité, elle peut retourner E \_ Fail pour supprimer un exemple.</span><span class="sxs-lookup"><span data-stu-id="b5cdd-135">For example, if the derived class implements quality control management, it might return E\_FAIL to drop a sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cdd-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5cdd-136">Requirements</span></span>



| <span data-ttu-id="b5cdd-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5cdd-137">Requirement</span></span> | <span data-ttu-id="b5cdd-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5cdd-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cdd-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5cdd-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b5cdd-140"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5cdd-140"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b5cdd-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5cdd-141">Library</span></span><br/> | <dl> <span data-ttu-id="b5cdd-142"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b5cdd-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5cdd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5cdd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cdd-144">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="b5cdd-144">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




