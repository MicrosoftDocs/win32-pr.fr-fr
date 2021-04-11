---
description: Spécifie si la capture de la voix DSP effectue un découpage central.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: MFPKEY_WMAAECMA_FEATR_CENTER_CLIP, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201887"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a><span data-ttu-id="2393a-103">MFPKEY \_ WMAAECMA \_ Feature de la \_ \_ propriété Clip</span><span class="sxs-lookup"><span data-stu-id="2393a-103">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP Property</span></span>

<span data-ttu-id="2393a-104">Spécifie si la capture de la voix DSP effectue un découpage central.</span><span class="sxs-lookup"><span data-stu-id="2393a-104">Specifies whether the Voice Capture DSP performs center clipping.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2393a-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2393a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2393a-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2393a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2393a-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="2393a-107">Data Type</span></span>

<span data-ttu-id="2393a-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="2393a-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="2393a-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="2393a-109">Default Value</span></span>

<span data-ttu-id="2393a-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="2393a-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="2393a-111">S'applique à</span><span class="sxs-lookup"><span data-stu-id="2393a-111">Applies To</span></span>

-   [<span data-ttu-id="2393a-112">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="2393a-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="2393a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2393a-113">Remarks</span></span>

<span data-ttu-id="2393a-114">Le découpage de centre est un processus qui supprime les petits reliquats d’écho restant après le traitement AEC, dans des situations à simple conversion (lorsque la parole se produit uniquement sur une extrémité de la ligne).</span><span class="sxs-lookup"><span data-stu-id="2393a-114">Center clipping is a process that removes small echo residuals that remain after AEC processing, in single-talk situations (when speech occurs only on one end of the line).</span></span>

<span data-ttu-id="2393a-115">Cette propriété peut avoir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2393a-115">This property can have the following values.</span></span>



| <span data-ttu-id="2393a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2393a-116">Value</span></span>          | <span data-ttu-id="2393a-117">Description</span><span class="sxs-lookup"><span data-stu-id="2393a-117">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="2393a-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="2393a-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="2393a-119">Désactivez le découpage du centre.</span><span class="sxs-lookup"><span data-stu-id="2393a-119">Disable center clipping.</span></span> |
| <span data-ttu-id="2393a-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="2393a-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="2393a-121">Activez le découpage du centre.</span><span class="sxs-lookup"><span data-stu-id="2393a-121">Enable center clipping.</span></span>  |



 

<span data-ttu-id="2393a-122">La valeur par défaut de cette propriété est \_ true (activé).</span><span class="sxs-lookup"><span data-stu-id="2393a-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="2393a-123">Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="2393a-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="2393a-124">Le DSP utilise cette propriété uniquement lorsque le traitement AEC est activé.</span><span class="sxs-lookup"><span data-stu-id="2393a-124">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="2393a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2393a-125">Requirements</span></span>



| <span data-ttu-id="2393a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2393a-126">Requirement</span></span> | <span data-ttu-id="2393a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2393a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2393a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2393a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2393a-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2393a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2393a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2393a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2393a-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2393a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2393a-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2393a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2393a-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2393a-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2393a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2393a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2393a-135">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2393a-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2393a-136">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="2393a-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
