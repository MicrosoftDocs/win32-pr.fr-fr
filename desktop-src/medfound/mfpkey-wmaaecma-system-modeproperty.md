---
description: Définit le mode de traitement pour le DSP de capture vocale.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520494"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a><span data-ttu-id="af86d-103">\_Propriété du \_ mode système MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="af86d-103">MFPKEY\_WMAAECMA\_SYSTEM\_MODE Property</span></span>

<span data-ttu-id="af86d-104">Définit le mode de traitement pour le DSP de capture vocale.</span><span class="sxs-lookup"><span data-stu-id="af86d-104">Sets the processing mode for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="af86d-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="af86d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="af86d-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="af86d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="af86d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="af86d-107">Data Type</span></span>

<span data-ttu-id="af86d-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="af86d-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="af86d-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="af86d-109">Applies To</span></span>

-   [<span data-ttu-id="af86d-110">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="af86d-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="af86d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="af86d-111">Remarks</span></span>

<span data-ttu-id="af86d-112">La valeur de cette propriété est un membre de l’énumération du [ \_ \_ mode système AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .</span><span class="sxs-lookup"><span data-stu-id="af86d-112">The value of this property is a member of the [AEC\_SYSTEM\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) enumeration.</span></span>

<span data-ttu-id="af86d-113">La propriété doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="af86d-113">The property must be one of the following values.</span></span>



| <span data-ttu-id="af86d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="af86d-114">Value</span></span> | <span data-ttu-id="af86d-115">Description</span><span class="sxs-lookup"><span data-stu-id="af86d-115">Description</span></span>                                 |
|-------|---------------------------------------------|
| <span data-ttu-id="af86d-116">0</span><span class="sxs-lookup"><span data-stu-id="af86d-116">0</span></span>     | <span data-ttu-id="af86d-117">Mode d’annulation de l’écho audio (AEC) uniquement</span><span class="sxs-lookup"><span data-stu-id="af86d-117">Audio echo cancellation (AEC) only mode</span></span>     |
| <span data-ttu-id="af86d-118">2</span><span class="sxs-lookup"><span data-stu-id="af86d-118">2</span></span>     | <span data-ttu-id="af86d-119">Mode de traitement du tableau de microphone (carte) uniquement</span><span class="sxs-lookup"><span data-stu-id="af86d-119">Microphone array processing (MAP) only mode</span></span> |
| <span data-ttu-id="af86d-120">4</span><span class="sxs-lookup"><span data-stu-id="af86d-120">4</span></span>     | <span data-ttu-id="af86d-121">AEC et mode MAP</span><span class="sxs-lookup"><span data-stu-id="af86d-121">AEC and MAP mode</span></span>                            |
| <span data-ttu-id="af86d-122">5</span><span class="sxs-lookup"><span data-stu-id="af86d-122">5</span></span>     | <span data-ttu-id="af86d-123">Ni AEC ni mode MAP</span><span class="sxs-lookup"><span data-stu-id="af86d-123">Neither AEC nor MAP mode</span></span>                    |



 

<span data-ttu-id="af86d-124">Vous devez définir cette propriété avant d’utiliser le DSP de capture vocale.</span><span class="sxs-lookup"><span data-stu-id="af86d-124">You must set this property before using the Voice Capture DSP.</span></span> <span data-ttu-id="af86d-125">Une fois cette propriété définie, vous pouvez utiliser le DSP avec ses paramètres par défaut ou définir des propriétés supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="af86d-125">After you set this property, you can use the DSP with its default settings, or set additional properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="af86d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af86d-126">Requirements</span></span>



| <span data-ttu-id="af86d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af86d-127">Requirement</span></span> | <span data-ttu-id="af86d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="af86d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af86d-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af86d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="af86d-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af86d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="af86d-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af86d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="af86d-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af86d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af86d-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="af86d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="af86d-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af86d-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af86d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af86d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af86d-136">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af86d-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="af86d-137">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="af86d-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
