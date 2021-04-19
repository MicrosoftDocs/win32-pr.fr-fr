---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl. h)
description: La transition de fractionnement révèle la nouvelle image en fractionnant l’ancienne image. Le fractionnement s’affiche sur une ligne horizontale ou verticale droite à partir du cadre.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_SPLIT
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532614"
---
# <a name="wmt_videoimage_transition_split"></a><span data-ttu-id="d6f4f-105">\_ \_ fractionnement de transition VIDEOIMAGE WMT \_</span><span class="sxs-lookup"><span data-stu-id="d6f4f-105">WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT</span></span>

<span data-ttu-id="d6f4f-106">La transition de fractionnement révèle la nouvelle image en fractionnant l’ancienne image.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-106">The split transition reveals the new image by splitting the old image.</span></span> <span data-ttu-id="d6f4f-107">Le fractionnement s’affiche sur une ligne horizontale ou verticale droite à partir du cadre.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-107">The split appears along a straight horizontal or vertical line starting inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6f4f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6f4f-108">Parameters</span></span>

<span data-ttu-id="d6f4f-109">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6f4f-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d6f4f-110">Parameter</span></span></th>
<th><span data-ttu-id="d6f4f-111">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="d6f4f-111">Structure member</span></span></th>
<th><span data-ttu-id="d6f4f-112">Description</span><span class="sxs-lookup"><span data-stu-id="d6f4f-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6f4f-113">Centrer X</span><span class="sxs-lookup"><span data-stu-id="d6f4f-113">Center X</span></span></td>
<td><span data-ttu-id="d6f4f-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="d6f4f-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="d6f4f-115">Coordonnée X, relative à la trame vidéo, de la ligne d’origine de la Division.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-115">X-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6f4f-116">Centrer Y</span><span class="sxs-lookup"><span data-stu-id="d6f4f-116">Center Y</span></span></td>
<td><span data-ttu-id="d6f4f-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="d6f4f-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="d6f4f-118">Coordonnée Y, relative à la trame vidéo, de la ligne d’origine de la Division.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-118">Y-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6f4f-119">Distance</span><span class="sxs-lookup"><span data-stu-id="d6f4f-119">Distance</span></span></td>
<td><span data-ttu-id="d6f4f-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="d6f4f-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="d6f4f-121">Largeur du fractionnement en pixels.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-121">Width of the split in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6f4f-122">Sens</span><span class="sxs-lookup"><span data-stu-id="d6f4f-122">Direction</span></span></td>
<td><span data-ttu-id="d6f4f-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="d6f4f-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="d6f4f-124">Orientation du fractionnement. Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6f4f-124">Orientation of the split.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="d6f4f-125">0-fractionne le long d’une ligne horizontale.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-125">0 - Splits along a horizontal line.</span></span></li>
<li><span data-ttu-id="d6f4f-126">1-fractionne le long d’une ligne verticale.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-126">1 - Splits along a vertical line.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6f4f-127">Composition</span><span class="sxs-lookup"><span data-stu-id="d6f4f-127">Composition</span></span></td>
<td><span data-ttu-id="d6f4f-128"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="d6f4f-128"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="d6f4f-129">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6f4f-129">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="d6f4f-130">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="d6f4f-130">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="d6f4f-131">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="d6f4f-131">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d6f4f-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6f4f-132">Requirements</span></span>



| <span data-ttu-id="d6f4f-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6f4f-133">Requirement</span></span> | <span data-ttu-id="d6f4f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6f4f-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f4f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6f4f-135">Header</span></span><br/> | <dl> <span data-ttu-id="d6f4f-136"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f4f-136"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f4f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6f4f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f4f-138">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="d6f4f-138">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





