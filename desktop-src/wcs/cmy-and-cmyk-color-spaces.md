---
title: Espaces de couleurs CMJ et CMJN
description: Les espaces de couleurs CMJ et CMJN sont souvent utilisés dans l’impression couleur. Un espace de couleurs CMJ utilise le cyan, le magenta et le jaune (CMJ) comme couleurs primaires. Les couleurs secondaires rouge, vert et bleu.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Système de couleurs Windows (WCS), espaces de couleurs CMJ
- WCS (système de couleurs Windows), CMJ d’espaces de couleurs
- gestion des couleurs des images, espaces de couleurs CMJ
- gestion des couleurs, espaces de couleurs CMJ
- couleurs, espaces de couleurs CMJ
- espaces de couleurs, CMJ
- Espaces de couleurs CMJ
- Windows Color System (WCS), espaces de couleurs CMJN
- WCS (système de couleurs Windows), espaces de couleurs CMJN
- gestion des couleurs des images, espaces de couleurs CMJN
- gestion des couleurs, espaces CMYKcolor
- couleurs, espaces de couleurs CMJN
- espaces colorimétriques, CMJN
- Espaces de couleurs CMJN
- Cyan
- Magenta
- yellow
- cyan magenta jaune (CMJ)
- CMJ (cyan magenta jaune)
- cyan magenta jaune noir (CMJN)
- CMJN (cyan magenta jaune noir)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106544333"
---
# <a name="cmy-and-cmyk-color-spaces"></a><span data-ttu-id="f73f1-126">Espaces de couleurs CMJ et CMJN</span><span class="sxs-lookup"><span data-stu-id="f73f1-126">CMY and CMYK Color Spaces</span></span>

<span data-ttu-id="f73f1-127">Les [espaces de couleurs](c.md) CMJ et CMJN sont souvent utilisés dans l’impression couleur.</span><span class="sxs-lookup"><span data-stu-id="f73f1-127">The CMY and CMYK [color spaces](c.md) are often used in color printing.</span></span> <span data-ttu-id="f73f1-128">Un espace de couleurs CMJ utilise le cyan, le magenta et le jaune (CMJ) comme [couleurs primaires](p.md).</span><span class="sxs-lookup"><span data-stu-id="f73f1-128">A CMY color space uses cyan, magenta, and yellow (CMY) as its [primary colors](p.md).</span></span> <span data-ttu-id="f73f1-129">Les couleurs secondaires rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="f73f1-129">Red, green, and blue are the secondary colors.</span></span>

<span data-ttu-id="f73f1-130">Les figures suivantes sont des représentations de couleur de l’espace de couleurs CMJ.</span><span class="sxs-lookup"><span data-stu-id="f73f1-130">The following figures are color representations of the CMY color space.</span></span> <span data-ttu-id="f73f1-131">L’espace de couleurs CMJ est normalisé.</span><span class="sxs-lookup"><span data-stu-id="f73f1-131">The CMY color space is normalized.</span></span>

![Cube d’espace de couleurs CMJ à des valeurs maximales](images/cmyclrs1.png)

![Cube d’espace colorimétrique CMJ aux valeurs minimales](images/cmyclrs2.png)

<span data-ttu-id="f73f1-134">L’espace de couleurs CMJ est soustrait.</span><span class="sxs-lookup"><span data-stu-id="f73f1-134">The CMY color space is subtractive.</span></span> <span data-ttu-id="f73f1-135">Par conséquent, le blanc se trouve à l’adresse (0,0, 0,0, 0,0) et le noir à (1,0, 1,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="f73f1-135">Therefore, white is at (0.0, 0.0, 0.0) and black is at (1.0, 1.0, 1.0).</span></span> <span data-ttu-id="f73f1-136">Si vous commencez avec le blanc sans soustraire les couleurs, vous êtes blanc.</span><span class="sxs-lookup"><span data-stu-id="f73f1-136">If you start with white and subtract no colors, you get white.</span></span> <span data-ttu-id="f73f1-137">Si vous commencez avec le blanc et que vous soustrayez toutes les couleurs de manière égale, vous êtes noir.</span><span class="sxs-lookup"><span data-stu-id="f73f1-137">If you start with white and subtract all colors equally, you get black.</span></span>

<span data-ttu-id="f73f1-138">L’espace colorimétrique CMJN est une variation sur le modèle CMJ.</span><span class="sxs-lookup"><span data-stu-id="f73f1-138">The CMYK color space is a variation on the CMY model.</span></span> <span data-ttu-id="f73f1-139">Il ajoute du noir (cyan, magenta, jaune et noir).</span><span class="sxs-lookup"><span data-stu-id="f73f1-139">It adds black (Cyan, Magenta, Yellow, and blacK).</span></span> <span data-ttu-id="f73f1-140">L’espace colorimétrique CMJN ferme l’intervalle entre la théorie et la pratique.</span><span class="sxs-lookup"><span data-stu-id="f73f1-140">The CMYK color space closes the gap between theory and practice.</span></span> <span data-ttu-id="f73f1-141">En théorie, le composant noir supplémentaire n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f73f1-141">In theory, the extra black component is not needed.</span></span> <span data-ttu-id="f73f1-142">Toutefois, l’expérience avec différents types d’encres et de papiers a montré que lorsque des composants équivalents des encres cyan, magenta et jaune sont mélangés, le résultat est généralement un brun foncé, et non le noir.</span><span class="sxs-lookup"><span data-stu-id="f73f1-142">However, experience with various types of inks and papers has shown that when equal components of cyan, magenta, and yellow inks are mixed, the result is usually a dark brown, not black.</span></span> <span data-ttu-id="f73f1-143">L’ajout d’encre noire à la combinaison résout ce problème.</span><span class="sxs-lookup"><span data-stu-id="f73f1-143">Adding black ink to the mix solves this problem.</span></span>

<span data-ttu-id="f73f1-144">Les espaces de couleurs CMJ et CMJN peuvent être indépendants des appareils, mais ils sont le plus souvent utilisés en référence à un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="f73f1-144">The CMY and CMYK colors spaces can be device independent, but most often they are used in reference to a specific device.</span></span>

 

 




