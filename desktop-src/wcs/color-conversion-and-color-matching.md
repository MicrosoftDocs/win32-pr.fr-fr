---
title: Conversion des couleurs et correspondance des couleurs
description: Le processus de conversion des couleurs d’un espace colorimétrique à un autre est appelé conversion des couleurs.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Système de couleurs Windows (WCS), conversion de couleurs
- WCS (système de couleurs Windows), conversion de couleurs
- gestion des couleurs des images, conversion de couleurs
- gestion des couleurs, conversion de couleurs
- couleurs, conversion de couleurs
- conversion de couleurs
- Système de couleurs Windows (WCS), correspondance des couleurs
- WCS (système de couleurs Windows), correspondance des couleurs
- gestion des couleurs des images, correspondance des couleurs
- gestion des couleurs, correspondance des couleurs
- couleurs, correspondance des couleurs
- correspondance des couleurs
- Windows Color System (WCS), mappage des couleurs
- WCS (système de couleurs Windows), mappage des couleurs
- gestion des couleurs des images, mappage des couleurs
- gestion des couleurs, mappage des couleurs
- couleurs, mappage des couleurs
- mappage des couleurs
- point blanc
- colorants
- correction gamma
- AVERTISSEMENT
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106523088"
---
# <a name="color-conversion-and-color-matching"></a><span data-ttu-id="382c5-125">Conversion des couleurs et correspondance des couleurs</span><span class="sxs-lookup"><span data-stu-id="382c5-125">Color Conversion and Color Matching</span></span>

<span data-ttu-id="382c5-126">Le processus de conversion des couleurs d’un [espace colorimétrique](c.md) à un autre est appelé *conversion des couleurs*.</span><span class="sxs-lookup"><span data-stu-id="382c5-126">The process of converting colors from one [color space](c.md) to another is called *color conversion*.</span></span> <span data-ttu-id="382c5-127">Toutes les couleurs d’un espace colorimétrique sont fixes par rapport au [point blanc](w.md)de l’espace de couleurs.</span><span class="sxs-lookup"><span data-stu-id="382c5-127">All colors in a color space are fixed relative to the color space's [white point](w.md).</span></span> <span data-ttu-id="382c5-128">Étant donné que le point blanc d’un espace de couleurs varie d’un appareil à l’appareil, une couleur convertie doit ensuite être mise en correspondance avec sa couleur la plus proche de l’espace de couleur de destination.</span><span class="sxs-lookup"><span data-stu-id="382c5-128">Since the white point of a color space varies from device to device, a converted color must then be matched to its visually closest color in the destination color space.</span></span> <span data-ttu-id="382c5-129">Ce processus est appelé « *mappage des couleurs*».</span><span class="sxs-lookup"><span data-stu-id="382c5-129">This process is called *color mapping*.</span></span>

<span data-ttu-id="382c5-130">Par exemple, si vous avez créé une image numérique sur votre écran, elle peut se trouver dans un espace de couleurs RVB dépendant du périphérique.</span><span class="sxs-lookup"><span data-stu-id="382c5-130">For example, if you have a digital image that you created on your display, it may be in a device-dependent RGB color space.</span></span> <span data-ttu-id="382c5-131">Si vous souhaitez l’imprimer sur une imprimante, celle-ci doit être convertie dans l’espace colorimétrique de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="382c5-131">If you want to print it on a printer, it must be converted to the printer's color space.</span></span> <span data-ttu-id="382c5-132">Étant donné que l’imprimante utilise probablement un espace colorimétrique CMJN dépendant du périphérique, toutes les valeurs RVB doivent être converties en CYMK.</span><span class="sxs-lookup"><span data-stu-id="382c5-132">Since the printer probably uses a device-dependent CMYK color space, all RGB values must be converted to CYMK.</span></span> <span data-ttu-id="382c5-133">Il s’agit de la [conversion de couleurs](c.md).</span><span class="sxs-lookup"><span data-stu-id="382c5-133">This is [color conversion](c.md).</span></span> <span data-ttu-id="382c5-134">Une fois que les valeurs sont spécifiées en termes d’espace CYMK, elles doivent être mises en correspondance avec la couleur la plus proche que l’imprimante peut produire.</span><span class="sxs-lookup"><span data-stu-id="382c5-134">Once the values are specified in terms of the CYMK space, they need to be matched to the closest color that the printer can produce.</span></span> <span data-ttu-id="382c5-135">C’est ce que l’on appelle le mappage des couleurs ou la [correspondance des couleurs](c.md).</span><span class="sxs-lookup"><span data-stu-id="382c5-135">This is called color mapping or [color matching](c.md).</span></span>

