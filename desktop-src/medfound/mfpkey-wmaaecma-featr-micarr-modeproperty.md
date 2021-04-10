---
description: Spécifie comment le DSP de capture vocale effectue le traitement du tableau de microphone.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: MFPKEY_WMAAECMA_FEATR_MICARR_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201885"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a><span data-ttu-id="38cb5-103">\_Propriété du \_ \_ mode MICARR MFPKEY WMAAECMA Feature \_</span><span class="sxs-lookup"><span data-stu-id="38cb5-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property</span></span>

<span data-ttu-id="38cb5-104">Spécifie comment le DSP de capture vocale effectue le traitement du tableau de microphone.</span><span class="sxs-lookup"><span data-stu-id="38cb5-104">Specifies how the Voice Capture DSP performs microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="38cb5-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="38cb5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="38cb5-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="38cb5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="38cb5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="38cb5-107">Data Type</span></span>

<span data-ttu-id="38cb5-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="38cb5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="38cb5-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="38cb5-109">Default Value</span></span>

<span data-ttu-id="38cb5-110">MICARRAY \_ un seul \_ faisceau</span><span class="sxs-lookup"><span data-stu-id="38cb5-110">MICARRAY\_SINGLE\_BEAM</span></span>

## <a name="applies-to"></a><span data-ttu-id="38cb5-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="38cb5-111">Applies To</span></span>

-   [<span data-ttu-id="38cb5-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="38cb5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="38cb5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="38cb5-113">Remarks</span></span>

<span data-ttu-id="38cb5-114">La valeur de cette propriété est un membre de l’énumération du [ \_ \_ mode de tableau MIC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) .</span><span class="sxs-lookup"><span data-stu-id="38cb5-114">The value of this property is a member of the [MIC\_ARRAY\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) enumeration.</span></span> <span data-ttu-id="38cb5-115">La valeur par défaut est MICARRAY \_ simple \_ Beam.</span><span class="sxs-lookup"><span data-stu-id="38cb5-115">The default value is MICARRAY\_SINGLE\_BEAM.</span></span> <span data-ttu-id="38cb5-116">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="38cb5-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="38cb5-117">Le DSP utilise cette propriété uniquement lorsque le traitement du tableau du microphone est activé.</span><span class="sxs-lookup"><span data-stu-id="38cb5-117">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="38cb5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38cb5-118">Requirements</span></span>



| <span data-ttu-id="38cb5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38cb5-119">Requirement</span></span> | <span data-ttu-id="38cb5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="38cb5-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38cb5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38cb5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="38cb5-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38cb5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="38cb5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38cb5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="38cb5-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38cb5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38cb5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="38cb5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="38cb5-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="38cb5-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38cb5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38cb5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38cb5-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="38cb5-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="38cb5-129">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="38cb5-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
