---
title: Transitions d’images vidéo
description: Transitions d’images vidéo
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format SDK, images vidéo transitions
- ASF (Advanced Systems Format), transitions d’images vidéo
- ASF (format des systèmes avancés), transitions d’images vidéo
- transitions d’images vidéo
- Codec image v2 Windows Media Video 9
- codecs, codec Windows Media Video 9 image v2
- flux vidéo, codec Windows Media Video 9 image v2
- flux vidéo, transitions d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029018"
---
# <a name="video-image-transitions"></a><span data-ttu-id="e9984-111">Transitions d’images vidéo</span><span class="sxs-lookup"><span data-stu-id="e9984-111">Video Image Transitions</span></span>

<span data-ttu-id="e9984-112">Le codec Windows Media Video 9 image v2 anime une série d’images, générant ainsi un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="e9984-112">The Windows Media Video 9 Image v2 codec animates a series of images, resulting in a video stream.</span></span> <span data-ttu-id="e9984-113">Le codec peut manipuler deux images en même temps, en les fusionnant et en créant une transition de l’une à l’autre, en fonction de la configuration que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="e9984-113">The codec can manipulate two images at once, blending them together and creating a transition from one to the other according to the configuration you supply.</span></span> <span data-ttu-id="e9984-114">Cette section décrit les transitions prises en charge et les paramètres dont elles ont besoin.</span><span class="sxs-lookup"><span data-stu-id="e9984-114">This section describes the supported transitions and the parameters they require.</span></span>

<span data-ttu-id="e9984-115">Les transitions sont répertoriées dans le tableau suivant par leurs identificateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="e9984-115">The transitions are listed in the following table by their global identifiers.</span></span>



