---
description: 'La méthode ConvertTimeFormat convertit d’un format d’heure en un autre. Cette méthode implémente la méthode IMediaSeeking :: ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Méthode CSourceSeeking. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520829"
---
# <a name="csourceseekingconverttimeformat-method"></a><span data-ttu-id="d3eb7-104">Méthode CSourceSeeking. ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d3eb7-104">CSourceSeeking.ConvertTimeFormat method</span></span>

<span data-ttu-id="d3eb7-105">La `ConvertTimeFormat` méthode convertit d’un format d’heure en un autre.</span><span class="sxs-lookup"><span data-stu-id="d3eb7-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="d3eb7-106">Cette méthode implémente la méthode [**IMediaSeeking :: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="d3eb7-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3eb7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3eb7-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d3eb7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3eb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3eb7-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="d3eb7-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="d3eb7-110">Pointeur vers une variable qui reçoit l’heure convertie.</span><span class="sxs-lookup"><span data-stu-id="d3eb7-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="d3eb7-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="d3eb7-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d3eb7-112">Pointeur vers le GUID du format cible.</span><span class="sxs-lookup"><span data-stu-id="d3eb7-112">Pointer to the GUID of the target format.</span></span> <span data-ttu-id="d3eb7-113">Si la **valeur est null**, le format actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d3eb7-113">If **NULL**, the current format is used.</span></span> <span data-ttu-id="d3eb7-114">Consultez [**GUID de format d’heure**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d3eb7-114">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3eb7-115">*Source*</span><span class="sxs-lookup"><span data-stu-id="d3eb7-115">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="d3eb7-116">Valeur de temps à convertir.</span><span class="sxs-lookup"><span data-stu-id="d3eb7-116">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="d3eb7-117">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="d3eb7-117">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d3eb7-118">Pointeur vers le GUID du format d’heure du format à convertir.</span><span class="sxs-lookup"><span data-stu-id="d3eb7-118">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="d3eb7-119">Si la **valeur est null**, le format actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d3eb7-119">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3eb7-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3eb7-120">Return value</span></span>

<span data-ttu-id="d3eb7-121">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d3eb7-121">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d3eb7-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d3eb7-122">Return code</span></span>                                                                                  | <span data-ttu-id="d3eb7-123">Description</span><span class="sxs-lookup"><span data-stu-id="d3eb7-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="d3eb7-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d3eb7-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d3eb7-125">Succès</span><span class="sxs-lookup"><span data-stu-id="d3eb7-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="d3eb7-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d3eb7-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d3eb7-127">Argument non valide</span><span class="sxs-lookup"><span data-stu-id="d3eb7-127">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="d3eb7-128"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d3eb7-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="d3eb7-129">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="d3eb7-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3eb7-130">Notes</span><span class="sxs-lookup"><span data-stu-id="d3eb7-130">Remarks</span></span>

<span data-ttu-id="d3eb7-131">Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).</span><span class="sxs-lookup"><span data-stu-id="d3eb7-131">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span> <span data-ttu-id="d3eb7-132">Cette méthode retourne E \_ INVALIDARG, sauf dans le cas trivial où *PTargetFormat* et *pSourceFormat* spécifient tous deux le temps de \_ format du \_ média \_ .</span><span class="sxs-lookup"><span data-stu-id="d3eb7-132">This method returns E\_INVALIDARG, except in the trivial case where *pTargetFormat* and *pSourceFormat* both specify TIME\_FORMAT\_MEDIA\_TIME.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3eb7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3eb7-133">Requirements</span></span>



| <span data-ttu-id="d3eb7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3eb7-134">Requirement</span></span> | <span data-ttu-id="d3eb7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3eb7-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3eb7-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d3eb7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d3eb7-137"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3eb7-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3eb7-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d3eb7-138">Library</span></span><br/> | <dl> <span data-ttu-id="d3eb7-139"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d3eb7-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3eb7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3eb7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3eb7-141">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="d3eb7-141">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




