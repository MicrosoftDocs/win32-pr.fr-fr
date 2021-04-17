---
title: Espaces de couleurs HSV
description: Les espaces colorimétriques de teinte, de saturation et de valeur (HSV) sont souvent utilisés par les artistes.
ms.assetid: a2ee9f29-0b81-4edc-8af8-f4df765e9952
keywords:
- Système de couleurs Windows (WCS), espaces de couleurs HSV
- WCS (système de couleurs Windows), espaces de couleurs HSV
- gestion des couleurs des images, espaces de couleurs HSV
- gestion des couleurs, espaces de couleurs HSV
- couleurs, espaces de couleurs HSV
- espaces colorimétriques, HSV
- Espaces de couleurs HSV
- Hue
- saturation
- value
- luminosité
- saturation zéro
- valeur de saturation de la teinte (HSV)
- HSV (valeur de saturation de la teinte)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4135e9c30dd69b8c5add5d9d8e6d784127ebaec9
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "104558006"
---
# <a name="hsv-color-spaces"></a><span data-ttu-id="16f6d-117">Espaces de couleurs HSV</span><span class="sxs-lookup"><span data-stu-id="16f6d-117">HSV Color Spaces</span></span>

<span data-ttu-id="16f6d-118">Les [espaces colorimétriques](c.md) de teinte, de saturation et de valeur (HSV) sont souvent utilisés par les artistes.</span><span class="sxs-lookup"><span data-stu-id="16f6d-118">Hue, saturation, and value (HSV) [color spaces](c.md) are often used by artists.</span></span> <span data-ttu-id="16f6d-119">« Teinte » est ce que nous considérons normalement comme des couleurs.</span><span class="sxs-lookup"><span data-stu-id="16f6d-119">"Hue" is what we normally think of as color.</span></span> <span data-ttu-id="16f6d-120">Il s’agit de l’attribut d’une couleur sur laquelle nous attribuons un nom tel que « rouge » ou « bleu ».</span><span class="sxs-lookup"><span data-stu-id="16f6d-120">It is the attribute of a color by which we give it a name such as "red" or "blue".</span></span> <span data-ttu-id="16f6d-121">« Valeur » est un autre mot pour « la clarté », l’attribut d’une couleur qui lui donne l’équivalent d’une nuance de gris entre le noir et le blanc.</span><span class="sxs-lookup"><span data-stu-id="16f6d-121">"Value" is another word for "lightness," the attribute of a color that makes it seem equivalent to some shade of gray between black and white.</span></span> <span data-ttu-id="16f6d-122">La saturation est une mesure de la différence entre une couleur et un gris de la même [luminosité](b.md).</span><span class="sxs-lookup"><span data-stu-id="16f6d-122">Saturation is a measure of how different a color appears from a gray of the same [lightness](b.md).</span></span> <span data-ttu-id="16f6d-123">La saturation zéro indique aucune teinte, il suffit de l’échelle en gris.</span><span class="sxs-lookup"><span data-stu-id="16f6d-123">Zero saturation indicates no hue, just gray scale.</span></span> <span data-ttu-id="16f6d-124">L’espace de couleurs HSV est normalisé.</span><span class="sxs-lookup"><span data-stu-id="16f6d-124">The HSV color space is normalized.</span></span>

![espace colorimétrique HSV](images/hsvline.png)

<span data-ttu-id="16f6d-126">La figure ci-dessus montre un dessin en courbes de l’espace HSV sous la forme d’un hexcone.</span><span class="sxs-lookup"><span data-stu-id="16f6d-126">The preceding figure shows a line drawing of HSV space in the form of a hexcone.</span></span> <span data-ttu-id="16f6d-127">Chacune de ses coupes est un hexagone.</span><span class="sxs-lookup"><span data-stu-id="16f6d-127">Each of its cross sections is a hexagon.</span></span> <span data-ttu-id="16f6d-128">Au niveau des sommets de chaque coupe se trouvent les couleurs rouge, jaune, vert, cyan, bleu et magenta.</span><span class="sxs-lookup"><span data-stu-id="16f6d-128">At the vertices of each cross section are the colors red, yellow, green, cyan, blue, and magenta.</span></span> <span data-ttu-id="16f6d-129">Une couleur dans l’espace HSV est spécifiée en indiquant un angle de teinte, le niveau de chrominance et le niveau de luminosité.</span><span class="sxs-lookup"><span data-stu-id="16f6d-129">A color in HSV space is specified by stating a hue angle, the chroma level, and the lightness level.</span></span> <span data-ttu-id="16f6d-130">Un angle de teinte de zéro est rouge.</span><span class="sxs-lookup"><span data-stu-id="16f6d-130">A hue angle of zero is red.</span></span> <span data-ttu-id="16f6d-131">L’angle de teinte augmente dans le sens inverse des aiguilles d’une passe.</span><span class="sxs-lookup"><span data-stu-id="16f6d-131">The hue angle increases in a counterclockwise direction.</span></span> <span data-ttu-id="16f6d-132">Les couleurs complémentaires sont écartées de 180.</span><span class="sxs-lookup"><span data-stu-id="16f6d-132">Complementary colors are 180 apart.</span></span>

<span data-ttu-id="16f6d-133">Les espaces de couleurs HSV peuvent dépendre du périphérique ou de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="16f6d-133">HSV color spaces can be device dependent or device independent.</span></span>

 

 




