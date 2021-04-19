---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl. h)
description: La transition en étoile révèle la nouvelle image dans une étoile à cinq branches dans le cadre.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_STAR
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528727"
---
# <a name="wmt_videoimage_transition_star"></a><span data-ttu-id="31766-104">\_étoile de \_ transition \_ VIDEOIMAGE WMT</span><span class="sxs-lookup"><span data-stu-id="31766-104">WMT\_VIDEOIMAGE\_TRANSITION\_STAR</span></span>

<span data-ttu-id="31766-105">La transition en étoile révèle la nouvelle image dans une étoile à cinq branches dans le cadre.</span><span class="sxs-lookup"><span data-stu-id="31766-105">The star transition reveals the new image in a five-pointed star inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="31766-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31766-106">Parameters</span></span>

<span data-ttu-id="31766-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="31766-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="31766-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="31766-108">Parameter</span></span></th>
<th><span data-ttu-id="31766-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="31766-109">Structure member</span></span></th>
<th><span data-ttu-id="31766-110">Description</span><span class="sxs-lookup"><span data-stu-id="31766-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31766-111">Centrer X</span><span class="sxs-lookup"><span data-stu-id="31766-111">Center X</span></span></td>
<td><span data-ttu-id="31766-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="31766-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="31766-113">Coordonnée X, relative à la trame vidéo, au centre de l’étoile.</span><span class="sxs-lookup"><span data-stu-id="31766-113">X-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31766-114">Centrer Y</span><span class="sxs-lookup"><span data-stu-id="31766-114">Center Y</span></span></td>
<td><span data-ttu-id="31766-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="31766-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="31766-116">Coordonnée Y, relative à la trame vidéo, au centre de l’étoile.</span><span class="sxs-lookup"><span data-stu-id="31766-116">Y-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="31766-117">Radius</span><span class="sxs-lookup"><span data-stu-id="31766-117">Radius</span></span></td>
<td><span data-ttu-id="31766-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="31766-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="31766-119">Rayon, en pixels, du cercle défini par les points de l’étoile.</span><span class="sxs-lookup"><span data-stu-id="31766-119">Radius, in pixels, of the circle defined by the points of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31766-120">Composition</span><span class="sxs-lookup"><span data-stu-id="31766-120">Composition</span></span></td>
<td><span data-ttu-id="31766-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="31766-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="31766-122">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="31766-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="31766-123">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="31766-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="31766-124">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="31766-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="31766-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31766-125">Requirements</span></span>



| <span data-ttu-id="31766-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31766-126">Requirement</span></span> | <span data-ttu-id="31766-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="31766-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31766-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="31766-128">Header</span></span><br/> | <dl> <span data-ttu-id="31766-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31766-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31766-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31766-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31766-131">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="31766-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





