---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl. h)
description: La transition de la roue révèle la nouvelle image en tournant quatre lignes autour d’un point pivot commun, comme les rayons d’une roue.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_WHEEL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541791"
---
# <a name="wmt_videoimage_transition_wheel"></a><span data-ttu-id="dde0a-104">\_volant de \_ transition \_ VIDEOIMAGE WMT</span><span class="sxs-lookup"><span data-stu-id="dde0a-104">WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL</span></span>

<span data-ttu-id="dde0a-105">La transition de la roue révèle la nouvelle image en tournant quatre lignes autour d’un point pivot commun, comme les rayons d’une roue.</span><span class="sxs-lookup"><span data-stu-id="dde0a-105">The wheel transition reveals the new image by rotating four lines around a common pivot point, like the spokes of a wheel.</span></span>

## <a name="parameters"></a><span data-ttu-id="dde0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dde0a-106">Parameters</span></span>

<span data-ttu-id="dde0a-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="dde0a-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dde0a-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dde0a-108">Parameter</span></span></th>
<th><span data-ttu-id="dde0a-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="dde0a-109">Structure member</span></span></th>
<th><span data-ttu-id="dde0a-110">Description</span><span class="sxs-lookup"><span data-stu-id="dde0a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dde0a-111">Centrer X</span><span class="sxs-lookup"><span data-stu-id="dde0a-111">Center X</span></span></td>
<td><span data-ttu-id="dde0a-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="dde0a-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="dde0a-113">Coordonnée X, relative à la trame vidéo, du centre de l’effet de roulette.</span><span class="sxs-lookup"><span data-stu-id="dde0a-113">X-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dde0a-114">Centrer Y</span><span class="sxs-lookup"><span data-stu-id="dde0a-114">Center Y</span></span></td>
<td><span data-ttu-id="dde0a-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="dde0a-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="dde0a-116">Coordonnée Y, relative à la trame vidéo, du centre de l’effet de roulette.</span><span class="sxs-lookup"><span data-stu-id="dde0a-116">Y-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dde0a-117">Angle</span><span class="sxs-lookup"><span data-stu-id="dde0a-117">Angle</span></span></td>
<td><span data-ttu-id="dde0a-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="dde0a-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="dde0a-119">Angle de rotation, en degrés, des rayons de l’effet de roulette.</span><span class="sxs-lookup"><span data-stu-id="dde0a-119">Angle of rotation, in degrees, of the spokes of the wheel effect.</span></span> <span data-ttu-id="dde0a-120">La valeur 0,0 indique l’ancienne image sans que la nouvelle image soit révélée.</span><span class="sxs-lookup"><span data-stu-id="dde0a-120">A value of 0.0 indicates the old image without any of the new image revealed.</span></span> <span data-ttu-id="dde0a-121">Une valeur de 90,0 indique que la nouvelle image est entièrement dévoilée. Le mouvement de 0,0 à 90,0 apparaît sous forme de rotation des rayons dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="dde0a-121">A value of 90.0 indicates the new image fully revealed.Movement from 0.0 to 90.0 appears as clockwise rotation of the spokes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dde0a-122">Composition</span><span class="sxs-lookup"><span data-stu-id="dde0a-122">Composition</span></span></td>
<td><span data-ttu-id="dde0a-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="dde0a-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="dde0a-124">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="dde0a-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="dde0a-125">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="dde0a-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="dde0a-126">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="dde0a-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="dde0a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dde0a-127">Requirements</span></span>



| <span data-ttu-id="dde0a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dde0a-128">Requirement</span></span> | <span data-ttu-id="dde0a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="dde0a-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dde0a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="dde0a-130">Header</span></span><br/> | <dl> <span data-ttu-id="dde0a-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dde0a-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dde0a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dde0a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde0a-133">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="dde0a-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





