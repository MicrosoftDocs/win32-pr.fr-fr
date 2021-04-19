---
description: Spécifie la poutre que le DSP de capture vocale utilise pour le traitement du tableau de microphone.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: MFPKEY_WMAAECMA_FEATR_MICARR_BEAM, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517741"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a><span data-ttu-id="ce389-103">MFPKEY \_ WMAAECMA \_ Feature \_ MICARR \_ Beam, propriété</span><span class="sxs-lookup"><span data-stu-id="ce389-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_BEAM Property</span></span>

<span data-ttu-id="ce389-104">Spécifie la poutre que le DSP de capture vocale utilise pour le traitement du tableau de microphone.</span><span class="sxs-lookup"><span data-stu-id="ce389-104">Specifies which beam the Voice Capture DSP uses for microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ce389-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ce389-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ce389-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="ce389-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ce389-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce389-107">Data Type</span></span>

<span data-ttu-id="ce389-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="ce389-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="ce389-109">S'applique à</span><span class="sxs-lookup"><span data-stu-id="ce389-109">Applies To</span></span>

-   [<span data-ttu-id="ce389-110">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="ce389-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="ce389-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ce389-111">Remarks</span></span>

<span data-ttu-id="ce389-112">Définissez cette propriété si la valeur de la propriété [MFPKEY \_ WMAAECMA \_ Feature \_ MICARR \_ mode](mfpkey-wmaaecma-featr-micarr-modeproperty.md) est MICARRAY \_ extern \_ Beam.</span><span class="sxs-lookup"><span data-stu-id="ce389-112">Set this property if the value of the [MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) property is MICARRAY\_EXTERN\_BEAM.</span></span>

<span data-ttu-id="ce389-113">Si la valeur du [**\_ \_ \_ \_ mode de MICARR MFPKEY WMAAECMA**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) est MICARRAY \_ un seul \_ faisceau, vous pouvez lire cette propriété pour interroger le faisceau qui a été sélectionné par le DSP.</span><span class="sxs-lookup"><span data-stu-id="ce389-113">If the value of [**MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) is MICARRAY\_SINGLE\_BEAM, you can read this property to query which beam was selected by the DSP.</span></span>

<span data-ttu-id="ce389-114">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ce389-114">This property can have the following values.</span></span> <span data-ttu-id="ce389-115">Les valeurs sont en degrés horizontaux.</span><span class="sxs-lookup"><span data-stu-id="ce389-115">Values are in degrees horizontal.</span></span>



| <span data-ttu-id="ce389-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce389-116">Value</span></span> | <span data-ttu-id="ce389-117">Description</span><span class="sxs-lookup"><span data-stu-id="ce389-117">Description</span></span>              |
|-------|--------------------------|
| <span data-ttu-id="ce389-118">0</span><span class="sxs-lookup"><span data-stu-id="ce389-118">0</span></span>     | <span data-ttu-id="ce389-119">-50 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-119">-50 degrees.</span></span>             |
| <span data-ttu-id="ce389-120">1</span><span class="sxs-lookup"><span data-stu-id="ce389-120">1</span></span>     | <span data-ttu-id="ce389-121">-40 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-121">-40 degrees.</span></span>             |
| <span data-ttu-id="ce389-122">2</span><span class="sxs-lookup"><span data-stu-id="ce389-122">2</span></span>     | <span data-ttu-id="ce389-123">-30 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-123">-30 degrees.</span></span>             |
| <span data-ttu-id="ce389-124">3</span><span class="sxs-lookup"><span data-stu-id="ce389-124">3</span></span>     | <span data-ttu-id="ce389-125">-20 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-125">-20 degrees.</span></span>             |
| <span data-ttu-id="ce389-126">4</span><span class="sxs-lookup"><span data-stu-id="ce389-126">4</span></span>     | <span data-ttu-id="ce389-127">-10 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-127">-10 degrees.</span></span>             |
| <span data-ttu-id="ce389-128">5</span><span class="sxs-lookup"><span data-stu-id="ce389-128">5</span></span>     | <span data-ttu-id="ce389-129">0 degré (poutre centrale).</span><span class="sxs-lookup"><span data-stu-id="ce389-129">0 degrees (center beam).</span></span> |
| <span data-ttu-id="ce389-130">6</span><span class="sxs-lookup"><span data-stu-id="ce389-130">6</span></span>     | <span data-ttu-id="ce389-131">10 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-131">10 degrees.</span></span>              |
| <span data-ttu-id="ce389-132">7</span><span class="sxs-lookup"><span data-stu-id="ce389-132">7</span></span>     | <span data-ttu-id="ce389-133">20 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-133">20 degrees.</span></span>              |
| <span data-ttu-id="ce389-134">8</span><span class="sxs-lookup"><span data-stu-id="ce389-134">8</span></span>     | <span data-ttu-id="ce389-135">30 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-135">30 degrees.</span></span>              |
| <span data-ttu-id="ce389-136">9</span><span class="sxs-lookup"><span data-stu-id="ce389-136">9</span></span>     | <span data-ttu-id="ce389-137">40 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-137">40 degrees.</span></span>              |
| <span data-ttu-id="ce389-138">10</span><span class="sxs-lookup"><span data-stu-id="ce389-138">10</span></span>    | <span data-ttu-id="ce389-139">50 degrés.</span><span class="sxs-lookup"><span data-stu-id="ce389-139">50 degrees.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="ce389-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce389-140">Requirements</span></span>



| <span data-ttu-id="ce389-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce389-141">Requirement</span></span> | <span data-ttu-id="ce389-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce389-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce389-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce389-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ce389-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce389-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ce389-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce389-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ce389-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce389-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce389-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce389-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce389-148"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce389-148"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce389-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce389-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce389-150">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce389-150">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ce389-151">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="ce389-151">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
