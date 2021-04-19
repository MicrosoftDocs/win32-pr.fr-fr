---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl. h)
description: La transition de rectangle révèle la nouvelle image dans un rectangle dans le cadre.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521670"
---
# <a name="wmt_videoimage_transition_rectangle"></a><span data-ttu-id="91b64-104">\_rectangle de \_ transition \_ VIDEOIMAGE WMT</span><span class="sxs-lookup"><span data-stu-id="91b64-104">WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE</span></span>

<span data-ttu-id="91b64-105">La transition de rectangle révèle la nouvelle image dans un rectangle dans le cadre.</span><span class="sxs-lookup"><span data-stu-id="91b64-105">The rectangle transition reveals the new image in a rectangle within the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="91b64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91b64-106">Parameters</span></span>

<span data-ttu-id="91b64-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="91b64-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91b64-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="91b64-108">Parameter</span></span></th>
<th><span data-ttu-id="91b64-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="91b64-109">Structure member</span></span></th>
<th><span data-ttu-id="91b64-110">Description</span><span class="sxs-lookup"><span data-stu-id="91b64-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91b64-111">Centrer X</span><span class="sxs-lookup"><span data-stu-id="91b64-111">Center X</span></span></td>
<td><span data-ttu-id="91b64-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="91b64-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="91b64-113">Coordonnée X, relative à la trame vidéo, au centre du rectangle.</span><span class="sxs-lookup"><span data-stu-id="91b64-113">X-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91b64-114">Centrer Y</span><span class="sxs-lookup"><span data-stu-id="91b64-114">Center Y</span></span></td>
<td><span data-ttu-id="91b64-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="91b64-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="91b64-116">Coordonnée Y, relative à la trame vidéo, au centre du rectangle.</span><span class="sxs-lookup"><span data-stu-id="91b64-116">Y-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91b64-117">Largeur</span><span class="sxs-lookup"><span data-stu-id="91b64-117">Width</span></span></td>
<td><span data-ttu-id="91b64-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="91b64-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="91b64-119">Largeur du rectangle en pixels.</span><span class="sxs-lookup"><span data-stu-id="91b64-119">Width of the rectangle in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91b64-120">Hauteur</span><span class="sxs-lookup"><span data-stu-id="91b64-120">Height</span></span></td>
<td><span data-ttu-id="91b64-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="91b64-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="91b64-122">Hauteur du rectangle en pixels.</span><span class="sxs-lookup"><span data-stu-id="91b64-122">Height of the rectangle in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91b64-123">Composition</span><span class="sxs-lookup"><span data-stu-id="91b64-123">Composition</span></span></td>
<td><span data-ttu-id="91b64-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="91b64-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="91b64-125">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="91b64-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="91b64-126">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="91b64-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="91b64-127">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="91b64-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="91b64-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91b64-128">Requirements</span></span>



| <span data-ttu-id="91b64-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91b64-129">Requirement</span></span> | <span data-ttu-id="91b64-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="91b64-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91b64-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="91b64-131">Header</span></span><br/> | <dl> <span data-ttu-id="91b64-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91b64-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91b64-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91b64-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b64-134">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="91b64-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