<span data-ttu-id="382c5-136">La conversion des couleurs et le mappage des couleurs doivent prendre en compte un certain nombre de facteurs spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="382c5-136">Both color conversion and color mapping must take into account a number of device-specific factors.</span></span> <span data-ttu-id="382c5-137">Par exemple, les blocs de construction des images d’écran sont des pixels.</span><span class="sxs-lookup"><span data-stu-id="382c5-137">For instance, the building blocks of screen images are pixels.</span></span> <span data-ttu-id="382c5-138">Chaque pixel a un nombre défini de bits pour stocker sa valeur d’index de couleur ou de couleur.</span><span class="sxs-lookup"><span data-stu-id="382c5-138">Each pixel has a set number of bits to store its color or color index value.</span></span> <span data-ttu-id="382c5-139">Le nombre de bits par pixel dépend du type d’affichage et de la carte d’affichage utilisés, et du mode de définition de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="382c5-139">The number of bits per pixel depends on the type of display and display adapter being used, and the mode to which that the adapter is set.</span></span> <span data-ttu-id="382c5-140">La plupart des types d’imprimante utilisent différents [colorants](c.md) et impriment à des résolutions particulières.</span><span class="sxs-lookup"><span data-stu-id="382c5-140">Most every printer type uses different [colorants](c.md) and prints at particular resolutions.</span></span>

<span data-ttu-id="382c5-141">En outre, les caractéristiques de tonalité physique d’un appareil sont souvent différentes sur des appareils différents.</span><span class="sxs-lookup"><span data-stu-id="382c5-141">In addition, the physical tone characteristics of a device are often different on different devices.</span></span> <span data-ttu-id="382c5-142">Par exemple, lorsque des couleurs sont produites par des moniteurs d’ordinateur, elles peuvent être différentes si elles étaient produites sur une presse d’impression.</span><span class="sxs-lookup"><span data-stu-id="382c5-142">For instance, when colors are produced by computer monitors, they can appear different than they would if they were produced on a printing press.</span></span> <span data-ttu-id="382c5-143">Un facteur de correction, appelé *correction gamma*, est fréquemment utilisé pour compenser ces différences.</span><span class="sxs-lookup"><span data-stu-id="382c5-143">A correction factor, called *gamma correction*, is frequently used to compensate for such differences.</span></span>

<span data-ttu-id="382c5-144">Le résultat de ces facteurs dépendants de l’appareil est que chaque périphérique de couleur a un ensemble particulier de couleurs qu’il peut produire.</span><span class="sxs-lookup"><span data-stu-id="382c5-144">The result of these device-dependent factors is that each color device has a particular set of colors that it can produce.</span></span> <span data-ttu-id="382c5-145">Ce jeu de couleurs est connu sous le nom de *gamme*.</span><span class="sxs-lookup"><span data-stu-id="382c5-145">This color set is known as its *gamut*.</span></span> <span data-ttu-id="382c5-146">Pour effectuer une conversion des couleurs et un mappage des couleurs, les couleurs d’une image doivent être converties à partir de l’espace de couleurs et de la gamme de l’appareil source dans l’espace colorimétrique du périphérique de destination.</span><span class="sxs-lookup"><span data-stu-id="382c5-146">To perform color conversion and color mapping, the colors in an image must be converted from the color space and gamut of the source device into the color space of the destination device.</span></span> <span data-ttu-id="382c5-147">Ils sont ensuite mis en correspondance avec la gamme de l’appareil de destination.</span><span class="sxs-lookup"><span data-stu-id="382c5-147">They are then matched into the gamut of the destination device.</span></span>

 

 




