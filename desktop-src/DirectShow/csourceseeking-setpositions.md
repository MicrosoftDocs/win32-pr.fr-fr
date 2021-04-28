---
description: 'Méthode CSourceSeeking. SetPositions : la méthode SetPositions définit la position actuelle et la position d’arrêt. Cette méthode implémente la méthode IMediaSeeking :: SetPositions.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Méthode CSourceSeeking. SetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b09dd92b97166b8d973328ec95e466abbda116bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085167"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="27cd3-104">Méthode CSourceSeeking. SetPositions</span><span class="sxs-lookup"><span data-stu-id="27cd3-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="27cd3-105">La `SetPositions` méthode définit la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="27cd3-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="27cd3-106">Cette méthode implémente la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="27cd3-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="27cd3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27cd3-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="27cd3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27cd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27cd3-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="27cd3-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="27cd3-110">Pointeur vers une variable qui spécifie la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="27cd3-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="27cd3-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="27cd3-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="27cd3-112">Combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="27cd3-112">Bitwise combination of flags.</span></span> <span data-ttu-id="27cd3-113">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="27cd3-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="27cd3-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="27cd3-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="27cd3-115">Pointeur vers une variable qui spécifie l’heure d’arrêt, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="27cd3-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="27cd3-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="27cd3-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="27cd3-117">Combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="27cd3-117">Bitwise combination of flags.</span></span> <span data-ttu-id="27cd3-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="27cd3-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27cd3-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27cd3-119">Return value</span></span>

<span data-ttu-id="27cd3-120">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27cd3-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="27cd3-121">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="27cd3-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="27cd3-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="27cd3-122">Return code</span></span>                                                                                  | <span data-ttu-id="27cd3-123">Description</span><span class="sxs-lookup"><span data-stu-id="27cd3-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="27cd3-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27cd3-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="27cd3-125">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="27cd3-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="27cd3-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="27cd3-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="27cd3-127">Indicateurs non valides</span><span class="sxs-lookup"><span data-stu-id="27cd3-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="27cd3-128"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="27cd3-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="27cd3-129">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="27cd3-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27cd3-130">Notes </span><span class="sxs-lookup"><span data-stu-id="27cd3-130">Remarks</span></span>

<span data-ttu-id="27cd3-131">Les indicateurs suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="27cd3-131">The following flags are supported:</span></span>

-   <span data-ttu-id="27cd3-132">\_Recherche de \_ noposition</span><span class="sxs-lookup"><span data-stu-id="27cd3-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="27cd3-133">\_Recherche de \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="27cd3-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="27cd3-134">\_Recherche de \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="27cd3-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="27cd3-135">\_Recherche \_ de IncrementalPositioning (*pStop* uniquement)</span><span class="sxs-lookup"><span data-stu-id="27cd3-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="27cd3-136">Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="27cd3-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="27cd3-137">Cette méthode met à jour les valeurs des variables [**membres CSourceSeeking :: m \_ RtStart**](csourceseeking-m-rtstart.md) et [**CSourceSeeking :: m \_ rtStop**](csourceseeking-m-rtstop.md) , puis appelle les méthodes virtuelles pures [**CSourceSeeking :: modifiez l'**](csourceseeking-changestart.md) et [**CSourceSeeking :: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="27cd3-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27cd3-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27cd3-138">Requirements</span></span>



| <span data-ttu-id="27cd3-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27cd3-139">Requirement</span></span> | <span data-ttu-id="27cd3-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="27cd3-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27cd3-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="27cd3-141">Header</span></span><br/>  | <dl> <span data-ttu-id="27cd3-142"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27cd3-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="27cd3-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="27cd3-143">Library</span></span><br/> | <dl> <span data-ttu-id="27cd3-144"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="27cd3-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27cd3-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27cd3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27cd3-146">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="27cd3-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




