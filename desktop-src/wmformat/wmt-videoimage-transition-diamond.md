---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Wmsdkidl. h)
description: La transition Diamond révèle la nouvelle image dans un losange.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_DIAMOND
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e3abfa337edd58fc536e530eb0ff6473c9a9d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545356"
---
# <a name="wmt_videoimage_transition_diamond"></a><span data-ttu-id="756e1-104">\_transition VIDEOIMAGE WMT- \_ \_ losange</span><span class="sxs-lookup"><span data-stu-id="756e1-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND</span></span>

<span data-ttu-id="756e1-105">La transition Diamond révèle la nouvelle image dans un losange.</span><span class="sxs-lookup"><span data-stu-id="756e1-105">The diamond transition reveals the new image in a diamond.</span></span>

## <a name="parameters"></a><span data-ttu-id="756e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="756e1-106">Parameters</span></span>

<span data-ttu-id="756e1-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="756e1-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="756e1-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="756e1-108">Parameter</span></span></th>
<th><span data-ttu-id="756e1-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="756e1-109">Structure member</span></span></th>
<th><span data-ttu-id="756e1-110">Description</span><span class="sxs-lookup"><span data-stu-id="756e1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="756e1-111">Centrer X</span><span class="sxs-lookup"><span data-stu-id="756e1-111">Center X</span></span></td>
<td><span data-ttu-id="756e1-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="756e1-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="756e1-113">Coordonnée X, relative à la trame vidéo, au centre du losange.</span><span class="sxs-lookup"><span data-stu-id="756e1-113">X-coordinate, relative to the video frame, of the center of the diamond.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="756e1-114">Centrer Y</span><span class="sxs-lookup"><span data-stu-id="756e1-114">Center Y</span></span></td>
<td><span data-ttu-id="756e1-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="756e1-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="756e1-116">Coordonnée Y, relative à la trame vidéo, au centre du losange.</span><span class="sxs-lookup"><span data-stu-id="756e1-116">Y-coordinate, relative to the video frame, of the center of the diamond.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="756e1-117">Largeur</span><span class="sxs-lookup"><span data-stu-id="756e1-117">Width</span></span></td>
<td><span data-ttu-id="756e1-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="756e1-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="756e1-119">Largeur du losange en pixels.</span><span class="sxs-lookup"><span data-stu-id="756e1-119">Width of the diamond in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="756e1-120">Hauteur</span><span class="sxs-lookup"><span data-stu-id="756e1-120">Height</span></span></td>
<td><span data-ttu-id="756e1-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="756e1-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="756e1-122">Hauteur du losange en pixels.</span><span class="sxs-lookup"><span data-stu-id="756e1-122">Height of the diamond in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="756e1-123">Composition</span><span class="sxs-lookup"><span data-stu-id="756e1-123">Composition</span></span></td>
<td><span data-ttu-id="756e1-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="756e1-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="756e1-125">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="756e1-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="756e1-126">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="756e1-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="756e1-127">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="756e1-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="756e1-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="756e1-128">Requirements</span></span>



| <span data-ttu-id="756e1-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="756e1-129">Requirement</span></span> | <span data-ttu-id="756e1-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="756e1-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="756e1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="756e1-131">Header</span></span><br/> | <dl> <span data-ttu-id="756e1-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="756e1-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="756e1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="756e1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756e1-134">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="756e1-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





