---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl. h)
description: La transition de V remplie révèle la nouvelle image dans un triangle provenant d’un côté du frame.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_FILLED_V
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542449"
---
# <a name="wmt_videoimage_transition_filled_v"></a><span data-ttu-id="a2831-104">VIDEOIMAGE de transition à la \_ \_ transition WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="a2831-104">WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V</span></span>

<span data-ttu-id="a2831-105">La transition de V remplie révèle la nouvelle image dans un triangle provenant d’un côté du frame.</span><span class="sxs-lookup"><span data-stu-id="a2831-105">The filled V transition reveals the new image in a triangle originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2831-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2831-106">Parameters</span></span>

<span data-ttu-id="a2831-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="a2831-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a2831-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a2831-108">Parameter</span></span></th>
<th><span data-ttu-id="a2831-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="a2831-109">Structure member</span></span></th>
<th><span data-ttu-id="a2831-110">Description</span><span class="sxs-lookup"><span data-stu-id="a2831-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a2831-111">Largeur</span><span class="sxs-lookup"><span data-stu-id="a2831-111">Width</span></span></td>
<td><span data-ttu-id="a2831-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="a2831-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="a2831-113">Largeur du V rempli en pixels.</span><span class="sxs-lookup"><span data-stu-id="a2831-113">Width of the filled V in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2831-114">Hauteur</span><span class="sxs-lookup"><span data-stu-id="a2831-114">Height</span></span></td>
<td><span data-ttu-id="a2831-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="a2831-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="a2831-116">Hauteur du V rempli en pixels.</span><span class="sxs-lookup"><span data-stu-id="a2831-116">Height of the filled V in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a2831-117">Sens</span><span class="sxs-lookup"><span data-stu-id="a2831-117">Direction</span></span></td>
<td><span data-ttu-id="a2831-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="a2831-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="a2831-119">Direction d’origine du V rempli. Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2831-119">Direction from which the filled V originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="a2831-120">0-entre le côté gauche du cadre.</span><span class="sxs-lookup"><span data-stu-id="a2831-120">0 - Enters from the left side of the frame.</span></span></li>
<li><span data-ttu-id="a2831-121">1 : entre le côté droit du cadre.</span><span class="sxs-lookup"><span data-stu-id="a2831-121">1 - Enters from the right side of the frame.</span></span></li>
<li><span data-ttu-id="a2831-122">2-entre le bas du cadre.</span><span class="sxs-lookup"><span data-stu-id="a2831-122">2 - Enters from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="a2831-123">3-entre le haut du cadre.</span><span class="sxs-lookup"><span data-stu-id="a2831-123">3 - Enters from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a2831-124">Composition</span><span class="sxs-lookup"><span data-stu-id="a2831-124">Composition</span></span></td>
<td><span data-ttu-id="a2831-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="a2831-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="a2831-126">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2831-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="a2831-127">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="a2831-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="a2831-128">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="a2831-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a2831-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2831-129">Requirements</span></span>



| <span data-ttu-id="a2831-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2831-130">Requirement</span></span> | <span data-ttu-id="a2831-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2831-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2831-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2831-132">Header</span></span><br/> | <dl> <span data-ttu-id="a2831-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2831-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2831-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2831-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2831-135">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="a2831-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





