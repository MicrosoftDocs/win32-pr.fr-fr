---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl. h)
description: La transition de la diapositive révèle la nouvelle image en faisant glisser l’ancienne image hors du cadre.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_SLIDE
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523993"
---
# <a name="wmt_videoimage_transition_slide"></a><span data-ttu-id="610f0-104">\_diapositive de \_ transition \_ VIDEOIMAGE WMT</span><span class="sxs-lookup"><span data-stu-id="610f0-104">WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE</span></span>

<span data-ttu-id="610f0-105">La transition de la diapositive révèle la nouvelle image en faisant glisser l’ancienne image hors du cadre.</span><span class="sxs-lookup"><span data-stu-id="610f0-105">The slide transition reveals the new image by sliding the old image out of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="610f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="610f0-106">Parameters</span></span>

<span data-ttu-id="610f0-107">Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.</span><span class="sxs-lookup"><span data-stu-id="610f0-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="610f0-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="610f0-108">Parameter</span></span></th>
<th><span data-ttu-id="610f0-109">Membre de structure</span><span class="sxs-lookup"><span data-stu-id="610f0-109">Structure member</span></span></th>
<th><span data-ttu-id="610f0-110">Description</span><span class="sxs-lookup"><span data-stu-id="610f0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="610f0-111">Distance</span><span class="sxs-lookup"><span data-stu-id="610f0-111">Distance</span></span></td>
<td><span data-ttu-id="610f0-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="610f0-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="610f0-113">Distance, en pixels, à partir de laquelle l’ancienne image s’éloigne du cadre.</span><span class="sxs-lookup"><span data-stu-id="610f0-113">Distance, in pixels, that the old image slides out of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="610f0-114">Sens</span><span class="sxs-lookup"><span data-stu-id="610f0-114">Direction</span></span></td>
<td><span data-ttu-id="610f0-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="610f0-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="610f0-116">Sens dans lequel l’ancienne image diapositives. Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="610f0-116">Direction in which the old image slides.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="610f0-117">0-glissement vers la droite.</span><span class="sxs-lookup"><span data-stu-id="610f0-117">0 - Slide to the right.</span></span></li>
<li><span data-ttu-id="610f0-118">1-déplacer vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="610f0-118">1 - Slide to the left.</span></span></li>
<li><span data-ttu-id="610f0-119">2-glissez vers le haut.</span><span class="sxs-lookup"><span data-stu-id="610f0-119">2 - Slide upward.</span></span></li>
<li><span data-ttu-id="610f0-120">3-déplacer vers le bas.</span><span class="sxs-lookup"><span data-stu-id="610f0-120">3 - Slide downward.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="610f0-121">Composition</span><span class="sxs-lookup"><span data-stu-id="610f0-121">Composition</span></span></td>
<td><span data-ttu-id="610f0-122"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="610f0-122"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="610f0-123">Définissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="610f0-123">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="610f0-124">0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</span><span class="sxs-lookup"><span data-stu-id="610f0-124">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="610f0-125">1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</span><span class="sxs-lookup"><span data-stu-id="610f0-125">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="610f0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="610f0-126">Requirements</span></span>



| <span data-ttu-id="610f0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="610f0-127">Requirement</span></span> | <span data-ttu-id="610f0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="610f0-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="610f0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="610f0-129">Header</span></span><br/> | <dl> <span data-ttu-id="610f0-130"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="610f0-130"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="610f0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="610f0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610f0-132">**Transitions d’images vidéo**</span><span class="sxs-lookup"><span data-stu-id="610f0-132">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





