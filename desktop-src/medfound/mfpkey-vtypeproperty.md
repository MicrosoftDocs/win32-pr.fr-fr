---
description: Spécifie la logique qui sera utilisée par le codec pour détecter la vidéo source entrelacée.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: MFPKEY_VTYPE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863441"
---
# <a name="mfpkey_vtype-property"></a><span data-ttu-id="244b3-103">MFPKEY \_ propriété VTYPE</span><span class="sxs-lookup"><span data-stu-id="244b3-103">MFPKEY\_VTYPE Property</span></span>

<span data-ttu-id="244b3-104">Spécifie la logique qui sera utilisée par le codec pour détecter la vidéo source entrelacée.</span><span class="sxs-lookup"><span data-stu-id="244b3-104">Specifies the logic that the codec will use to detect interlaced source video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="244b3-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="244b3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="244b3-106">\_wszWMVCVType g</span><span class="sxs-lookup"><span data-stu-id="244b3-106">g\_wszWMVCVType</span></span>

## <a name="data-type"></a><span data-ttu-id="244b3-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="244b3-107">Data Type</span></span>

<span data-ttu-id="244b3-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="244b3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="244b3-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="244b3-109">Default Value</span></span>

<span data-ttu-id="244b3-110">0</span><span class="sxs-lookup"><span data-stu-id="244b3-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="244b3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="244b3-111">Remarks</span></span>

<span data-ttu-id="244b3-112">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="244b3-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="244b3-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="244b3-113">Value</span></span> | <span data-ttu-id="244b3-114">Description</span><span class="sxs-lookup"><span data-stu-id="244b3-114">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244b3-115">0</span><span class="sxs-lookup"><span data-stu-id="244b3-115">0</span></span>     | <span data-ttu-id="244b3-116">Le codec utilise la logique standard de détection de type de trame.</span><span class="sxs-lookup"><span data-stu-id="244b3-116">The codec will use the standard frame-type detection logic.</span></span>                                                                                 |
| <span data-ttu-id="244b3-117">1</span><span class="sxs-lookup"><span data-stu-id="244b3-117">1</span></span>     | <span data-ttu-id="244b3-118">Le codec traitera toutes les trames vidéo source en tant que trames entrelacées.</span><span class="sxs-lookup"><span data-stu-id="244b3-118">The codec will treat all source video frames as interlaced frames.</span></span>                                                                          |
| <span data-ttu-id="244b3-119">2</span><span class="sxs-lookup"><span data-stu-id="244b3-119">2</span></span>     | <span data-ttu-id="244b3-120">Le codec traitera toutes les trames vidéo sources comme des champs de vidéo entrelacée.</span><span class="sxs-lookup"><span data-stu-id="244b3-120">The codec will treat all source video frames as fields of interlaced video.</span></span>                                                                 |
| <span data-ttu-id="244b3-121">3</span><span class="sxs-lookup"><span data-stu-id="244b3-121">3</span></span>     | <span data-ttu-id="244b3-122">Le codec déterminera automatiquement si les images vidéo d’entrée sont des images entrelacées ou des champs de vidéo entrelacée.</span><span class="sxs-lookup"><span data-stu-id="244b3-122">The codec will automatically determine whether input video frames are interlaced frames or fields of interlaced video.</span></span>                      |
| <span data-ttu-id="244b3-123">4</span><span class="sxs-lookup"><span data-stu-id="244b3-123">4</span></span>     | <span data-ttu-id="244b3-124">Le codec déterminera automatiquement si les images vidéo d’entrée sont des images progressives, des images entrelacées ou des champs de vidéo entrelacée.</span><span class="sxs-lookup"><span data-stu-id="244b3-124">The codec will automatically determine whether input video frames are progressive frames, interlaced frames, or fields of interlaced video.</span></span> |



 

<span data-ttu-id="244b3-125">Cette propriété détermine la méthode d’encodage d’image utilisée pour l’encodage vidéo progressif ou entrelacé.</span><span class="sxs-lookup"><span data-stu-id="244b3-125">This property determines the picture encoding method used for progressive or interlaced video encoding.</span></span>

<span data-ttu-id="244b3-126">Si aucun type de vidéo n’est spécifié, le codec utilise l’encodage de trame progressif pour les sessions de codage progressive et l’encodage entrelacé de champ pour les sessions d’encodage entrelacées.</span><span class="sxs-lookup"><span data-stu-id="244b3-126">If no video type is specified, the codec will use progressive frame encoding for progressive encoding sessions, and field interlaced encoding for interlaced encoding sessions.</span></span> <span data-ttu-id="244b3-127">Le type de session d’encodage vidéo (progressif ou entrelacé) est défini à l’aide de la propriété [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="244b3-127">The type of video encoding session (progressive or interlaced) is set by using the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="244b3-128">La propriété [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) doit avoir la valeur variant \_ true pour produire une sortie entrelacée ; sinon, la définition de la propriété MPFKEY VTYPE n’aura \_ aucun effet.</span><span class="sxs-lookup"><span data-stu-id="244b3-128">The [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property must be set to VARIANT\_TRUE in order to produce interlaced output; otherwise, setting the MPFKEY\_VTYPE property will have no effect.</span></span>

 

<span data-ttu-id="244b3-129">Quand la vidéo entrelacée est encodée, il est possible de spécifier plusieurs méthodes d’encodage d’image.</span><span class="sxs-lookup"><span data-stu-id="244b3-129">When interlaced video is being encoded, it is possible to specify several picture encoding methods.</span></span> <span data-ttu-id="244b3-130">En général, la méthode la plus efficace pour encoder une vidéo entrelacée consiste à utiliser la méthode entrelacée de champ (2).</span><span class="sxs-lookup"><span data-stu-id="244b3-130">Typically the most efficient way to encode interlaced video is to use the field interlaced method (2).</span></span> <span data-ttu-id="244b3-131">Si la vidéo source contient très peu de mouvement, la méthode entrelacée de cadre (1) ou la méthode de trame/champ automatique (2) peut être plus appropriée.</span><span class="sxs-lookup"><span data-stu-id="244b3-131">If the source video contains very little motion, the frame interlaced method (1) or the auto frame/field method (2) might be more suitable.</span></span>

<span data-ttu-id="244b3-132">Lors de l’encodage de contenu mixte (contenant à la fois des frames progressifs et entrelacés), il est préférable d’utiliser la valeur de la trame automatique/de champ/progressive (4).</span><span class="sxs-lookup"><span data-stu-id="244b3-132">When encoding mixed content (containing both progressive and interlaced frames), it's best to use the value auto frame/field/progressive method (4).</span></span>

## <a name="requirements"></a><span data-ttu-id="244b3-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="244b3-133">Requirements</span></span>



| <span data-ttu-id="244b3-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="244b3-134">Requirement</span></span> | <span data-ttu-id="244b3-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="244b3-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="244b3-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="244b3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="244b3-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="244b3-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="244b3-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="244b3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="244b3-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="244b3-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="244b3-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="244b3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="244b3-141"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="244b3-141"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="244b3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="244b3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244b3-143">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="244b3-143">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




