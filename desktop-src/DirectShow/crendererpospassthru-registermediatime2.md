---
description: La méthode RegisterMediaTime met en cache les horodatages de l’échantillon actuel. Cette méthode utilise les paramètres *StartTime* et *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: CRendererPosPassThru. RegisterMediaTime, méthode (Ctlutil. h)-StartTime et EndTime, paramètres
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
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106540125"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a><span data-ttu-id="f0cbf-104">CRendererPosPassThru. RegisterMediaTime, méthode (Ctlutil. h)-StartTime et EndTime, paramètres</span><span class="sxs-lookup"><span data-stu-id="f0cbf-104">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h) - StartTime and EndTime parameters</span></span>

<span data-ttu-id="f0cbf-105">La méthode [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) met en cache les horodatages de l’échantillon actuel.</span><span class="sxs-lookup"><span data-stu-id="f0cbf-105">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0cbf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0cbf-106">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="f0cbf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0cbf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0cbf-108">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="f0cbf-108">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f0cbf-109">Heure de début de l’exemple, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="f0cbf-109">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="f0cbf-110">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="f0cbf-110">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f0cbf-111">Heure de fin de l’échantillon, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="f0cbf-111">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0cbf-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0cbf-112">Return value</span></span>

<span data-ttu-id="f0cbf-113">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0cbf-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f0cbf-114">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0cbf-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="f0cbf-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f0cbf-115">Return code</span></span>                                                                          | <span data-ttu-id="f0cbf-116">Description</span><span class="sxs-lookup"><span data-stu-id="f0cbf-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f0cbf-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0cbf-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f0cbf-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f0cbf-118">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0cbf-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f0cbf-119">Remarks</span></span>

<span data-ttu-id="f0cbf-120">Cette méthode stocke les valeurs d’horodatage indiquées dans *StartTime* et *EndTime*.</span><span class="sxs-lookup"><span data-stu-id="f0cbf-120">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="f0cbf-121">La méthode [**CRendererPosPassThru :: GetMediaTime**](crendererpospassthru-getmediatime.md) récupère les mêmes valeurs.</span><span class="sxs-lookup"><span data-stu-id="f0cbf-121">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="f0cbf-122">Le filtre doit appeler cette méthode pour chaque exemple qu’il reçoit.</span><span class="sxs-lookup"><span data-stu-id="f0cbf-122">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="f0cbf-123">La méthode est surchargée pour accepter soit un pointeur vers l’exemple, soit les valeurs d’horodatage elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="f0cbf-123">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0cbf-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0cbf-124">Requirements</span></span>



| <span data-ttu-id="f0cbf-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0cbf-125">Requirement</span></span> | <span data-ttu-id="f0cbf-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0cbf-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0cbf-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0cbf-127">Header</span></span>  | <span data-ttu-id="f0cbf-128">Ctlutil. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="f0cbf-128">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="f0cbf-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0cbf-129">Library</span></span> | <span data-ttu-id="f0cbf-130">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="f0cbf-130">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




