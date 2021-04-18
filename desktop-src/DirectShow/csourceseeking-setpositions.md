---
description: 'La méthode SetPositions définit la position actuelle et la position d’arrêt. Cette méthode implémente la méthode IMediaSeeking :: SetPositions.'
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
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532875"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="c8e0a-104">Méthode CSourceSeeking. SetPositions</span><span class="sxs-lookup"><span data-stu-id="c8e0a-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="c8e0a-105">La `SetPositions` méthode définit la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c8e0a-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="c8e0a-106">Cette méthode implémente la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="c8e0a-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e0a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8e0a-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c8e0a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8e0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e0a-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="c8e0a-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e0a-110">Pointeur vers une variable qui spécifie la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="c8e0a-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="c8e0a-111">*CurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="c8e0a-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e0a-112">Combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="c8e0a-112">Bitwise combination of flags.</span></span> <span data-ttu-id="c8e0a-113">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c8e0a-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c8e0a-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="c8e0a-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e0a-115">Pointeur vers une variable qui spécifie l’heure d’arrêt, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="c8e0a-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="c8e0a-116">*StopFlags*</span><span class="sxs-lookup"><span data-stu-id="c8e0a-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e0a-117">Combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="c8e0a-117">Bitwise combination of flags.</span></span> <span data-ttu-id="c8e0a-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c8e0a-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e0a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8e0a-119">Return value</span></span>

<span data-ttu-id="c8e0a-120">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8e0a-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c8e0a-121">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8e0a-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="c8e0a-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c8e0a-122">Return code</span></span>                                                                                  | <span data-ttu-id="c8e0a-123">Description</span><span class="sxs-lookup"><span data-stu-id="c8e0a-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="c8e0a-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c8e0a-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c8e0a-125">Succès</span><span class="sxs-lookup"><span data-stu-id="c8e0a-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="c8e0a-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c8e0a-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c8e0a-127">Indicateurs non valides</span><span class="sxs-lookup"><span data-stu-id="c8e0a-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="c8e0a-128"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="c8e0a-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="c8e0a-129">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="c8e0a-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c8e0a-130">Notes</span><span class="sxs-lookup"><span data-stu-id="c8e0a-130">Remarks</span></span>

<span data-ttu-id="c8e0a-131">Les indicateurs suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="c8e0a-131">The following flags are supported:</span></span>

-   <span data-ttu-id="c8e0a-132">\_Recherche de \_ noposition</span><span class="sxs-lookup"><span data-stu-id="c8e0a-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="c8e0a-133">\_Recherche de \_ AbsolutePositioning</span><span class="sxs-lookup"><span data-stu-id="c8e0a-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="c8e0a-134">\_Recherche de \_ RelativePositioning</span><span class="sxs-lookup"><span data-stu-id="c8e0a-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="c8e0a-135">\_Recherche \_ de IncrementalPositioning (*pStop* uniquement)</span><span class="sxs-lookup"><span data-stu-id="c8e0a-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="c8e0a-136">Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="c8e0a-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="c8e0a-137">Cette méthode met à jour les valeurs des variables [**membres CSourceSeeking :: m \_ RtStart**](csourceseeking-m-rtstart.md) et [**CSourceSeeking :: m \_ rtStop**](csourceseeking-m-rtstop.md) , puis appelle les méthodes virtuelles pures [**CSourceSeeking :: modifiez l'**](csourceseeking-changestart.md) et [**CSourceSeeking :: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="c8e0a-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e0a-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8e0a-138">Requirements</span></span>



| <span data-ttu-id="c8e0a-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8e0a-139">Requirement</span></span> | <span data-ttu-id="c8e0a-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8e0a-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e0a-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8e0a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="c8e0a-142"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8e0a-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8e0a-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c8e0a-143">Library</span></span><br/> | <dl> <span data-ttu-id="c8e0a-144"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c8e0a-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8e0a-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8e0a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e0a-146">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="c8e0a-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




