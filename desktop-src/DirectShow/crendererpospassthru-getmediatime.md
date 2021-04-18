---
description: La méthode GetMediaTime récupère les horodatages sur l’échantillon actuel.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Méthode CRendererPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533380"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="77fe3-103">Méthode CRendererPosPassThru. GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="77fe3-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="77fe3-104">La `GetMediaTime` méthode récupère les horodatages sur l’échantillon actuel.</span><span class="sxs-lookup"><span data-stu-id="77fe3-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="77fe3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77fe3-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="77fe3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77fe3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77fe3-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="77fe3-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="77fe3-108">Pointeur vers une variable qui reçoit l’heure de début, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="77fe3-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="77fe3-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="77fe3-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="77fe3-110">Pointeur vers une variable qui reçoit l’heure de fin, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="77fe3-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="77fe3-111">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="77fe3-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77fe3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77fe3-112">Return value</span></span>

<span data-ttu-id="77fe3-113">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77fe3-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="77fe3-114">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="77fe3-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="77fe3-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="77fe3-115">Return code</span></span>                                                                                  | <span data-ttu-id="77fe3-116">Description</span><span class="sxs-lookup"><span data-stu-id="77fe3-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="77fe3-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="77fe3-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="77fe3-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="77fe3-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="77fe3-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="77fe3-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="77fe3-120">La conversion vers ce format n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="77fe3-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="77fe3-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="77fe3-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="77fe3-122">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="77fe3-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="77fe3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="77fe3-123">Remarks</span></span>

<span data-ttu-id="77fe3-124">Cette méthode remplace la méthode [**CPosPassThru :: GetMediaTime**](cpospassthru-getmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="77fe3-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="77fe3-125">Les valeurs de date et d’heure sont converties au format d’heure actuel en appelant la méthode [**CPosPassThru :: ConvertTimeFormat**](cpospassthru-converttimeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="77fe3-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="77fe3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77fe3-126">Requirements</span></span>



| <span data-ttu-id="77fe3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77fe3-127">Requirement</span></span> | <span data-ttu-id="77fe3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="77fe3-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77fe3-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="77fe3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="77fe3-130"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77fe3-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="77fe3-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77fe3-131">Library</span></span><br/> | <dl> <span data-ttu-id="77fe3-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="77fe3-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




