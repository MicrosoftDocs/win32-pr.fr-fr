---
description: Spécifie la taille de trame audio utilisée par le DSP de capture vocal.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: MFPKEY_WMAAECMA_FEATR_FRAME_SIZE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521457"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a><span data-ttu-id="670e5-103">\_Propriété de \_ taille de \_ trame MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="670e5-103">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE Property</span></span>

<span data-ttu-id="670e5-104">Spécifie la taille de trame audio utilisée par le DSP de capture vocal.</span><span class="sxs-lookup"><span data-stu-id="670e5-104">Specifies the audio frame size used by the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="670e5-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="670e5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="670e5-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="670e5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="670e5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="670e5-107">Data Type</span></span>

<span data-ttu-id="670e5-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="670e5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="670e5-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="670e5-109">Default Value</span></span>

<span data-ttu-id="670e5-110">0</span><span class="sxs-lookup"><span data-stu-id="670e5-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="670e5-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="670e5-111">Applies To</span></span>

-   [<span data-ttu-id="670e5-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="670e5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="670e5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="670e5-113">Remarks</span></span>

<span data-ttu-id="670e5-114">L’algorithme d’annulation de l’écho acoustique traite les échantillons audio PCM un frame à la fois.</span><span class="sxs-lookup"><span data-stu-id="670e5-114">The acoustic echo cancellation (AEC) algorithm processes PCM audio samples one frame at a time.</span></span> <span data-ttu-id="670e5-115">La valeur de cette propriété est la taille du cadre audio, en échantillons.</span><span class="sxs-lookup"><span data-stu-id="670e5-115">The value of this property is the size of the audio frame, in samples.</span></span> <span data-ttu-id="670e5-116">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="670e5-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="670e5-117">Le DSP de capture vocale prend en charge les tailles d’image suivantes :</span><span class="sxs-lookup"><span data-stu-id="670e5-117">The Voice Capture DSP supports the following frame sizes:</span></span>

-   <span data-ttu-id="670e5-118">80</span><span class="sxs-lookup"><span data-stu-id="670e5-118">80</span></span>
-   <span data-ttu-id="670e5-119">128</span><span class="sxs-lookup"><span data-stu-id="670e5-119">128</span></span>
-   <span data-ttu-id="670e5-120">160</span><span class="sxs-lookup"><span data-stu-id="670e5-120">160</span></span>
-   <span data-ttu-id="670e5-121">240</span><span class="sxs-lookup"><span data-stu-id="670e5-121">240</span></span>
-   <span data-ttu-id="670e5-122">256</span><span class="sxs-lookup"><span data-stu-id="670e5-122">256</span></span>
-   <span data-ttu-id="670e5-123">320</span><span class="sxs-lookup"><span data-stu-id="670e5-123">320</span></span>

<span data-ttu-id="670e5-124">Si la valeur de cette propriété est égale à zéro, le DSP sélectionne la taille de trame en fonction du mode système et du format de sortie.</span><span class="sxs-lookup"><span data-stu-id="670e5-124">If the value of this property is zero, the DSP selects the frame size based on the system mode and the output format.</span></span>

<span data-ttu-id="670e5-125">Toutefois, pour des performances optimales, il est recommandé que les applications utilisent la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="670e5-125">For the best performance, however, it is recommended that applications use the default value.</span></span> <span data-ttu-id="670e5-126">Si le mode de traitement est un tableau de microphones uniquement, la valeur par défaut est 320 exemples.</span><span class="sxs-lookup"><span data-stu-id="670e5-126">If the processing mode is microphone array only, the default value is 320 samples.</span></span> <span data-ttu-id="670e5-127">Pour tous les autres modes de traitement, la valeur par défaut est 160 exemples.</span><span class="sxs-lookup"><span data-stu-id="670e5-127">For all other processing modes, the default value is 160 samples.</span></span> <span data-ttu-id="670e5-128">Pour plus d’informations sur les modes de traitement du DSP de capture vocale, consultez [ \_ \_ \_ mode système MFPKEY WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md).</span><span class="sxs-lookup"><span data-stu-id="670e5-128">For more information about the processing modes of the Voice Capture DSP, see [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md).</span></span>

<span data-ttu-id="670e5-129">Après le premier appel à [**IMediaObject :: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) ou [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), vous pouvez lire cette propriété pour obtenir la taille de frame réelle en cours d’utilisation, même si le [**\_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA**](mfpkey-wmaaecma-feature-modeproperty.md) est false.</span><span class="sxs-lookup"><span data-stu-id="670e5-129">After the first call to [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) or [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), you can read this property to get the actual frame size in use, even when [**MFPKEY\_WMAAECMA\_FEATURE\_MODE**](mfpkey-wmaaecma-feature-modeproperty.md) is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="670e5-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="670e5-130">Requirements</span></span>



| <span data-ttu-id="670e5-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="670e5-131">Requirement</span></span> | <span data-ttu-id="670e5-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="670e5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="670e5-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="670e5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="670e5-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="670e5-134">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="670e5-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="670e5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="670e5-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="670e5-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="670e5-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="670e5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="670e5-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="670e5-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670e5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="670e5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670e5-140">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="670e5-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="670e5-141">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="670e5-141">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
