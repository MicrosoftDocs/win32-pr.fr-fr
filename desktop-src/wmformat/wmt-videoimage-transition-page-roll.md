---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl. h)
description: La transition de retour de page transforme l’ancienne image avec un effet de basculement de page, révélant la nouvelle image en dessous.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520824"
---
# <a name="wmt_videoimage_transition_page_roll"></a><span data-ttu-id="c124a-104">\_rouleau de \_ page de transition VIDEOIMAGE \_ WMT \_</span><span class="sxs-lookup"><span data-stu-id="c124a-104">WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL</span></span>

<span data-ttu-id="c124a-105">La transition de retour de page transforme l’ancienne image avec un effet de basculement de page, révélant la nouvelle image en dessous.</span><span class="sxs-lookup"><span data-stu-id="c124a-105">The page roll transition transforms the old image with a page-flipping effect, revealing the new image underneath.</span></span>

## <a name="parameters"></a><span data-ttu-id="c124a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c124a-106">Parameters</span></span>

<span data-ttu-id="c124a-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="c124a-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c124a-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c124a-108">Parameter</span></span></th>
<th><span data-ttu-id="c124a-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="c124a-109">Structure member</span></span></th>
<th><span data-ttu-id="c124a-110">Description</span><span class="sxs-lookup"><span data-stu-id="c124a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c124a-111">Radius</span><span class="sxs-lookup"><span data-stu-id="c124a-111">Radius</span></span></td>
<td><span data-ttu-id="c124a-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="c124a-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="c124a-113">Rayon de la pellicule dans l’effet de rouleau de page.</span><span class="sxs-lookup"><span data-stu-id="c124a-113">Radius of the roll in the page roll effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c124a-114">Distance</span><span class="sxs-lookup"><span data-stu-id="c124a-114">Distance</span></span></td>
<td><span data-ttu-id="c124a-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="c124a-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="c124a-116">Quantité de la nouvelle image qui est révélée par l’effet de rouleau de page, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c124a-116">Amount of the new image that is revealed by the page roll effect, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c124a-117">Sens</span><span class="sxs-lookup"><span data-stu-id="c124a-117">Direction</span></span></td>
<td><span data-ttu-id="c124a-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="c124a-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="c124a-119">Angle ou côté de l’image vidéo, à partir duquel le déroulement de la page est à l’origine. Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c124a-119">Corner or side of the video frame, from which the page roll originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="c124a-120">0-côté gauche</span><span class="sxs-lookup"><span data-stu-id="c124a-120">0 - Left side</span></span></li>
<li><span data-ttu-id="c124a-121">1-côté droit</span><span class="sxs-lookup"><span data-stu-id="c124a-121">1 - Right side</span></span></li>
<li><span data-ttu-id="c124a-122">2-bas</span><span class="sxs-lookup"><span data-stu-id="c124a-122">2 - Bottom</span></span></li>
<li><span data-ttu-id="c124a-123">3-haut</span><span class="sxs-lookup"><span data-stu-id="c124a-123">3 - Top</span></span></li>
<li><span data-ttu-id="c124a-124">4-angle inférieur gauche</span><span class="sxs-lookup"><span data-stu-id="c124a-124">4 - Bottom left corner</span></span></li>
<li><span data-ttu-id="c124a-125">5-coin inférieur droit</span><span class="sxs-lookup"><span data-stu-id="c124a-125">5 - Bottom right corner</span></span></li>
<li><span data-ttu-id="c124a-126">6-coin supérieur gauche</span><span class="sxs-lookup"><span data-stu-id="c124a-126">6 - Upper left corner</span></span></li>
<li><span data-ttu-id="c124a-127">7-coin supérieur droit</span><span class="sxs-lookup"><span data-stu-id="c124a-127">7 - Upper right corner</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c124a-128">Composition</span><span class="sxs-lookup"><span data-stu-id="c124a-128">Composition</span></span></td>
<td><span data-ttu-id="c124a-129"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="c124a-129"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="c124a-130">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c124a-130">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="c124a-131">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="c124a-131">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="c124a-132">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="c124a-132">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c124a-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c124a-133">Requirements</span></span>



| <span data-ttu-id="c124a-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c124a-134">Requirement</span></span> | <span data-ttu-id="c124a-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c124a-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c124a-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c124a-136">Header</span></span><br/> | <dl> <span data-ttu-id="c124a-137"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c124a-137"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c124a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c124a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c124a-139">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="c124a-139">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





