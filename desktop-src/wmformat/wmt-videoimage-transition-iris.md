---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl. h)
description: La transition Iris affiche la nouvelle image le long d’un axe x et un axe y. L’effet visuel de cette transition est que la nouvelle image apparaît dans une croix étendue qui atteint tous les côtés du cadre.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_IRIS
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522812"
---
# <a name="wmt_videoimage_transition_iris"></a><span data-ttu-id="68d5f-105">\_VIDEOIMAGE de \_ transition de BASCULement WMT \_</span><span class="sxs-lookup"><span data-stu-id="68d5f-105">WMT\_VIDEOIMAGE\_TRANSITION\_IRIS</span></span>

<span data-ttu-id="68d5f-106">La transition Iris affiche la nouvelle image le long d’un axe x et un axe y.</span><span class="sxs-lookup"><span data-stu-id="68d5f-106">The iris transition reveals the new image along an x-axis and a y-axis.</span></span> <span data-ttu-id="68d5f-107">L’effet visuel de cette transition est que la nouvelle image apparaît dans une croix étendue qui atteint tous les côtés du cadre.</span><span class="sxs-lookup"><span data-stu-id="68d5f-107">The visual effect of this transition is that the new image appears in a widening cross reaching to all sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="68d5f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68d5f-108">Parameters</span></span>

<span data-ttu-id="68d5f-109">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="68d5f-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68d5f-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="68d5f-110">Parameter</span></span></th>
<th><span data-ttu-id="68d5f-111">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="68d5f-111">Structure member</span></span></th>
<th><span data-ttu-id="68d5f-112">Description</span><span class="sxs-lookup"><span data-stu-id="68d5f-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68d5f-113">Centrer X</span><span class="sxs-lookup"><span data-stu-id="68d5f-113">Center X</span></span></td>
<td><span data-ttu-id="68d5f-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="68d5f-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="68d5f-115">Coordonnée X, relative à la trame vidéo, du centre de l’effet IRIS.</span><span class="sxs-lookup"><span data-stu-id="68d5f-115">X-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68d5f-116">Centrer Y</span><span class="sxs-lookup"><span data-stu-id="68d5f-116">Center Y</span></span></td>
<td><span data-ttu-id="68d5f-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="68d5f-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="68d5f-118">Coordonnée Y, relative à la trame vidéo, du centre de l’effet IRIS.</span><span class="sxs-lookup"><span data-stu-id="68d5f-118">Y-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68d5f-119">Largeur</span><span class="sxs-lookup"><span data-stu-id="68d5f-119">Width</span></span></td>
<td><span data-ttu-id="68d5f-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="68d5f-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="68d5f-121">Largeur de la ligne verticale qui révèle la nouvelle image, en pixels.</span><span class="sxs-lookup"><span data-stu-id="68d5f-121">Width of the vertical line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68d5f-122">Hauteur</span><span class="sxs-lookup"><span data-stu-id="68d5f-122">Height</span></span></td>
<td><span data-ttu-id="68d5f-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="68d5f-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="68d5f-124">Hauteur de la ligne horizontale qui révèle la nouvelle image, en pixels.</span><span class="sxs-lookup"><span data-stu-id="68d5f-124">Height of the horizontal line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68d5f-125">Composition</span><span class="sxs-lookup"><span data-stu-id="68d5f-125">Composition</span></span></td>
<td><span data-ttu-id="68d5f-126"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="68d5f-126"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="68d5f-127">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="68d5f-127">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="68d5f-128">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="68d5f-128">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="68d5f-129">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="68d5f-129">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="68d5f-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68d5f-130">Requirements</span></span>



| <span data-ttu-id="68d5f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68d5f-131">Requirement</span></span> | <span data-ttu-id="68d5f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="68d5f-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68d5f-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="68d5f-133">Header</span></span><br/> | <dl> <span data-ttu-id="68d5f-134"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68d5f-134"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68d5f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68d5f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d5f-136">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="68d5f-136">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