| <span data-ttu-id="e9984-116">Identificateur de la transition</span><span class="sxs-lookup"><span data-stu-id="e9984-116">Transition identifier</span></span>                                                                           | <span data-ttu-id="e9984-117">Description</span><span class="sxs-lookup"><span data-stu-id="e9984-117">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9984-118">**\_liaison d' \_ étrave de transition VIDEOIMAGE \_ WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e9984-118">**WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE**</span></span>](wmt-videoimage-transition-bow-tie.md)              | <span data-ttu-id="e9984-119">Une nouvelle image est révélée dans un ensemble de triangles sur les côtés opposés du cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-119">New image is revealed in a set of triangles on opposite sides of the frame.</span></span>                                                                  |
| [<span data-ttu-id="e9984-120">**\_cercle de \_ transition \_ VIDEOIMAGE WMT**</span><span class="sxs-lookup"><span data-stu-id="e9984-120">**WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE**</span></span>](wmt-videoimage-transition-circle.md)                 | <span data-ttu-id="e9984-121">La nouvelle image est révélée dans un cercle.</span><span class="sxs-lookup"><span data-stu-id="e9984-121">New image is revealed in a circle.</span></span>                                                                                                           |
| [<span data-ttu-id="e9984-122">**\_ \_ fondu croisé de transition VIDEOIMAGE \_ WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e9984-122">**WMT\_VIDEOIMAGE\_TRANSITION\_CROSS\_FADE**</span></span>](wmt-videoimage-transition-cross-fade.md)        | <span data-ttu-id="e9984-123">Aucune transition spéciale, les coefficients de fusion des deux images déterminent la fondu enchaîné (dissolution).</span><span class="sxs-lookup"><span data-stu-id="e9984-123">No special transition, the blend coefficients of the two images determine the cross-fade (dissolve).</span></span>                                         |
| [<span data-ttu-id="e9984-124">**\_transition de \_ transition VIDEOIMAGE en \_ diagonale**</span><span class="sxs-lookup"><span data-stu-id="e9984-124">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL**</span></span>](wmt-videoimage-transition-diagonal.md)             | <span data-ttu-id="e9984-125">Une nouvelle image est révélée le long d’une ligne diagonale, en partant d’un coin du cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-125">New image is revealed along a diagonal line originating in one corner of the frame.</span></span>                                                          |
| [<span data-ttu-id="e9984-126">**\_transition VIDEOIMAGE WMT- \_ \_ losange**</span><span class="sxs-lookup"><span data-stu-id="e9984-126">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND**</span></span>](wmt-videoimage-transition-diamond.md)               | <span data-ttu-id="e9984-127">La nouvelle image est révélée en losange.</span><span class="sxs-lookup"><span data-stu-id="e9984-127">New image is revealed in a diamond.</span></span>                                                                                                          |
| [<span data-ttu-id="e9984-128">**\_ \_ transition \_ en fondu VIDEOIMAGE WMT \_ vers la \_ couleur**</span><span class="sxs-lookup"><span data-stu-id="e9984-128">**WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR**</span></span>](wmt-videoimage-transition-fade-to-color.md) | <span data-ttu-id="e9984-129">Se dissout de l’image à une image de couleur unie.</span><span class="sxs-lookup"><span data-stu-id="e9984-129">Dissolves from the image to a frame of solid color.</span></span>                                                                                          |
| [<span data-ttu-id="e9984-130">**VIDEOIMAGE de transition à la \_ \_ transition WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e9984-130">**WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V**</span></span>](wmt-videoimage-transition-filled-v.md)            | <span data-ttu-id="e9984-131">La nouvelle image est révélée dans un triangle provenant d’un côté du cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-131">New image is revealed in a triangle originating from one side of the frame.</span></span>                                                                  |
| [<span data-ttu-id="e9984-132">**\_ \_ basculement de transition VIDEOIMAGE WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e9984-132">**WMT\_VIDEOIMAGE\_TRANSITION\_FLIP**</span></span>](wmt-videoimage-transition-flip.md)                     | <span data-ttu-id="e9984-133">L’ancienne image est pivotée sur un axe y à travers le centre du cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-133">Old image is rotated on a y-axis through the center of the frame.</span></span> <span data-ttu-id="e9984-134">La nouvelle image est révélée à l’arrière de l’ancienne image.</span><span class="sxs-lookup"><span data-stu-id="e9984-134">The new image is revealed as the back of the old image.</span></span>                    |
| [<span data-ttu-id="e9984-135">**inversion de \_ transition VIDEOIMAGE WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e9984-135">**WMT\_VIDEOIMAGE\_TRANSITION\_INSET**</span></span>](wmt-videoimage-transition-inset.md)                   | <span data-ttu-id="e9984-136">Une nouvelle image est révélée par un rectangle provenant d’un coin du cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-136">New image is revealed by a rectangle originating from one corner of the frame.</span></span>                                                               |
| [<span data-ttu-id="e9984-137">**\_VIDEOIMAGE de \_ transition de BASCULement WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e9984-137">**WMT\_VIDEOIMAGE\_TRANSITION\_IRIS**</span></span>](wmt-videoimage-transition-iris.md)                     | <span data-ttu-id="e9984-138">La nouvelle image est révélée le long de l’axe x et de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="e9984-138">New image is revealed along an x-axis and a y-axis.</span></span>                                                                                          |
| [<span data-ttu-id="e9984-139">**\_rouleau de \_ page de transition VIDEOIMAGE \_ WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e9984-139">**WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL**</span></span>](wmt-videoimage-transition-page-roll.md)          | <span data-ttu-id="e9984-140">L’ancienne image est transformée en effet de basculement de page, révélant ainsi la nouvelle image sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e9984-140">Old image is transformed in a page-flipping effect, revealing the new image underneath.</span></span>                                                      |
| [<span data-ttu-id="e9984-141">**\_rectangle de \_ transition \_ VIDEOIMAGE WMT**</span><span class="sxs-lookup"><span data-stu-id="e9984-141">**WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE**</span></span>](wmt-videoimage-transition-rectangle.md)           | <span data-ttu-id="e9984-142">Une nouvelle image est révélée par un rectangle dans le cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-142">New image is revealed by a rectangle within the frame.</span></span>                                                                                       |
| [<span data-ttu-id="e9984-143">**\_révélation de \_ transition \_ VIDEOIMAGE WMT**</span><span class="sxs-lookup"><span data-stu-id="e9984-143">**WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL**</span></span>](wmt-videoimage-transition-reveal.md)                 | <span data-ttu-id="e9984-144">La nouvelle image est révélée le long d’une ligne droite provenant d’un côté du cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-144">New image is revealed along a straight line originating from one side of the frame.</span></span>                                                          |
| [<span data-ttu-id="e9984-145">**\_diapositive de \_ transition \_ VIDEOIMAGE WMT**</span><span class="sxs-lookup"><span data-stu-id="e9984-145">**WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE**</span></span>](wmt-videoimage-transition-slide.md)                   | <span data-ttu-id="e9984-146">L’ancienne image coulisse en dehors du cadre, en révélant la nouvelle image sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="e9984-146">Old image slides out of the frame, revealing the new image underneath.</span></span>                                                                       |
| [<span data-ttu-id="e9984-147">**\_ \_ fractionnement de transition VIDEOIMAGE WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e9984-147">**WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT**</span></span>](wmt-videoimage-transition-split.md)                   | <span data-ttu-id="e9984-148">Une nouvelle image est révélée par un fractionnement horizontal ou vertical dans l’ancienne image.</span><span class="sxs-lookup"><span data-stu-id="e9984-148">New image is revealed by a horizontal or vertical split in the old image.</span></span> <span data-ttu-id="e9984-149">Le fractionnement s’affiche sur une ligne droite à partir du cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-149">The split appears along a straight line starting inside the frame.</span></span> |
| [<span data-ttu-id="e9984-150">**\_étoile de \_ transition \_ VIDEOIMAGE WMT**</span><span class="sxs-lookup"><span data-stu-id="e9984-150">**WMT\_VIDEOIMAGE\_TRANSITION\_STAR**</span></span>](wmt-videoimage-transition-star.md)                     | <span data-ttu-id="e9984-151">Une nouvelle image est révélée par une étoile à cinq branches dans le cadre.</span><span class="sxs-lookup"><span data-stu-id="e9984-151">New image is revealed by a five-pointed star inside the frame.</span></span>                                                                               |
| [<span data-ttu-id="e9984-152">**\_volant de \_ transition \_ VIDEOIMAGE WMT**</span><span class="sxs-lookup"><span data-stu-id="e9984-152">**WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL**</span></span>](wmt-videoimage-transition-wheel.md)                   | <span data-ttu-id="e9984-153">La nouvelle image est révélée par quatre rayons pivotés avec un point pivot commun.</span><span class="sxs-lookup"><span data-stu-id="e9984-153">New image is revealed by four rotating spokes with a common pivot point.</span></span>                                                                     |



 

<span data-ttu-id="e9984-154">Chaque transition est entièrement décrite dans sa propre rubrique.</span><span class="sxs-lookup"><span data-stu-id="e9984-154">Each transition is fully described in its own topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9984-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9984-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9984-156">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="e9984-156">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="e9984-157">**\_VIDEOIMAGE WMT \_ SAMPLE2**</span><span class="sxs-lookup"><span data-stu-id="e9984-157">**WMT\_VIDEOIMAGE\_SAMPLE2**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




