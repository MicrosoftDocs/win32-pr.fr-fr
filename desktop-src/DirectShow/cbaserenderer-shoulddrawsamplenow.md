---
description: La méthode ShouldDrawSampleNow détermine la façon dont un échantillon est planifié pour le rendu.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Méthode CBaseRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530016"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a><span data-ttu-id="915dd-103">Méthode CBaseRenderer. ShouldDrawSampleNow</span><span class="sxs-lookup"><span data-stu-id="915dd-103">CBaseRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="915dd-104">La `ShouldDrawSampleNow` méthode détermine la façon dont un échantillon est planifié pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="915dd-104">The `ShouldDrawSampleNow` method determines how a sample is scheduled for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="915dd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="915dd-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="915dd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="915dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="915dd-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="915dd-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="915dd-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="915dd-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="915dd-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="915dd-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="915dd-110">Pointeur vers une variable qui contient l’heure de début de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="915dd-110">Pointer to a variable that contains the sample's start time.</span></span>

</dd> <dt>

<span data-ttu-id="915dd-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="915dd-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="915dd-112">Pointeur vers une variable qui contient l’heure de fin de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="915dd-112">Pointer to a variable that contains the sample's end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="915dd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="915dd-113">Return value</span></span>

<span data-ttu-id="915dd-114">Retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="915dd-114">Returns S\_FALSE.</span></span> <span data-ttu-id="915dd-115">Si la classe dérivée se substitue à cette méthode, retournez l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="915dd-115">If the derived class overrides this method, return one of the values shown in the following table.</span></span>



| <span data-ttu-id="915dd-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="915dd-116">Return code</span></span>                                                                               | <span data-ttu-id="915dd-117">Description</span><span class="sxs-lookup"><span data-stu-id="915dd-117">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="915dd-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="915dd-119">L’exemple doit être rendu immédiatement.</span><span class="sxs-lookup"><span data-stu-id="915dd-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="915dd-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-120"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="915dd-121">L’exemple doit être planifié pour le rendu, en fonction des horodatages.</span><span class="sxs-lookup"><span data-stu-id="915dd-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="915dd-122"><dt>**Code d'erreur**</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-122"><dt>**Error code**</dt></span></span> </dl> | <span data-ttu-id="915dd-123">Ne rendez pas cet exemple.</span><span class="sxs-lookup"><span data-stu-id="915dd-123">Do not render this sample.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="915dd-124">Notes</span><span class="sxs-lookup"><span data-stu-id="915dd-124">Remarks</span></span>

<span data-ttu-id="915dd-125">La méthode [**CBaseRenderer :: GetSampleTimes**](cbaserenderer-getsampletimes.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="915dd-125">The [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method calls this method.</span></span> <span data-ttu-id="915dd-126">Par défaut, les exemples sont toujours planifiés pour le rendu en fonction de leur horodatage.</span><span class="sxs-lookup"><span data-stu-id="915dd-126">By default, samples are always scheduled for rendering based on their time stamps.</span></span> <span data-ttu-id="915dd-127">La classe dérivée peut substituer cette méthode. par exemple, pour implémenter le contrôle de qualité.</span><span class="sxs-lookup"><span data-stu-id="915dd-127">The derived class can override this method; for example, to implement quality control.</span></span>

## <a name="requirements"></a><span data-ttu-id="915dd-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="915dd-128">Requirements</span></span>



| <span data-ttu-id="915dd-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="915dd-129">Requirement</span></span> | <span data-ttu-id="915dd-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="915dd-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="915dd-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="915dd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="915dd-132"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="915dd-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="915dd-133">Library</span></span><br/> | <dl> <span data-ttu-id="915dd-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="915dd-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="915dd-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="915dd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915dd-136">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="915dd-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




