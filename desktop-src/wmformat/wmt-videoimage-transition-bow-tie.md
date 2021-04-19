---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl. h)
description: La transition de liaison papillone révèle la nouvelle image dans un ensemble de triangles sur les côtés opposés du cadre.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539506"
---
# <a name="wmt_videoimage_transition_bow_tie"></a><span data-ttu-id="332d4-104">\_liaison d' \_ étrave de transition VIDEOIMAGE \_ WMT \_</span><span class="sxs-lookup"><span data-stu-id="332d4-104">WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE</span></span>

<span data-ttu-id="332d4-105">La transition de liaison papillone révèle la nouvelle image dans un ensemble de triangles sur les côtés opposés du cadre.</span><span class="sxs-lookup"><span data-stu-id="332d4-105">The bow tie transition reveals the new image in a set of triangles on opposite sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="332d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="332d4-106">Parameters</span></span>

<span data-ttu-id="332d4-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="332d4-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="332d4-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="332d4-108">Parameter</span></span></th>
<th><span data-ttu-id="332d4-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="332d4-109">Structure member</span></span></th>
<th><span data-ttu-id="332d4-110">Description</span><span class="sxs-lookup"><span data-stu-id="332d4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="332d4-111">Largeur</span><span class="sxs-lookup"><span data-stu-id="332d4-111">Width</span></span></td>
<td><span data-ttu-id="332d4-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="332d4-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="332d4-113">Largeur de chaque côté triangulaire de l’égalité d’étrave.</span><span class="sxs-lookup"><span data-stu-id="332d4-113">Width of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="332d4-114">Hauteur</span><span class="sxs-lookup"><span data-stu-id="332d4-114">Height</span></span></td>
<td><span data-ttu-id="332d4-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="332d4-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="332d4-116">Hauteur de chaque côté triangulaire de l’égalité d’étrave.</span><span class="sxs-lookup"><span data-stu-id="332d4-116">Height of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="332d4-117">Sens</span><span class="sxs-lookup"><span data-stu-id="332d4-117">Direction</span></span></td>
<td><span data-ttu-id="332d4-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="332d4-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="332d4-119">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="332d4-119">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="332d4-120">0-spécifie l’effet de lien d’étrave horizontal, dans lequel les triangles entrent à partir des côtés droit et gauche du cadre.</span><span class="sxs-lookup"><span data-stu-id="332d4-120">0 - Specifies horizontal bow tie effect, in which the triangles enter from the right and left sides of the frame.</span></span></li>
<li><span data-ttu-id="332d4-121">1-spécifie l’effet de lien d’inclinaison vertical, dans lequel les triangles entrent en haut et en bas du cadre.</span><span class="sxs-lookup"><span data-stu-id="332d4-121">1 - Specifies vertical bow tie effect, in which the triangles enter from the top and bottom of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="332d4-122">Composition</span><span class="sxs-lookup"><span data-stu-id="332d4-122">Composition</span></span></td>
<td><span data-ttu-id="332d4-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="332d4-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="332d4-124">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="332d4-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="332d4-125">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="332d4-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="332d4-126">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="332d4-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="332d4-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="332d4-127">Requirements</span></span>



| <span data-ttu-id="332d4-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="332d4-128">Requirement</span></span> | <span data-ttu-id="332d4-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="332d4-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="332d4-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="332d4-130">Header</span></span><br/> | <dl> <span data-ttu-id="332d4-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="332d4-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332d4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="332d4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332d4-133">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="332d4-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





