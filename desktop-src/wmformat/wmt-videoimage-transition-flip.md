---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl. h)
description: La transition de retournement fait pivoter l’ancienne image sur un axe y à travers le centre du cadre. La nouvelle image est révélée à l’arrière de l’ancienne image.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_FLIP
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537702"
---
# <a name="wmt_videoimage_transition_flip"></a><span data-ttu-id="6cba4-105">\_ \_ basculement de transition VIDEOIMAGE WMT \_</span><span class="sxs-lookup"><span data-stu-id="6cba4-105">WMT\_VIDEOIMAGE\_TRANSITION\_FLIP</span></span>

<span data-ttu-id="6cba4-106">La transition de retournement fait pivoter l’ancienne image sur un axe y à travers le centre du cadre.</span><span class="sxs-lookup"><span data-stu-id="6cba4-106">The flip transition rotates the old image on a y-axis through the center of the frame.</span></span> <span data-ttu-id="6cba4-107">La nouvelle image est révélée à l’arrière de l’ancienne image.</span><span class="sxs-lookup"><span data-stu-id="6cba4-107">The new image is revealed as the back of the old image.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cba4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cba4-108">Parameters</span></span>

<span data-ttu-id="6cba4-109">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="6cba4-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cba4-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6cba4-110">Parameter</span></span></th>
<th><span data-ttu-id="6cba4-111">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="6cba4-111">Structure member</span></span></th>
<th><span data-ttu-id="6cba4-112">Description</span><span class="sxs-lookup"><span data-stu-id="6cba4-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6cba4-113">Angle</span><span class="sxs-lookup"><span data-stu-id="6cba4-113">Angle</span></span></td>
<td><span data-ttu-id="6cba4-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="6cba4-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="6cba4-115">Angle de rotation, de 0,0 à 180,0 degrés.</span><span class="sxs-lookup"><span data-stu-id="6cba4-115">Angle of the rotation, from 0.0 to 180.0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cba4-116">Composition</span><span class="sxs-lookup"><span data-stu-id="6cba4-116">Composition</span></span></td>
<td><span data-ttu-id="6cba4-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="6cba4-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="6cba4-118">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6cba4-118">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="6cba4-119">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="6cba4-119">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="6cba4-120">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="6cba4-120">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="6cba4-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6cba4-121">Remarks</span></span>

<span data-ttu-id="6cba4-122">Vous pouvez visualiser l’effet de cette transition comme si les deux images étaient des photographies physiques collées en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="6cba4-122">You can visualize the effect of this transition as if both images were physical photographs glued together back-to-back.</span></span> <span data-ttu-id="6cba4-123">La transition a le même effet que le maintien de deux photographies de ce type au centre du bord inférieur et les faire pivoter de 180 degrés.</span><span class="sxs-lookup"><span data-stu-id="6cba4-123">The transition has the same effect as holding two such photographs at the center of the bottom edge and rotating them 180 degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cba4-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cba4-124">Requirements</span></span>



| <span data-ttu-id="6cba4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cba4-125">Requirement</span></span> | <span data-ttu-id="6cba4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cba4-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cba4-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cba4-127">Header</span></span><br/> | <dl> <span data-ttu-id="6cba4-128"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cba4-128"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cba4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cba4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cba4-130">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="6cba4-130">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





