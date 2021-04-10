---
description: Cette rubrique décrit deux concepts connexes, le rapport hauteur/largeur des images et les proportions en pixels.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Rapport hauteur/largeur des images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201858"
---
# <a name="picture-aspect-ratio"></a><span data-ttu-id="e3c00-103">Rapport hauteur/largeur des images</span><span class="sxs-lookup"><span data-stu-id="e3c00-103">Picture Aspect Ratio</span></span>

<span data-ttu-id="e3c00-104">Cette rubrique décrit deux concepts connexes, le rapport hauteur/largeur des images et les proportions en pixels.</span><span class="sxs-lookup"><span data-stu-id="e3c00-104">This topic describes two related concepts, picture aspect ratio and pixel aspect ratio.</span></span> <span data-ttu-id="e3c00-105">Il décrit ensuite comment ces concepts sont exprimés en Microsoft Media Foundation à l’aide de types de médias.</span><span class="sxs-lookup"><span data-stu-id="e3c00-105">It then describes how these concepts are expressed in Microsoft Media Foundation using media types.</span></span>

-   [<span data-ttu-id="e3c00-106">Rapport hauteur/largeur des images</span><span class="sxs-lookup"><span data-stu-id="e3c00-106">Picture Aspect Ratio</span></span>](#picture-aspect-ratio)
    -   [<span data-ttu-id="e3c00-107">Cadre</span><span class="sxs-lookup"><span data-stu-id="e3c00-107">Letterboxing</span></span>](#letterboxing)
    -   [<span data-ttu-id="e3c00-108">Panoramique et numérisation</span><span class="sxs-lookup"><span data-stu-id="e3c00-108">Pan-and-Scan</span></span>](#pan-and-scan)
-   [<span data-ttu-id="e3c00-109">Proportions de pixels</span><span class="sxs-lookup"><span data-stu-id="e3c00-109">Pixel Aspect Ratio</span></span>](#pixel-aspect-ratio)
-   [<span data-ttu-id="e3c00-110">Utilisation des proportions</span><span class="sxs-lookup"><span data-stu-id="e3c00-110">Working with Aspect Ratios</span></span>](#working-with-aspect-ratios)
-   [<span data-ttu-id="e3c00-111">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="e3c00-111">Code Examples</span></span>](#code-examples)
    -   [<span data-ttu-id="e3c00-112">Recherche de la zone d’affichage</span><span class="sxs-lookup"><span data-stu-id="e3c00-112">Finding the Display Area</span></span>](#finding-the-display-area)
    -   [<span data-ttu-id="e3c00-113">Conversion entre les proportions de pixels</span><span class="sxs-lookup"><span data-stu-id="e3c00-113">Converting Between Pixel Aspect Ratios</span></span>](#converting-between-pixel-aspect-ratios)
    -   [<span data-ttu-id="e3c00-114">Calcul de la zone de bandes</span><span class="sxs-lookup"><span data-stu-id="e3c00-114">Calculating the Letterbox Area</span></span>](#calculating-the-letterbox-area)
-   [<span data-ttu-id="e3c00-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3c00-115">Related topics</span></span>](#related-topics)

## <a name="picture-aspect-ratio"></a><span data-ttu-id="e3c00-116">Rapport hauteur/largeur des images</span><span class="sxs-lookup"><span data-stu-id="e3c00-116">Picture Aspect Ratio</span></span>

<span data-ttu-id="e3c00-117">Les proportions d' *image* définissent la forme de l’image vidéo affichée.</span><span class="sxs-lookup"><span data-stu-id="e3c00-117">*Picture aspect ratio* defines the shape of the displayed video image.</span></span> <span data-ttu-id="e3c00-118">Les proportions d’image sont X :Y, où X :Y est le rapport entre la largeur de l’image et la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="e3c00-118">Picture aspect ratio is notated X:Y, where X:Y is the ratio of picture width to picture height.</span></span> <span data-ttu-id="e3c00-119">La plupart des normes vidéo utilisent le rapport hauteur/largeur des images 4:3 ou 16:9.</span><span class="sxs-lookup"><span data-stu-id="e3c00-119">Most video standards use either 4:3 or 16:9 picture aspect ratio.</span></span> <span data-ttu-id="e3c00-120">Les proportions 16:9 sont généralement appelées *panoramiques*.</span><span class="sxs-lookup"><span data-stu-id="e3c00-120">The 16:9 aspect ratio is commonly called *widescreen*.</span></span> <span data-ttu-id="e3c00-121">Le film cinématographique utilise souvent des proportions 1:85:1 ou 1:66:1.</span><span class="sxs-lookup"><span data-stu-id="e3c00-121">Cinema film often uses a 1:85:1 or 1:66:1 aspect ratio.</span></span> <span data-ttu-id="e3c00-122">Les proportions de l’image sont également appelées proportions d' *affichage* (Dar).</span><span class="sxs-lookup"><span data-stu-id="e3c00-122">Picture aspect ratio is also called *display aspect ratio* (DAR).</span></span>

![Diagramme montrant les proportions 4:3 et 16:9](images/aspect-ratio01.png)

<span data-ttu-id="e3c00-124">Parfois, l’image vidéo n’a pas la même forme que la zone d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3c00-124">Sometimes the video image does not have the same shape as the display area.</span></span> <span data-ttu-id="e3c00-125">Par exemple, une vidéo 4:3 peut être affichée sur un téléviseur grand écran (16 × 9).</span><span class="sxs-lookup"><span data-stu-id="e3c00-125">For example, a 4:3 video might be shown on a widescreen (16×9) television.</span></span> <span data-ttu-id="e3c00-126">Dans une vidéo informatique, la vidéo peut être affichée à l’intérieur d’une fenêtre qui a une taille arbitraire.</span><span class="sxs-lookup"><span data-stu-id="e3c00-126">In computer video, the video might be shown inside a window that has an arbitrary size.</span></span> <span data-ttu-id="e3c00-127">Dans ce cas, il existe trois façons d’ajuster l’image dans la zone d’affichage :</span><span class="sxs-lookup"><span data-stu-id="e3c00-127">In that case, there are three ways the image can be made to fit within the display area:</span></span>

-   <span data-ttu-id="e3c00-128">Étirer l’image le long d’un axe pour l’ajuster à la zone d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3c00-128">Stretch the image along one axis to fit the display area.</span></span>
-   <span data-ttu-id="e3c00-129">Mettez l’image à l’échelle pour l’ajuster à la zone d’affichage tout en conservant les proportions d’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="e3c00-129">Scale the image to fit the display area, while maintaining the original picture aspect ratio.</span></span>
-   <span data-ttu-id="e3c00-130">Rognez l’image.</span><span class="sxs-lookup"><span data-stu-id="e3c00-130">Crop the image.</span></span>

<span data-ttu-id="e3c00-131">L’étirement de l’image pour l’ajuster à la zone d’affichage est presque toujours incorrect, car elle ne conserve pas les proportions de l’image correctes.</span><span class="sxs-lookup"><span data-stu-id="e3c00-131">Stretching the image to fit the display area is almost always wrong, because it does not preserve the correct picture aspect ratio.</span></span>

### <a name="letterboxing"></a><span data-ttu-id="e3c00-132">Cadre</span><span class="sxs-lookup"><span data-stu-id="e3c00-132">Letterboxing</span></span>

<span data-ttu-id="e3c00-133">Le processus de mise à l’échelle d’une image grand écran pour l’adapter à un affichage 4:3 est appelé *cadre*, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="e3c00-133">The process of scaling a widescreen image to fit a 4:3 display is called *letterboxing*, shown in the next diagram.</span></span> <span data-ttu-id="e3c00-134">Les zones de rectanglular résultantes en haut et en bas de l’image sont généralement remplies en noir, bien que d’autres couleurs puissent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="e3c00-134">The resulting rectanglular areas at the top and bottom of the image are typically filled with black, although other colors can be used.</span></span>

![Diagramme montrant la bonne façon de les bandes](images/aspect-ratio02.png)

<span data-ttu-id="e3c00-136">La casse inverse, avec la mise à l’échelle d’une image 4:3 pour l’adapter à un écran panoramique, est parfois appelée *pillarboxing*.</span><span class="sxs-lookup"><span data-stu-id="e3c00-136">The reverse case, scaling a 4:3 image to fit a widescreen display, is sometimes called *pillarboxing*.</span></span> <span data-ttu-id="e3c00-137">Toutefois, *le terme de* la zone de données est également utilisé dans un sens général, pour signifier la mise à l’échelle d’une image vidéo pour l’adapter à une zone d’affichage donnée.</span><span class="sxs-lookup"><span data-stu-id="e3c00-137">However, the term *letterbox* is also used in a general sense, to mean scaling a video image to fit any given display area.</span></span>

![Diagramme montrant pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a><span data-ttu-id="e3c00-139">Panoramique et numérisation</span><span class="sxs-lookup"><span data-stu-id="e3c00-139">Pan-and-Scan</span></span>

<span data-ttu-id="e3c00-140">Le panoramique et l’analyse sont une technique par laquelle une image panoramique est rognée dans une zone rectangulaire de 4 × 3, pour être affichée sur un appareil d’affichage 4:3.</span><span class="sxs-lookup"><span data-stu-id="e3c00-140">Pan-and-scan is a technique whereby a widescreen image is cropped to a 4×3 rectangular area, for display on a 4:3 display device.</span></span> <span data-ttu-id="e3c00-141">L’image obtenue remplit l’intégralité de l’affichage, sans nécessiter de zones de bandes noires, mais les parties de l’image d’origine sont rognées de l’image.</span><span class="sxs-lookup"><span data-stu-id="e3c00-141">The resulting image fills the entire display, without requiring black letterbox areas, but portions of the original image are cropped out of the picture.</span></span> <span data-ttu-id="e3c00-142">La zone rognée peut se déplacer d’un cadre à l’autres, comme la zone d’intérêt change.</span><span class="sxs-lookup"><span data-stu-id="e3c00-142">The area that is cropped can move from frame to frame, as the area of interest shifts.</span></span> <span data-ttu-id="e3c00-143">Le terme « panoramique » dans *panoramique et numérisation* fait référence à l’effet panoramique provoqué par le déplacement de la zone panoramique-et-numérisation.</span><span class="sxs-lookup"><span data-stu-id="e3c00-143">The term "pan" in *pan-and-scan* refers to the panning effect that is caused by moving the pan-and-scan area.</span></span>

![Diagramme montrant le panoramique et l’analyse](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a><span data-ttu-id="e3c00-145">Proportions de pixels</span><span class="sxs-lookup"><span data-stu-id="e3c00-145">Pixel Aspect Ratio</span></span>

<span data-ttu-id="e3c00-146">Les proportions en *pixels* (par) mesurent la forme d’un pixel.</span><span class="sxs-lookup"><span data-stu-id="e3c00-146">*Pixel aspect ratio* (PAR) measures the shape of a pixel.</span></span>

<span data-ttu-id="e3c00-147">Lorsqu’une image numérique est capturée, l’image est échantillonnée à la fois verticalement et horizontalement, ce qui se traduit par un tableau rectangulaire d’échantillons quantifiés, appelé *pixels* ou *pixels*.</span><span class="sxs-lookup"><span data-stu-id="e3c00-147">When a digital image is captured, the image is sampled both vertically and horizontally, resulting in a rectangular array of quantized samples, called *pixels* or *pels*.</span></span> <span data-ttu-id="e3c00-148">La forme de la grille d’échantillonnage détermine la forme des pixels de l’image numérisée.</span><span class="sxs-lookup"><span data-stu-id="e3c00-148">The shape of the sampling grid determines the shape of the pixels in the digitized image.</span></span>

<span data-ttu-id="e3c00-149">Voici un exemple qui utilise des nombres réduits pour simplifier la mathématique.</span><span class="sxs-lookup"><span data-stu-id="e3c00-149">Here is an example that uses small numbers to keep the math simple.</span></span> <span data-ttu-id="e3c00-150">Supposons que l’image d’origine est carrée (autrement dit, les proportions de l’image sont 1:1); et supposons que la grille d’échantillonnage contient 12 éléments, organisés en une grille 4 × 3.</span><span class="sxs-lookup"><span data-stu-id="e3c00-150">Suppose that the original image is square (that is, the picture aspect ratio is 1:1); and suppose the sampling grid contains 12 elements, arranged in a 4×3 grid.</span></span> <span data-ttu-id="e3c00-151">La forme de chaque pixel résultant sera plus grande que la largeur.</span><span class="sxs-lookup"><span data-stu-id="e3c00-151">The shape of each resulting pixel will be taller than it is wide.</span></span> <span data-ttu-id="e3c00-152">Plus précisément, la forme de chaque pixel sera 3 × 4.</span><span class="sxs-lookup"><span data-stu-id="e3c00-152">Specifically, the shape of each pixel will be 3×4.</span></span> <span data-ttu-id="e3c00-153">Les pixels qui ne sont pas des carrés sont appelés des *pixels non carrés*.</span><span class="sxs-lookup"><span data-stu-id="e3c00-153">Pixels that are not square are called *non-square pixels*.</span></span>

![Diagramme montrant une grille d’échantillonnage non carrée](images/aspect-ratio05.png)

<span data-ttu-id="e3c00-155">Les proportions de pixels s’appliquent également au périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3c00-155">Pixel aspect ratio also applies to the display device.</span></span> <span data-ttu-id="e3c00-156">La forme physique du périphérique d’affichage et la résolution de pixel physique (en travers et en baisse) déterminent le pair du périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="e3c00-156">The physical shape of the display device and the physical pixel resolution (across and down) determine the PAR of the display device.</span></span> <span data-ttu-id="e3c00-157">Les moniteurs d’ordinateur utilisent généralement des pixels carrés.</span><span class="sxs-lookup"><span data-stu-id="e3c00-157">Computer monitors generally use square pixels.</span></span> <span data-ttu-id="e3c00-158">Si l’image PAR et l’affichage PAR ne correspondent pas, l’image doit être mise à l’échelle dans une dimension, verticalement ou horizontalement, afin de s’afficher correctement.</span><span class="sxs-lookup"><span data-stu-id="e3c00-158">If the image PAR and the display PAR do not match, the image must be scaled in one dimension, either vertically or horizontally, in order to display correctly.</span></span> <span data-ttu-id="e3c00-159">La formule suivante est associée à, à l’aspect des proportions (DAR) et à la taille de l’image en pixels :</span><span class="sxs-lookup"><span data-stu-id="e3c00-159">The following formula relates PAR, display aspect ratio (DAR), and image size in pixels:</span></span>

<span data-ttu-id="e3c00-160">*Dar* = (*largeur de l’image en pixels*  /  *hauteur de l’image en pixels*) × *par*</span><span class="sxs-lookup"><span data-stu-id="e3c00-160">*DAR* = (*image width in pixels* / *image height in pixels*) × *PAR*</span></span>

<span data-ttu-id="e3c00-161">Notez que la largeur de l’image et la hauteur de l’image dans cette formule font référence à l’image en mémoire, et non à l’image affichée.</span><span class="sxs-lookup"><span data-stu-id="e3c00-161">Note that image width and image height in this formula refer to the image in memory, not the displayed image.</span></span>

<span data-ttu-id="e3c00-162">Voici un exemple concret : la vidéo analogique NTSC-M contient 480 lignes de numérisation dans la zone d’image active.</span><span class="sxs-lookup"><span data-stu-id="e3c00-162">Here is a real-world example: NTSC-M analog video contains 480 scan lines in the active image area.</span></span> <span data-ttu-id="e3c00-163">ITU-R Rec. BT. 601 spécifie un taux d’échantillonnage horizontal de 704 pixels visibles par ligne, ce qui génère une image numérique avec 704 x 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="e3c00-163">ITU-R Rec. BT.601 specifies a horizontal sampling rate of 704 visible pixels per line, yielding a digital image with 704 x 480 pixels.</span></span> <span data-ttu-id="e3c00-164">Les proportions de l’image prévues sont 4:3, ce qui donne un pas de 10:11.</span><span class="sxs-lookup"><span data-stu-id="e3c00-164">The intended picture aspect ratio is 4:3, yielding a PAR of 10:11.</span></span>

-   <span data-ttu-id="e3c00-165">DAR : 4:3</span><span class="sxs-lookup"><span data-stu-id="e3c00-165">DAR: 4:3</span></span>
-   <span data-ttu-id="e3c00-166">Largeur en pixels : 704</span><span class="sxs-lookup"><span data-stu-id="e3c00-166">Width in pixels: 704</span></span>
-   <span data-ttu-id="e3c00-167">Hauteur en pixels : 480</span><span class="sxs-lookup"><span data-stu-id="e3c00-167">Height in pixels: 480</span></span>
-   <span data-ttu-id="e3c00-168">PAR : 10/11</span><span class="sxs-lookup"><span data-stu-id="e3c00-168">PAR: 10/11</span></span>

<span data-ttu-id="e3c00-169">4/3 = (704/420) x (10/11)</span><span class="sxs-lookup"><span data-stu-id="e3c00-169">4/3 = (704/420) x (10/11)</span></span>

<span data-ttu-id="e3c00-170">Pour afficher correctement cette image sur un appareil d’affichage avec des pixels carrés, vous devez mettre à l’échelle la largeur par 10/11 ou la hauteur de 11/10.</span><span class="sxs-lookup"><span data-stu-id="e3c00-170">To display this image correctly on a display device with square pixels, you must scale either the width by 10/11 or the height by 11/10.</span></span>

## <a name="working-with-aspect-ratios"></a><span data-ttu-id="e3c00-171">Utilisation des proportions</span><span class="sxs-lookup"><span data-stu-id="e3c00-171">Working with Aspect Ratios</span></span>

<span data-ttu-id="e3c00-172">La forme correcte d’une image vidéo est définie par le proportions en *pixels* (par) et la *zone d’affichage*.</span><span class="sxs-lookup"><span data-stu-id="e3c00-172">The correct shape of a video frame is defined by the *pixel aspect ratio* (PAR) and the *display area*.</span></span>

-   <span data-ttu-id="e3c00-173">Le pair définit la forme des pixels dans une image.</span><span class="sxs-lookup"><span data-stu-id="e3c00-173">The PAR defines the shape of the pixels in an image.</span></span> <span data-ttu-id="e3c00-174">Les pixels carrés ont un rapport hauteur/largeur de 1:1.</span><span class="sxs-lookup"><span data-stu-id="e3c00-174">Square pixels have an aspect ratio of 1:1.</span></span> <span data-ttu-id="e3c00-175">Tout autre rapport hauteur/largeur décrit un pixel non carré.</span><span class="sxs-lookup"><span data-stu-id="e3c00-175">Any other aspect ratio describes a non-square pixel.</span></span> <span data-ttu-id="e3c00-176">Par exemple, la télévision NTSC utilise une PAR 10:11.</span><span class="sxs-lookup"><span data-stu-id="e3c00-176">For example, NTSC television uses a 10:11 PAR.</span></span> <span data-ttu-id="e3c00-177">En supposant que vous présentiez la vidéo sur un moniteur d’ordinateur, l’affichage présente des pixels carrés (1:1 PAR).</span><span class="sxs-lookup"><span data-stu-id="e3c00-177">Assuming that you are presenting the video on a computer monitor, the display will have square pixels (1:1 PAR).</span></span> <span data-ttu-id="e3c00-178">Le pair du contenu source est fourni dans l’attribut de proportions [**MF \_ Mt en \_ \_ \_ pixels**](mf-mt-pixel-aspect-ratio-attribute.md) sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="e3c00-178">The PAR of the source content is given in the [**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute on the media type.</span></span>
-   <span data-ttu-id="e3c00-179">La zone d’affichage est la région de l’image vidéo qui est destinée à être affichée.</span><span class="sxs-lookup"><span data-stu-id="e3c00-179">The display area is the region of the video image that is intended to be shown.</span></span> <span data-ttu-id="e3c00-180">Deux zones d’affichage pertinentes peuvent être spécifiées dans le type de média :</span><span class="sxs-lookup"><span data-stu-id="e3c00-180">There are two relevant display areas that might be specified in the media type:</span></span>
    -   <span data-ttu-id="e3c00-181">Ouverture pan-and-Scan.</span><span class="sxs-lookup"><span data-stu-id="e3c00-181">Pan-and-scan aperture.</span></span> <span data-ttu-id="e3c00-182">L’ouverture pan-and-Scan est une région 4 × 3 de vidéo qui doit être affichée en mode panoramique/numérisation.</span><span class="sxs-lookup"><span data-stu-id="e3c00-182">The pan-and-scan aperture is a 4×3 region of video that should be displayed in pan/scan mode.</span></span> <span data-ttu-id="e3c00-183">Il est utilisé pour afficher un contenu à grand écran sur un affichage 4 × 3 sans cadre.</span><span class="sxs-lookup"><span data-stu-id="e3c00-183">It is used to show wide-screen content on a 4×3 display without letterboxing.</span></span> <span data-ttu-id="e3c00-184">L’ouverture de la panoramisation et de l’analyse est indiquée dans l’attribut de l’ouverture de l' [**\_ \_ \_ \_ analyse panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md) et doit être utilisée uniquement lorsque l’attribut d’activation de l' [**\_ \_ \_ analyse \_ panoramique MF MT**](mf-mt-pan-scan-enabled-attribute.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="e3c00-184">The pan-and-scan aperture is given in the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute and should be used only when the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute is **TRUE**.</span></span>
    -   <span data-ttu-id="e3c00-185">Afficher l’ouverture.</span><span class="sxs-lookup"><span data-stu-id="e3c00-185">Display aperture.</span></span> <span data-ttu-id="e3c00-186">Cette ouverture est définie dans certaines normes vidéo.</span><span class="sxs-lookup"><span data-stu-id="e3c00-186">This aperture is defined in some video standards.</span></span> <span data-ttu-id="e3c00-187">Tout ce qui se trouve en dehors de l’ouverture d’affichage est la région de suranalyse et ne doit pas être affiché.</span><span class="sxs-lookup"><span data-stu-id="e3c00-187">Anything outside of the display aperture is the overscan region and should not be displayed.</span></span> <span data-ttu-id="e3c00-188">Par exemple, la télévision NTSC est de 720 × 480 pixels avec une ouverture d’affichage de 704 × 480.</span><span class="sxs-lookup"><span data-stu-id="e3c00-188">For example, NTSC television is 720×480 pixels with a display aperture of 704×480.</span></span> <span data-ttu-id="e3c00-189">L’ouverture de l’affichage est indiquée dans l’attribut de l’ouverture de l’affichage de la version d' [**\_ \_ \_ \_ affichage minimale MF MT**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e3c00-189">The display aperture is given in the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span> <span data-ttu-id="e3c00-190">S’il est présent, il doit être utilisé lorsque le mode pan-and-Scan a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="e3c00-190">If present, it should be used when pan-and-scan mode is **FALSE**.</span></span>

<span data-ttu-id="e3c00-191">Si le mode pan-and-can a la **valeur false** et qu’aucune ouverture n’est définie, la totalité de l’image vidéo doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="e3c00-191">If pan-and-can mode is **FALSE** and no display aperture is defined, the entire video frame should be displayed.</span></span> <span data-ttu-id="e3c00-192">En fait, c’est le cas pour la plupart des contenus vidéo autres que la télévision et les vidéos DVD.</span><span class="sxs-lookup"><span data-stu-id="e3c00-192">In fact, this is the case for most video content other than television and DVD video.</span></span> <span data-ttu-id="e3c00-193">Les proportions de l’image entière sont calculées en fonction de la largeur de la zone d’affichage (largeur de la *zone d’affichage*  /  ) × *par*.</span><span class="sxs-lookup"><span data-stu-id="e3c00-193">The aspect ratio of the entire picture is calculated as (*display area width* / *display area height*) × *PAR*.</span></span>

## <a name="code-examples"></a><span data-ttu-id="e3c00-194">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="e3c00-194">Code Examples</span></span>

### <a name="finding-the-display-area"></a><span data-ttu-id="e3c00-195">Recherche de la zone d’affichage</span><span class="sxs-lookup"><span data-stu-id="e3c00-195">Finding the Display Area</span></span>

<span data-ttu-id="e3c00-196">Le code suivant montre comment obtenir la zone d’affichage à partir du type de média.</span><span class="sxs-lookup"><span data-stu-id="e3c00-196">The following code shows how to get the display area from the media type.</span></span>


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a><span data-ttu-id="e3c00-197">Conversion entre les proportions de pixels</span><span class="sxs-lookup"><span data-stu-id="e3c00-197">Converting Between Pixel Aspect Ratios</span></span>

<span data-ttu-id="e3c00-198">Le code suivant montre comment convertir un rectangle d’un proportions de pixels (PAR) en un autre, tout en conservant les proportions d’image.</span><span class="sxs-lookup"><span data-stu-id="e3c00-198">The following code shows how to convert a rectangle from one pixel aspect ratio (PAR) to another, while preserving the picture aspect ratio.</span></span>


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a><span data-ttu-id="e3c00-199">Calcul de la zone de bandes</span><span class="sxs-lookup"><span data-stu-id="e3c00-199">Calculating the Letterbox Area</span></span>

<span data-ttu-id="e3c00-200">Le code suivant calcule la zone de bandes en fonction d’un rectangle source et d’un rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="e3c00-200">The following code calculates the letterbox area, given a source and destination rectangle.</span></span> <span data-ttu-id="e3c00-201">Il est supposé que les deux rectangles ont le même PAR.</span><span class="sxs-lookup"><span data-stu-id="e3c00-201">It is assumed that both rectangles have the same PAR.</span></span>


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a><span data-ttu-id="e3c00-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3c00-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3c00-203">Types de médias</span><span class="sxs-lookup"><span data-stu-id="e3c00-203">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="e3c00-204">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="e3c00-204">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="e3c00-205">**\_ouverture de \_ l' \_ affichage \_ de la version MF**</span><span class="sxs-lookup"><span data-stu-id="e3c00-205">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="e3c00-206">**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**</span><span class="sxs-lookup"><span data-stu-id="e3c00-206">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="e3c00-207">**\_ \_ analyse panoramique MF \_ MT \_ activée**</span><span class="sxs-lookup"><span data-stu-id="e3c00-207">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[<span data-ttu-id="e3c00-208">**\_ \_ \_ rapport hauteur/largeur des pixels \_ MF**</span><span class="sxs-lookup"><span data-stu-id="e3c00-208">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



