---
description: 'La méthode ConvertTimeFormat convertit d’un format d’heure en un autre. Cette méthode implémente la méthode IMediaSeeking :: ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Méthode CPosPassThru. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526331"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="1e3f6-104">Méthode CPosPassThru. ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1e3f6-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="1e3f6-105">La `ConvertTimeFormat` méthode convertit d’un format d’heure en un autre.</span><span class="sxs-lookup"><span data-stu-id="1e3f6-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="1e3f6-106">Cette méthode implémente la méthode [**IMediaSeeking :: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="1e3f6-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e3f6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e3f6-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="1e3f6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e3f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e3f6-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="1e3f6-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="1e3f6-110">Pointeur vers une variable qui reçoit l’heure convertie.</span><span class="sxs-lookup"><span data-stu-id="1e3f6-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="1e3f6-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="1e3f6-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="1e3f6-112">Pointeur vers le GUID du format d’heure du format cible.</span><span class="sxs-lookup"><span data-stu-id="1e3f6-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="1e3f6-113">Si la **valeur est null**, le format actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1e3f6-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="1e3f6-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="1e3f6-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="1e3f6-115">Valeur de temps à convertir.</span><span class="sxs-lookup"><span data-stu-id="1e3f6-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="1e3f6-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="1e3f6-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="1e3f6-117">Pointeur vers le GUID du format d’heure du format à convertir.</span><span class="sxs-lookup"><span data-stu-id="1e3f6-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="1e3f6-118">Si la **valeur est null**, le format actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1e3f6-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e3f6-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e3f6-119">Return value</span></span>

<span data-ttu-id="1e3f6-120">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="1e3f6-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e3f6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e3f6-121">Requirements</span></span>



| <span data-ttu-id="1e3f6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e3f6-122">Requirement</span></span> | <span data-ttu-id="1e3f6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e3f6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e3f6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e3f6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1e3f6-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e3f6-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e3f6-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e3f6-126">Library</span></span><br/> | <dl> <span data-ttu-id="1e3f6-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1e3f6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e3f6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e3f6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e3f6-129">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="1e3f6-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="1e3f6-130">**GUID de format d’heure**</span><span class="sxs-lookup"><span data-stu-id="1e3f6-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




