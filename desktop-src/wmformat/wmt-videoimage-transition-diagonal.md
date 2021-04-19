---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl. h)
description: La transition diagonale révèle la nouvelle image le long d’une ligne diagonale, en partant d’un coin du cadre.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527295"
---
# <a name="wmt_videoimage_transition_diagonal"></a><span data-ttu-id="25691-104">\_transition de \_ transition VIDEOIMAGE en \_ diagonale</span><span class="sxs-lookup"><span data-stu-id="25691-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL</span></span>

<span data-ttu-id="25691-105">La transition diagonale révèle la nouvelle image le long d’une ligne diagonale, en partant d’un coin du cadre.</span><span class="sxs-lookup"><span data-stu-id="25691-105">The diagonal transition reveals the new image along a diagonal line originating in one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="25691-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25691-106">Parameters</span></span>

<span data-ttu-id="25691-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="25691-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="25691-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="25691-108">Parameter</span></span></th>
<th><span data-ttu-id="25691-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="25691-109">Structure member</span></span></th>
<th><span data-ttu-id="25691-110">Description</span><span class="sxs-lookup"><span data-stu-id="25691-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="25691-111">Largeur</span><span class="sxs-lookup"><span data-stu-id="25691-111">Width</span></span></td>
<td><span data-ttu-id="25691-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="25691-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="25691-113">Largeur de la section diagonale en pixels.</span><span class="sxs-lookup"><span data-stu-id="25691-113">Width of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25691-114">Hauteur</span><span class="sxs-lookup"><span data-stu-id="25691-114">Height</span></span></td>
<td><span data-ttu-id="25691-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="25691-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="25691-116">Hauteur de la section diagonale en pixels.</span><span class="sxs-lookup"><span data-stu-id="25691-116">Height of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="25691-117">Sens</span><span class="sxs-lookup"><span data-stu-id="25691-117">Direction</span></span></td>
<td><span data-ttu-id="25691-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="25691-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="25691-119">Détermine l’angle d’origine de la transition. Définissez sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="25691-119">Determines the corner from which the transition originates.Set to one of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="25691-120">0-en haut à droite</span><span class="sxs-lookup"><span data-stu-id="25691-120">0 - Upper right</span></span></li>
<li><span data-ttu-id="25691-121">1-en haut à gauche</span><span class="sxs-lookup"><span data-stu-id="25691-121">1 - Upper left</span></span></li>
<li><span data-ttu-id="25691-122">2-en bas à droite</span><span class="sxs-lookup"><span data-stu-id="25691-122">2 - Lower right</span></span></li>
<li><span data-ttu-id="25691-123">3-en bas à gauche</span><span class="sxs-lookup"><span data-stu-id="25691-123">3 - Lower left</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="25691-124">Composition</span><span class="sxs-lookup"><span data-stu-id="25691-124">Composition</span></span></td>
<td><span data-ttu-id="25691-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="25691-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="25691-126">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="25691-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="25691-127">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="25691-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="25691-128">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="25691-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="25691-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25691-129">Requirements</span></span>



| <span data-ttu-id="25691-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25691-130">Requirement</span></span> | <span data-ttu-id="25691-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="25691-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25691-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="25691-132">Header</span></span><br/> | <dl> <span data-ttu-id="25691-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25691-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25691-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25691-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25691-135">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="25691-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





