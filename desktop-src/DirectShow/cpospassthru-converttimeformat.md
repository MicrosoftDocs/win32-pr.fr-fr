---
description: 'Méthode CPosPassThru. ConvertTimeFormat : la méthode ConvertTimeFormat convertit d’un format d’heure en un autre. Cette méthode implémente la méthode IMediaSeeking :: ConvertTimeFormat.'
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
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098957"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="c2187-104">Méthode CPosPassThru. ConvertTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c2187-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="c2187-105">La `ConvertTimeFormat` méthode convertit d’un format d’heure en un autre.</span><span class="sxs-lookup"><span data-stu-id="c2187-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="c2187-106">Cette méthode implémente la méthode [**IMediaSeeking :: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="c2187-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2187-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2187-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="c2187-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2187-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2187-109">*pTarget*</span><span class="sxs-lookup"><span data-stu-id="c2187-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="c2187-110">Pointeur vers une variable qui reçoit l’heure convertie.</span><span class="sxs-lookup"><span data-stu-id="c2187-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="c2187-111">*pTargetFormat*</span><span class="sxs-lookup"><span data-stu-id="c2187-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c2187-112">Pointeur vers le GUID du format d’heure du format cible.</span><span class="sxs-lookup"><span data-stu-id="c2187-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="c2187-113">Si la **valeur est null**, le format actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c2187-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="c2187-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="c2187-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="c2187-115">Valeur de temps à convertir.</span><span class="sxs-lookup"><span data-stu-id="c2187-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="c2187-116">*pSourceFormat*</span><span class="sxs-lookup"><span data-stu-id="c2187-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c2187-117">Pointeur vers le GUID du format d’heure du format à convertir.</span><span class="sxs-lookup"><span data-stu-id="c2187-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="c2187-118">Si la **valeur est null**, le format actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c2187-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2187-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c2187-119">Return value</span></span>

<span data-ttu-id="c2187-120">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="c2187-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2187-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2187-121">Requirements</span></span>



| <span data-ttu-id="c2187-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2187-122">Requirement</span></span> | <span data-ttu-id="c2187-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2187-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2187-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2187-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c2187-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2187-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c2187-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2187-126">Library</span></span><br/> | <dl> <span data-ttu-id="c2187-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c2187-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2187-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2187-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2187-129">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="c2187-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="c2187-130">**GUID de format d’heure**</span><span class="sxs-lookup"><span data-stu-id="c2187-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




