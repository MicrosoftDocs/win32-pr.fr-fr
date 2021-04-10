---
description: Spécifie le mode de contrôle de la section. Les valeurs valides sont 0, 1 et 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: CODECAPI_AVEncSliceControlMode, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950903"
---
# <a name="codecapi_avencslicecontrolmode-property"></a><span data-ttu-id="af569-104">CODECAPI \_ propriété AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="af569-104">CODECAPI\_AVEncSliceControlMode property</span></span>

<span data-ttu-id="af569-105">Spécifie le mode de contrôle de la section.</span><span class="sxs-lookup"><span data-stu-id="af569-105">Specifies the slice control mode.</span></span> <span data-ttu-id="af569-106">Les valeurs valides sont 0, 1 et 2.</span><span class="sxs-lookup"><span data-stu-id="af569-106">Valid values are 0, 1, and 2.</span></span>

## <a name="data-type"></a><span data-ttu-id="af569-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="af569-107">Data type</span></span>

<span data-ttu-id="af569-108">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="af569-108">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="af569-109">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="af569-109">Property GUID</span></span>

<span data-ttu-id="af569-110">**CODECAPI \_ AVEncSliceControlMode**</span><span class="sxs-lookup"><span data-stu-id="af569-110">**CODECAPI\_AVEncSliceControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="af569-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="af569-111">Property value</span></span>

<span data-ttu-id="af569-112">Valeurs du mode de contrôle Slice :</span><span class="sxs-lookup"><span data-stu-id="af569-112">Slice control mode values:</span></span>



| <span data-ttu-id="af569-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="af569-113">Value</span></span>                                                                        | <span data-ttu-id="af569-114">Signification</span><span class="sxs-lookup"><span data-stu-id="af569-114">Meaning</span></span>                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af569-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="af569-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="af569-116">Si cette valeur est définie sur 0, cela signifie que la propriété [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) spécifie la taille de la tranche en unités de blocs macros par tranche.</span><span class="sxs-lookup"><span data-stu-id="af569-116">Setting this value to 0 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblocks per slice.</span></span><br/>     |
| <dl> <span data-ttu-id="af569-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="af569-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="af569-118">Si la valeur 1 est définie, la propriété [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) spécifie la taille de la tranche en unités de bits par tranche.</span><span class="sxs-lookup"><span data-stu-id="af569-118">Setting this value to 1 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of bits per slice.</span></span><br/>            |
| <dl> <span data-ttu-id="af569-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="af569-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="af569-120">Si cette valeur est définie sur 2, la propriété [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) spécifie la taille de la tranche en unités de lignes bloc macro par tranche.</span><span class="sxs-lookup"><span data-stu-id="af569-120">Setting this value to 2 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblock rows per slice.</span></span><br/> |



 

<span data-ttu-id="af569-121">L’encodeur retourne les valeurs qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="af569-121">The encoder returns the values that it supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="af569-122">Notes</span><span class="sxs-lookup"><span data-stu-id="af569-122">Remarks</span></span>

<span data-ttu-id="af569-123">**Encodeurs H. 264/AVC :**</span><span class="sxs-lookup"><span data-stu-id="af569-123">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="af569-124">Il est recommandé que l’encodeur prenne en charge [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)et [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="af569-124">It is recommended that the encoder supports [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="af569-125">Si [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) n’est pas appelé pour CODECAPI \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) pour CODECAPI \_ AVEncSliceControlMode peut retourner **VFW \_ E \_ CODECAPI \_ aucune \_ \_ valeur actuelle**.</span><span class="sxs-lookup"><span data-stu-id="af569-125">If [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) is not called for CODECAPI\_AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) for CODECAPI\_AVEncSliceControlMode can return **VFW\_E\_CODECAPI\_NO\_CURRENT\_VALUE**.</span></span> <span data-ttu-id="af569-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) peut retourner **VFW \_ E \_ CODECAPI \_ pas de \_ valeur par défaut** pour CODECAPI \_ AVEncSliceControlMode.</span><span class="sxs-lookup"><span data-stu-id="af569-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) may return **VFW\_E\_CODECAPI\_NO\_DEFAULT** for CODECAPI\_AVEncSliceControlMode.</span></span>

<span data-ttu-id="af569-127">La valeur par défaut recommandée est 2 (taille en Mo par tranche).</span><span class="sxs-lookup"><span data-stu-id="af569-127">Recommended default value is 2 (size in MB row per slice).</span></span>

<span data-ttu-id="af569-128">Il s’agit d’une API statique, ce qui signifie que l’application a gagné la modification pendant que l’encodeur est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="af569-128">This is a static API, which means the application won t change this while the encoder is running.</span></span>

## <a name="examples"></a><span data-ttu-id="af569-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="af569-129">Examples</span></span>


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a><span data-ttu-id="af569-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af569-130">Requirements</span></span>



| <span data-ttu-id="af569-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af569-131">Requirement</span></span> | <span data-ttu-id="af569-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="af569-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af569-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af569-133">Minimum supported client</span></span><br/> | <span data-ttu-id="af569-134">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="af569-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="af569-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af569-135">Minimum supported server</span></span><br/> | <span data-ttu-id="af569-136">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="af569-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="af569-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="af569-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="af569-138"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="af569-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af569-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af569-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af569-140">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af569-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

