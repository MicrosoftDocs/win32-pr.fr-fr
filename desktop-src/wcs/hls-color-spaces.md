---
title: Espaces de couleurs HLS
description: Les espaces de couleurs TLS sont également largement utilisés par les artistes. Ses composants de couleur sont la teinte, la luminosité et la saturation (Chroma).
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- Système de couleurs Windows (WCS), espaces de couleurs TLS
- WCS (système de couleurs Windows), espaces de couleurs TLS
- gestion des couleurs des images, espaces de couleurs TLS
- gestion des couleurs, espaces de couleurs TLS
- couleurs, espaces de couleurs TLS
- espaces de couleurs, TLS
- Espaces de couleurs TLS
- Hue
- saturation
- luminosité
- saturation zéro
- saturation de la luminosité de la teinte (TLS)
- TLS (saturation de la luminosité de la teinte)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613a62d4a998b51f9bfb22bd7431dd8645a72f3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106523733"
---
# <a name="hls-color-spaces"></a><span data-ttu-id="554d0-117">Espaces de couleurs HLS</span><span class="sxs-lookup"><span data-stu-id="554d0-117">HLS Color Spaces</span></span>

<span data-ttu-id="554d0-118">Les [espaces de couleurs](c.md) TLS sont également largement utilisés par les artistes.</span><span class="sxs-lookup"><span data-stu-id="554d0-118">HLS [color spaces](c.md) are also widely used by artists.</span></span> <span data-ttu-id="554d0-119">Ses composants de couleur sont la teinte, la luminosité et la saturation (Chroma).</span><span class="sxs-lookup"><span data-stu-id="554d0-119">Its color components are hue, lightness, and saturation (chroma).</span></span>

<span data-ttu-id="554d0-120">La teinte a la même signification que le modèle HSV, sauf qu’un angle de teinte de 0 correspond au bleu dans ce modèle.</span><span class="sxs-lookup"><span data-stu-id="554d0-120">Hue has the same meaning as the HSV model, except that a hue angle of 0 corresponds to blue in this model.</span></span> <span data-ttu-id="554d0-121">Le magenta est à 60, le rouge est à 120.</span><span class="sxs-lookup"><span data-stu-id="554d0-121">Magenta is at 60, red is at 120.</span></span> <span data-ttu-id="554d0-122">Comme pour le modèle HSV, les couleurs complémentaires sont 180.</span><span class="sxs-lookup"><span data-stu-id="554d0-122">As with the HSV model, complementary colors are 180 apart.</span></span>

<span data-ttu-id="554d0-123">La clarté correspond à la quantité de noir ou de blanc dans une couleur.</span><span class="sxs-lookup"><span data-stu-id="554d0-123">Lightness is the amount of black or white in a color.</span></span> <span data-ttu-id="554d0-124">En renforçant la clarté, vous ajoutez du blanc à la teinte.</span><span class="sxs-lookup"><span data-stu-id="554d0-124">Increasing lightness adds white to the hue.</span></span> <span data-ttu-id="554d0-125">La diminution de la clarté ajoute du noir à la teinte.</span><span class="sxs-lookup"><span data-stu-id="554d0-125">Decreasing lightness adds black to the hue.</span></span>

<span data-ttu-id="554d0-126">La [saturation](s.md) dans le modèle TLS est une mesure de la « pureté » d’une teinte.</span><span class="sxs-lookup"><span data-stu-id="554d0-126">[Saturation](s.md) in the HLS model is a measure of the "purity" of a hue.</span></span> <span data-ttu-id="554d0-127">La saturation étant réduite, la teinte devient plus grise.</span><span class="sxs-lookup"><span data-stu-id="554d0-127">As saturation is decreased, the hue becomes more gray.</span></span> <span data-ttu-id="554d0-128">Une valeur de saturation de zéro produit une valeur d’échelle grise.</span><span class="sxs-lookup"><span data-stu-id="554d0-128">A saturation value of zero results in a gray-scale value.</span></span>

<span data-ttu-id="554d0-129">La figure suivante est un dessin linéaire de l’espace TLS, qui est un double hexcone.</span><span class="sxs-lookup"><span data-stu-id="554d0-129">The following figure is a line drawing of HLS space, which is a double hexcone.</span></span> <span data-ttu-id="554d0-130">Toute section transversale horizontale de l’espace de couleurs TLS est un hexagone.</span><span class="sxs-lookup"><span data-stu-id="554d0-130">Any horizontal cross section of the HLS color space is a hexagon.</span></span> <span data-ttu-id="554d0-131">TLS est un espace de couleurs normalisé.</span><span class="sxs-lookup"><span data-stu-id="554d0-131">HLS is a normalized color space.</span></span> <span data-ttu-id="554d0-132">Autrement dit, les valeurs de luminosité et de saturation sont comprises entre 0,0 et 1,0 inclus.</span><span class="sxs-lookup"><span data-stu-id="554d0-132">That is, the lightness and saturation values range from 0.0 to 1.0 inclusive.</span></span> <span data-ttu-id="554d0-133">La teinte varie de 0 à 360 inclus.</span><span class="sxs-lookup"><span data-stu-id="554d0-133">Hue varies from 0 to 360 inclusive.</span></span>

![espace de couleurs TLS](images/hlsline.png)

<span data-ttu-id="554d0-135">Les espaces de couleurs TLS peuvent dépendre du périphérique ou de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="554d0-135">HLS color spaces can be device dependent or device independent.</span></span>

 

 




