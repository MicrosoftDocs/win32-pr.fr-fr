---
title: WMT_VIDEOIMAGE_TRANSITION_CIRCLE (Wmsdkidl. h)
description: La transition de cercle révèle la nouvelle image dans un cercle.
ms.assetid: ba3bcf46-1254-4aad-a958-0f9ddb2f40dc
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_CIRCLE
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf3a8eff2ca5a5069fa01c4e61bc0735808fd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528840"
---
# <a name="wmt_videoimage_transition_circle"></a><span data-ttu-id="bda2d-104">\_cercle de \_ transition \_ VIDEOIMAGE WMT</span><span class="sxs-lookup"><span data-stu-id="bda2d-104">WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE</span></span>

<span data-ttu-id="bda2d-105">La transition de cercle révèle la nouvelle image dans un cercle.</span><span class="sxs-lookup"><span data-stu-id="bda2d-105">The circle transition reveals the new image in a circle.</span></span>

## <a name="parameters"></a><span data-ttu-id="bda2d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bda2d-106">Parameters</span></span>

<span data-ttu-id="bda2d-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="bda2d-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bda2d-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="bda2d-108">Parameter</span></span></th>
<th><span data-ttu-id="bda2d-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="bda2d-109">Structure member</span></span></th>
<th><span data-ttu-id="bda2d-110">Description</span><span class="sxs-lookup"><span data-stu-id="bda2d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bda2d-111">Centrer X</span><span class="sxs-lookup"><span data-stu-id="bda2d-111">Center X</span></span></td>
<td><span data-ttu-id="bda2d-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="bda2d-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="bda2d-113">Coordonnée X, relative à la trame vidéo, du centre du cercle.</span><span class="sxs-lookup"><span data-stu-id="bda2d-113">X-coordinate, relative to the video frame, of the center of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bda2d-114">Centrer Y</span><span class="sxs-lookup"><span data-stu-id="bda2d-114">Center Y</span></span></td>
<td><span data-ttu-id="bda2d-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="bda2d-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="bda2d-116">Coordonnée Y, relative à la trame vidéo, du centre du cercle.</span><span class="sxs-lookup"><span data-stu-id="bda2d-116">Y-coordinate, relative to the video frame, of center of the circle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bda2d-117">Radius</span><span class="sxs-lookup"><span data-stu-id="bda2d-117">Radius</span></span></td>
<td><span data-ttu-id="bda2d-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="bda2d-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="bda2d-119">Rayon, en pixels, du cercle.</span><span class="sxs-lookup"><span data-stu-id="bda2d-119">Radius, in pixels, of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bda2d-120">Composition</span><span class="sxs-lookup"><span data-stu-id="bda2d-120">Composition</span></span></td>
<td><span data-ttu-id="bda2d-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="bda2d-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="bda2d-122">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bda2d-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="bda2d-123">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="bda2d-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="bda2d-124">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="bda2d-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="bda2d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bda2d-125">Requirements</span></span>



| <span data-ttu-id="bda2d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bda2d-126">Requirement</span></span> | <span data-ttu-id="bda2d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda2d-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bda2d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="bda2d-128">Header</span></span><br/> | <dl> <span data-ttu-id="bda2d-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bda2d-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bda2d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bda2d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda2d-131">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="bda2d-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





