---
description: Spécifie si le codec utilise l’optimisation de la mise à l’échelle vidéo.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: MFPKEY_VIDEOSCALING, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863982"
---
# <a name="mfpkey_videoscaling-property"></a><span data-ttu-id="dcd14-103">MFPKEY \_ propriété VIDEOSCALING</span><span class="sxs-lookup"><span data-stu-id="dcd14-103">MFPKEY\_VIDEOSCALING Property</span></span>

<span data-ttu-id="dcd14-104">Spécifie si le codec utilise l’optimisation de la mise à l’échelle vidéo.</span><span class="sxs-lookup"><span data-stu-id="dcd14-104">Specifies whether the codec will use video scaling optimization.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="dcd14-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="dcd14-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="dcd14-106">\_wszWMVCVideoScaling g</span><span class="sxs-lookup"><span data-stu-id="dcd14-106">g\_wszWMVCVideoScaling</span></span>

## <a name="data-type"></a><span data-ttu-id="dcd14-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="dcd14-107">Data Type</span></span>

<span data-ttu-id="dcd14-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="dcd14-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="dcd14-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="dcd14-109">Default Value</span></span>

<span data-ttu-id="dcd14-110">0</span><span class="sxs-lookup"><span data-stu-id="dcd14-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd14-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dcd14-111">Remarks</span></span>

<span data-ttu-id="dcd14-112">La mise à l’échelle vidéo est un type d’optimisation de perception qui peut améliorer la qualité visuelle de la vidéo encodée à des vitesses de transmission faibles.</span><span class="sxs-lookup"><span data-stu-id="dcd14-112">Video scaling is a type of perceptual optimization that can improve the visual quality of video encoded at low bit rates.</span></span> <span data-ttu-id="dcd14-113">L’optimisation de la mise à l’échelle vidéo réduit les artefacts prononcés, mais peut sacrifier les détails de l’image.</span><span class="sxs-lookup"><span data-stu-id="dcd14-113">The video scaling optimization reduces pronounced artifacts, but can sacrifice image detail.</span></span> <span data-ttu-id="dcd14-114">Cette optimisation affecte la plage de luminance de la vidéo encodée comme décrit ci-dessous, mais n’affecte pas la résolution physique de la vidéo de sortie.</span><span class="sxs-lookup"><span data-stu-id="dcd14-114">This optimization affects the luma range of the encoded video as described below but does not affect the physical resolution of the output video.</span></span>

<span data-ttu-id="dcd14-115">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="dcd14-115">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="dcd14-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcd14-116">Value</span></span> | <span data-ttu-id="dcd14-117">Description</span><span class="sxs-lookup"><span data-stu-id="dcd14-117">Description</span></span>                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd14-118">0</span><span class="sxs-lookup"><span data-stu-id="dcd14-118">0</span></span>     | <span data-ttu-id="dcd14-119">La mise à l’échelle vidéo ne sera pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="dcd14-119">Video scaling will not be used.</span></span>                                                                                       |
| <span data-ttu-id="dcd14-120">1</span><span class="sxs-lookup"><span data-stu-id="dcd14-120">1</span></span>     | <span data-ttu-id="dcd14-121">L’encodeur utilise l’optimisation de la mise à l’échelle vidéo classique.</span><span class="sxs-lookup"><span data-stu-id="dcd14-121">The encoder will use conservative video scaling optimization.</span></span> <span data-ttu-id="dcd14-122">La plage de luminance sera mise à l’échelle de 0... 255 à 26... 229.</span><span class="sxs-lookup"><span data-stu-id="dcd14-122">The luma range will be scaled from 0...255 to 26...229.</span></span> |
| <span data-ttu-id="dcd14-123">2</span><span class="sxs-lookup"><span data-stu-id="dcd14-123">2</span></span>     | <span data-ttu-id="dcd14-124">L’encodeur utilise l’optimisation de la mise à l’échelle vidéo agressive.</span><span class="sxs-lookup"><span data-stu-id="dcd14-124">The encoder will use aggressive video scaling optimization.</span></span> <span data-ttu-id="dcd14-125">La plage de luminance sera mise à l’échelle de 0... 255 à 31... 224.</span><span class="sxs-lookup"><span data-stu-id="dcd14-125">The luma range will be scaled from 0...255 to 31...224.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="dcd14-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcd14-126">Requirements</span></span>



| <span data-ttu-id="dcd14-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcd14-127">Requirement</span></span> | <span data-ttu-id="dcd14-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcd14-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd14-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcd14-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd14-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcd14-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dcd14-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcd14-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd14-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcd14-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dcd14-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcd14-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcd14-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcd14-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcd14-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcd14-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd14-136">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dcd14-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




