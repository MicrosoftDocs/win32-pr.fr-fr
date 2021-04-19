---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl. h)
description: La transition incrustée révèle la nouvelle image dans un rectangle provenant d’un coin du cadre.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_INSET
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542308"
---
# <a name="wmt_videoimage_transition_inset"></a><span data-ttu-id="d7730-104">inversion de \_ transition VIDEOIMAGE WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="d7730-104">WMT\_VIDEOIMAGE\_TRANSITION\_INSET</span></span>

<span data-ttu-id="d7730-105">La transition incrustée révèle la nouvelle image dans un rectangle provenant d’un coin du cadre.</span><span class="sxs-lookup"><span data-stu-id="d7730-105">The inset transition reveals the new image in a rectangle originating from one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7730-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7730-106">Parameters</span></span>

<span data-ttu-id="d7730-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="d7730-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7730-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d7730-108">Parameter</span></span></th>
<th><span data-ttu-id="d7730-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="d7730-109">Structure member</span></span></th>
<th><span data-ttu-id="d7730-110">Description</span><span class="sxs-lookup"><span data-stu-id="d7730-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7730-111">Largeur</span><span class="sxs-lookup"><span data-stu-id="d7730-111">Width</span></span></td>
<td><span data-ttu-id="d7730-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="d7730-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="d7730-113">Largeur de l’incrustation en pixels.</span><span class="sxs-lookup"><span data-stu-id="d7730-113">Width of the inset in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7730-114">Hauteur</span><span class="sxs-lookup"><span data-stu-id="d7730-114">Height</span></span></td>
<td><span data-ttu-id="d7730-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="d7730-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="d7730-116">Hauteur de l’incrustation en pixels.</span><span class="sxs-lookup"><span data-stu-id="d7730-116">Height of the inset in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7730-117">Sens</span><span class="sxs-lookup"><span data-stu-id="d7730-117">Direction</span></span></td>
<td><span data-ttu-id="d7730-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="d7730-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="d7730-119">Angle d’origine de l’encart. Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7730-119">Corner from which the inset originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="d7730-120">0-en bas à gauche</span><span class="sxs-lookup"><span data-stu-id="d7730-120">0 - Lower left</span></span></li>
<li><span data-ttu-id="d7730-121">1-en bas à droite</span><span class="sxs-lookup"><span data-stu-id="d7730-121">1 - Lower right</span></span></li>
<li><span data-ttu-id="d7730-122">2-en haut à gauche</span><span class="sxs-lookup"><span data-stu-id="d7730-122">2 - Upper left</span></span></li>
<li><span data-ttu-id="d7730-123">3-en haut à droite</span><span class="sxs-lookup"><span data-stu-id="d7730-123">3 - Upper right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7730-124">Composition</span><span class="sxs-lookup"><span data-stu-id="d7730-124">Composition</span></span></td>
<td><span data-ttu-id="d7730-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="d7730-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="d7730-126">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7730-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="d7730-127">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="d7730-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="d7730-128">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="d7730-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d7730-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7730-129">Requirements</span></span>



| <span data-ttu-id="d7730-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7730-130">Requirement</span></span> | <span data-ttu-id="d7730-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7730-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7730-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7730-132">Header</span></span><br/> | <dl> <span data-ttu-id="d7730-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7730-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7730-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7730-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7730-135">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="d7730-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





