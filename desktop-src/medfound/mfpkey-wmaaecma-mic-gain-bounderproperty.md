---
description: Spécifie si le DSP de capture vocale applique le délimitation du gain de microphone.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518140"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a><span data-ttu-id="680c0-103">Propriété de MFPKEY \_ WMAAECMA \_ MIC \_ gain \_</span><span class="sxs-lookup"><span data-stu-id="680c0-103">MFPKEY\_WMAAECMA\_MIC\_GAIN\_BOUNDER Property</span></span>

<span data-ttu-id="680c0-104">Spécifie si le DSP de capture vocale applique le délimitation du gain de microphone.</span><span class="sxs-lookup"><span data-stu-id="680c0-104">Specifies whether the Voice Capture DSP applies microphone gain bounding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="680c0-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="680c0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="680c0-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="680c0-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="680c0-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="680c0-107">Data Type</span></span>

<span data-ttu-id="680c0-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="680c0-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="680c0-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="680c0-109">Default Value</span></span>

<span data-ttu-id="680c0-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="680c0-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="680c0-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="680c0-111">Applies To</span></span>

-   [<span data-ttu-id="680c0-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="680c0-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="680c0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="680c0-113">Remarks</span></span>

<span data-ttu-id="680c0-114">Le gain de gain de microphone garantit que le microphone a le niveau de gain correct.</span><span class="sxs-lookup"><span data-stu-id="680c0-114">Microphone gain bounding ensures that the microphone has the correct level of gain.</span></span> <span data-ttu-id="680c0-115">Si le gain est trop élevé, le signal capturé peut être saturé et sera coupé.</span><span class="sxs-lookup"><span data-stu-id="680c0-115">If gain is too high, the captured signal might be saturated and will be clipped.</span></span> <span data-ttu-id="680c0-116">Le découpage est un effet non linéaire qui entraîne l’échec de l’algorithme d’annulation de l’écho acoustique (AEC).</span><span class="sxs-lookup"><span data-stu-id="680c0-116">Clipping is a non-linear effect, which will cause the acoustic echo cancellation (AEC) algorithm to fail.</span></span> <span data-ttu-id="680c0-117">Si le gain est trop faible, le rapport signal-bruit est faible, ce qui peut également entraîner l’échec ou l’inefficacité de l’algorithme AEC.</span><span class="sxs-lookup"><span data-stu-id="680c0-117">If the gain is too low, the signal-to-noise ratio is low, which can also cause the AEC algorithm to fail or not perform well.</span></span>

<span data-ttu-id="680c0-118">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="680c0-118">This property can have the following values.</span></span>



| <span data-ttu-id="680c0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="680c0-119">Value</span></span>          | <span data-ttu-id="680c0-120">Description</span><span class="sxs-lookup"><span data-stu-id="680c0-120">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="680c0-121">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="680c0-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="680c0-122">Activez le délimitation du gain de microphone.</span><span class="sxs-lookup"><span data-stu-id="680c0-122">Enable microphone gain bounding.</span></span>  |
| <span data-ttu-id="680c0-123">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="680c0-123">VARIANT\_FALSE</span></span> | <span data-ttu-id="680c0-124">Désactive le délimitation du gain de microphone.</span><span class="sxs-lookup"><span data-stu-id="680c0-124">Disable microphone gain bounding.</span></span> |



 

<span data-ttu-id="680c0-125">La valeur par défaut de cette propriété est \_ true (activé).</span><span class="sxs-lookup"><span data-stu-id="680c0-125">The default value of this property is VARIANT\_TRUE (enabled).</span></span>

<span data-ttu-id="680c0-126">Le délimitation du gain de microphone s’applique uniquement lorsque le DSP fonctionne en mode Source.</span><span class="sxs-lookup"><span data-stu-id="680c0-126">Microphone gain bounding is applies only when the DSP operates in source mode.</span></span> <span data-ttu-id="680c0-127">En mode filtre, l’application doit s’assurer que le microphone a le niveau de gain correct.</span><span class="sxs-lookup"><span data-stu-id="680c0-127">In filter mode, the application must ensure that the microphone has the correct gain level.</span></span>

## <a name="requirements"></a><span data-ttu-id="680c0-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="680c0-128">Requirements</span></span>



| <span data-ttu-id="680c0-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="680c0-129">Requirement</span></span> | <span data-ttu-id="680c0-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="680c0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="680c0-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680c0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="680c0-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680c0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="680c0-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680c0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="680c0-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680c0-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="680c0-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="680c0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="680c0-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="680c0-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="680c0-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="680c0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="680c0-138">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="680c0-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="680c0-139">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="680c0-139">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
