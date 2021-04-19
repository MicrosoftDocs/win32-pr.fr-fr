---
description: Spécifie si le DSP de capture vocale effectue une suppression du bruit.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: MFPKEY_WMAAECMA_FEATR_NS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524531"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a><span data-ttu-id="aa84c-103">\_Propriété NS de MFPKEY WMAAECMA \_ Feature \_</span><span class="sxs-lookup"><span data-stu-id="aa84c-103">MFPKEY\_WMAAECMA\_FEATR\_NS Property</span></span>

<span data-ttu-id="aa84c-104">Spécifie si le DSP de capture vocale effectue une suppression du bruit.</span><span class="sxs-lookup"><span data-stu-id="aa84c-104">Specifies whether the Voice Capture DSP performs noise suppression.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="aa84c-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="aa84c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="aa84c-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="aa84c-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="aa84c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="aa84c-107">Data Type</span></span>

<span data-ttu-id="aa84c-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="aa84c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="aa84c-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="aa84c-109">Default Value</span></span>

<span data-ttu-id="aa84c-110">1</span><span class="sxs-lookup"><span data-stu-id="aa84c-110">1</span></span>

## <a name="applies-to"></a><span data-ttu-id="aa84c-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="aa84c-111">Applies To</span></span>

-   [<span data-ttu-id="aa84c-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="aa84c-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="aa84c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="aa84c-113">Remarks</span></span>

<span data-ttu-id="aa84c-114">La suppression du bruit est un composant DSP (Digital Signal Processing) qui supprime ou réduit le bruit d’arrière-plan stationnaire dans le signal audio.</span><span class="sxs-lookup"><span data-stu-id="aa84c-114">Noise suppression is a digital signal processing (DSP) component that suppresses or reduces stationary background noise in the audio signal.</span></span> <span data-ttu-id="aa84c-115">La suppression du bruit est appliquée après le traitement de l’annulation de l’écho acoustique (AEC) et du tableau du microphone.</span><span class="sxs-lookup"><span data-stu-id="aa84c-115">Noise suppression is applied after the acoustic echo cancellation (AEC) and microphone array processing.</span></span>

<span data-ttu-id="aa84c-116">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="aa84c-116">This property can have the following values.</span></span>



| <span data-ttu-id="aa84c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa84c-117">Value</span></span> | <span data-ttu-id="aa84c-118">Description</span><span class="sxs-lookup"><span data-stu-id="aa84c-118">Description</span></span>                |
|-------|----------------------------|
| <span data-ttu-id="aa84c-119">0</span><span class="sxs-lookup"><span data-stu-id="aa84c-119">0</span></span>     | <span data-ttu-id="aa84c-120">Désactivez la suppression du bruit.</span><span class="sxs-lookup"><span data-stu-id="aa84c-120">Disable noise suppression.</span></span> |
| <span data-ttu-id="aa84c-121">1</span><span class="sxs-lookup"><span data-stu-id="aa84c-121">1</span></span>     | <span data-ttu-id="aa84c-122">Activez la suppression du bruit.</span><span class="sxs-lookup"><span data-stu-id="aa84c-122">Enable noise suppression.</span></span>  |



 

<span data-ttu-id="aa84c-123">La valeur par défaut de cette propriété est 1 (activé).</span><span class="sxs-lookup"><span data-stu-id="aa84c-123">The default value of this property is 1 (enabled).</span></span> <span data-ttu-id="aa84c-124">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="aa84c-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa84c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa84c-125">Requirements</span></span>



| <span data-ttu-id="aa84c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa84c-126">Requirement</span></span> | <span data-ttu-id="aa84c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa84c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa84c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa84c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aa84c-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa84c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aa84c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa84c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aa84c-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa84c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa84c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa84c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa84c-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa84c-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa84c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa84c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa84c-135">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aa84c-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="aa84c-136">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="aa84c-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
