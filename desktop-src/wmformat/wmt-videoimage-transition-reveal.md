---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: La transition de révélation révèle la nouvelle image le long d’une ligne droite provenant d’un côté du cadre.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_REVEAL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526616"
---
# <a name="wmt_videoimage_transition_reveal"></a><span data-ttu-id="b2715-104">\_révélation de \_ transition \_ VIDEOIMAGE WMT</span><span class="sxs-lookup"><span data-stu-id="b2715-104">WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL</span></span>

<span data-ttu-id="b2715-105">La transition de révélation révèle la nouvelle image le long d’une ligne droite provenant d’un côté du cadre.</span><span class="sxs-lookup"><span data-stu-id="b2715-105">The reveal transition reveals the new image along a straight line originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2715-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2715-106">Parameters</span></span>

<span data-ttu-id="b2715-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="b2715-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2715-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b2715-108">Parameter</span></span></th>
<th><span data-ttu-id="b2715-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="b2715-109">Structure member</span></span></th>
<th><span data-ttu-id="b2715-110">Description</span><span class="sxs-lookup"><span data-stu-id="b2715-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2715-111">Distance</span><span class="sxs-lookup"><span data-stu-id="b2715-111">Distance</span></span></td>
<td><span data-ttu-id="b2715-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="b2715-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="b2715-113">Quantité de la nouvelle image révélée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="b2715-113">Amount of the new image revealed, in pixels.</span></span> <span data-ttu-id="b2715-114">Cette valeur est relative au côté origine du frame.</span><span class="sxs-lookup"><span data-stu-id="b2715-114">This value is relative to the originating side of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2715-115">Sens</span><span class="sxs-lookup"><span data-stu-id="b2715-115">Direction</span></span></td>
<td><span data-ttu-id="b2715-116"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="b2715-116"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="b2715-117">Direction de la révélation. Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2715-117">Direction of the revealing.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="b2715-118">0-révéler à droite ; proviennent du côté gauche du frame.</span><span class="sxs-lookup"><span data-stu-id="b2715-118">0 - Reveal to the right; originate from the left side of the frame.</span></span></li>
<li><span data-ttu-id="b2715-119">1-révéler à gauche ; proviennent du côté droit du frame.</span><span class="sxs-lookup"><span data-stu-id="b2715-119">1 - Reveal to the left; originate from the right side of the frame.</span></span></li>
<li><span data-ttu-id="b2715-120">2-révéler vers le haut ; proviennent du bas du frame.</span><span class="sxs-lookup"><span data-stu-id="b2715-120">2 - Reveal upward; originate from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="b2715-121">3-révéler à la baisse ; proviennent du haut du frame.</span><span class="sxs-lookup"><span data-stu-id="b2715-121">3 - Reveal downward; originate from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2715-122">Composition</span><span class="sxs-lookup"><span data-stu-id="b2715-122">Composition</span></span></td>
<td><span data-ttu-id="b2715-123"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="b2715-123"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="b2715-124">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2715-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="b2715-125">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="b2715-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="b2715-126">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="b2715-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b2715-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2715-127">Requirements</span></span>



| <span data-ttu-id="b2715-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2715-128">Requirement</span></span> | <span data-ttu-id="b2715-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2715-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2715-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2715-130">Header</span></span><br/> | <dl> <span data-ttu-id="b2715-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2715-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2715-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2715-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2715-133">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="b2715-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





