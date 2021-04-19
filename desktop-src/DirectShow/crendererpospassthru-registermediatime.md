---
description: La méthode RegisterMediaTime met en cache les horodatages de l’échantillon actuel.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Méthode CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541082"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="827a6-103">Méthode CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="827a6-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="827a6-104">La méthode **RegisterMediaTime** met en cache les horodatages de l’échantillon actuel.</span><span class="sxs-lookup"><span data-stu-id="827a6-104">The **RegisterMediaTime** method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="827a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="827a6-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="827a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="827a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="827a6-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="827a6-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="827a6-108">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="827a6-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="827a6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="827a6-109">Return value</span></span>

<span data-ttu-id="827a6-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="827a6-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="827a6-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="827a6-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="827a6-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="827a6-112">Return code</span></span>                                                                                                  | <span data-ttu-id="827a6-113">Description</span><span class="sxs-lookup"><span data-stu-id="827a6-113">Description</span></span>                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="827a6-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="827a6-114"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="827a6-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="827a6-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="827a6-116"><dt>**\_heure du média VFW E \_ \_ \_ non \_ définie**</dt></span><span class="sxs-lookup"><span data-stu-id="827a6-116"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="827a6-117">L’exemple n’est pas horodaté.</span><span class="sxs-lookup"><span data-stu-id="827a6-117">The sample is not time-stamped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="827a6-118">Notes</span><span class="sxs-lookup"><span data-stu-id="827a6-118">Remarks</span></span>

<span data-ttu-id="827a6-119">Cette méthode stocke les horodatages de l’échantillon actuel.</span><span class="sxs-lookup"><span data-stu-id="827a6-119">This method stores the time stamps from the current sample.</span></span> <span data-ttu-id="827a6-120">La méthode [**CRendererPosPassThru :: GetMediaTime**](crendererpospassthru-getmediatime.md) récupère les mêmes valeurs.</span><span class="sxs-lookup"><span data-stu-id="827a6-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="827a6-121">Le filtre doit appeler cette méthode pour chaque exemple qu’il reçoit.</span><span class="sxs-lookup"><span data-stu-id="827a6-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="827a6-122">La méthode est surchargée pour accepter soit un pointeur vers l’exemple, soit les valeurs d’horodatage elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="827a6-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="827a6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="827a6-123">Requirements</span></span>



| <span data-ttu-id="827a6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="827a6-124">Requirement</span></span> | <span data-ttu-id="827a6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="827a6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="827a6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="827a6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="827a6-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="827a6-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="827a6-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="827a6-128">Library</span></span><br/> | <dl> <span data-ttu-id="827a6-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="827a6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




