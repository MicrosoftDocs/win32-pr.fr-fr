---
title: Spécification des ressources d’image du ruban
description: En tant que système de présentation de commande riche, l’infrastructure de ruban Windows est conçue pour prendre en charge les ressources d’image de manière intensive tout au long de l’interface utilisateur du ruban. Toutes les ressources d’image sont déclarées dans le balisage du ruban ou interrogées à partir d’une application hôte du ruban.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Ruban Windows, ressources d’image
- Ruban, ressources d’image
- Ruban Windows, transparence
- Ruban, transparence
- Ruban Windows, profondeur de couleur
- Ruban, profondeur de couleur
- Ruban Windows, contraste
- Ruban, contraste
- ressources d’image dans le ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463547"
---
# <a name="specifying-ribbon-image-resources"></a><span data-ttu-id="d6e00-113">Spécification des ressources d’image du ruban</span><span class="sxs-lookup"><span data-stu-id="d6e00-113">Specifying Ribbon Image Resources</span></span>

<span data-ttu-id="d6e00-114">En tant que système de présentation de commande riche, l’infrastructure de ruban Windows est conçue pour prendre en charge les ressources d’image de manière intensive tout au long de l’interface utilisateur du ruban.</span><span class="sxs-lookup"><span data-stu-id="d6e00-114">As a rich command presentation system, the Windows Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="d6e00-115">Toutes les ressources d’image sont déclarées dans le [balisage du ruban](windowsribbon-schema.md) ou interrogées à partir d’une application hôte du ruban.</span><span class="sxs-lookup"><span data-stu-id="d6e00-115">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="d6e00-116">Pour Windows 8 et versions ultérieures, l’infrastructure du ruban prend en charge les formats graphiques suivants : fichiers BMP (bitmaps) 32 bits et fichiers PNG (Portable Network Graphics) avec transparence.</span><span class="sxs-lookup"><span data-stu-id="d6e00-116">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="d6e00-117">Pour Windows 7 et les versions antérieures, les ressources d’image doivent être conformes au format graphique BMP standard utilisé dans Windows.</span><span class="sxs-lookup"><span data-stu-id="d6e00-117">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="d6e00-118">Une erreur de compilation peut se produire si un format d’image non pris en charge est fourni à l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="d6e00-118">A compilation error may occur if an unsupported image format is supplied to the framework.</span></span>

 

## <a name="image-sizes"></a><span data-ttu-id="d6e00-119">Tailles d’image</span><span class="sxs-lookup"><span data-stu-id="d6e00-119">Image Sizes</span></span>

<span data-ttu-id="d6e00-120">Pour offrir une plus grande flexibilité pour les dispositions de contrôle de ruban lors du redimensionnement d’une fenêtre d’application, l’infrastructure du ruban accepte et affiche les images dans l’une des deux tailles suivantes : grande ou petite.</span><span class="sxs-lookup"><span data-stu-id="d6e00-120">To provide greater flexibility for Ribbon control layouts when resizing an application window, the Ribbon framework accepts and renders images in one of two sizes: large or small.</span></span>

<span data-ttu-id="d6e00-121">Les images suivantes illustrent une application de ruban qui prend en charge plusieurs tailles de ruban grâce à des dispositions de contrôle flexibles et au remplacement d’images volumineuses par des images de petite taille disponibles.</span><span class="sxs-lookup"><span data-stu-id="d6e00-121">The following images illustrate a Ribbon application that supports multiple Ribbon sizes through flexible control layouts and the replacement of large images with small images where available.</span></span>

<span data-ttu-id="d6e00-122">La capture d’écran suivante montre le ruban avec des images de grande taille pour les contrôles de zoom.</span><span class="sxs-lookup"><span data-stu-id="d6e00-122">The following screen shot shows the Ribbon with large images for the Zoom controls.</span></span>

![capture d’écran montrant un ruban qui utilise des images de grande taille pour les contrôles de zoom.](images/overviews/imageresources-largeimage.png)

<span data-ttu-id="d6e00-124">La capture d’écran suivante montre le même ruban redimensionné avec de petites images pour les contrôles de zoom</span><span class="sxs-lookup"><span data-stu-id="d6e00-124">The following screen shot shows the same Ribbon resized with small images for the Zoom controls</span></span>

![capture d’écran montrant un ruban qui utilise de petites images pour les contrôles de zoom.](images/overviews/imageresources-smallimage.png)

<span data-ttu-id="d6e00-126">La capture d’écran suivante montre le ruban dans un état masqué.</span><span class="sxs-lookup"><span data-stu-id="d6e00-126">The following screen shot shows the ribbon in hidden state.</span></span> <span data-ttu-id="d6e00-127">Le ruban est masqué lorsque toutes les dispositions de contrôle potentielles ont été épuisées et que le ruban ne peut pas être rendu avec un espace de travail d’application utilisable.</span><span class="sxs-lookup"><span data-stu-id="d6e00-127">The ribbon is hidden when all potential control layouts have been exhausted and the ribbon cannot be rendered with a usable application workspace.</span></span>

![capture d’écran montrant un ruban réduit.](images/overviews/imageresources-noimage.png)

<span data-ttu-id="d6e00-129">Pour toute image, la taille de pixel exacte dépend de la résolution d’affichage, ou des points par pouce (dpi), de l’analyse utilisée.</span><span class="sxs-lookup"><span data-stu-id="d6e00-129">For any image, the exact pixel size is dependent on the display resolution, or dots per inch (dpi), of the monitor being used.</span></span> <span data-ttu-id="d6e00-130">À 96 ppp, les images volumineuses ont une taille de 32x32 pixels et les images de petite taille sont de 16 x 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="d6e00-130">At 96 dpi, large images are 32x32 pixels in size and small images are 16x16 pixels in size.</span></span> <span data-ttu-id="d6e00-131">Les tailles d’image augmentent de manière linéaire par rapport à la fonction dpi, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d6e00-131">The image sizes increase in a linear fashion relative to dpi as illustrated in the following table.</span></span>



| <span data-ttu-id="d6e00-132">PPP</span><span class="sxs-lookup"><span data-stu-id="d6e00-132">DPI</span></span>     | <span data-ttu-id="d6e00-133">Petite image</span><span class="sxs-lookup"><span data-stu-id="d6e00-133">Small Image</span></span>  | <span data-ttu-id="d6e00-134">Grande image</span><span class="sxs-lookup"><span data-stu-id="d6e00-134">Large Image</span></span>  |
|---------|--------------|--------------|
| <span data-ttu-id="d6e00-135">96 ppp</span><span class="sxs-lookup"><span data-stu-id="d6e00-135">96 dpi</span></span>  | <span data-ttu-id="d6e00-136">16x16 pixels</span><span class="sxs-lookup"><span data-stu-id="d6e00-136">16x16 pixels</span></span> | <span data-ttu-id="d6e00-137">32 x 32 pixels</span><span class="sxs-lookup"><span data-stu-id="d6e00-137">32x32 pixels</span></span> |
| <span data-ttu-id="d6e00-138">120 ppp</span><span class="sxs-lookup"><span data-stu-id="d6e00-138">120 dpi</span></span> | <span data-ttu-id="d6e00-139">20x20 pixels</span><span class="sxs-lookup"><span data-stu-id="d6e00-139">20x20 pixels</span></span> | <span data-ttu-id="d6e00-140">40 x 40 pixels</span><span class="sxs-lookup"><span data-stu-id="d6e00-140">40x40 pixels</span></span> |
| <span data-ttu-id="d6e00-141">144 PPP</span><span class="sxs-lookup"><span data-stu-id="d6e00-141">144 dpi</span></span> | <span data-ttu-id="d6e00-142">24x24 pixels</span><span class="sxs-lookup"><span data-stu-id="d6e00-142">24x24 pixels</span></span> | <span data-ttu-id="d6e00-143">48 pixels</span><span class="sxs-lookup"><span data-stu-id="d6e00-143">48x48 pixels</span></span> |
| <span data-ttu-id="d6e00-144">192 PPP</span><span class="sxs-lookup"><span data-stu-id="d6e00-144">192 dpi</span></span> | <span data-ttu-id="d6e00-145">32 x 32 pixels</span><span class="sxs-lookup"><span data-stu-id="d6e00-145">32x32 pixels</span></span> | <span data-ttu-id="d6e00-146">64x64 pixels</span><span class="sxs-lookup"><span data-stu-id="d6e00-146">64x64 pixels</span></span> |



 

<span data-ttu-id="d6e00-147">L’infrastructure du ruban met à l’échelle les ressources d’image selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="d6e00-147">The Ribbon framework scales image resources as required.</span></span> <span data-ttu-id="d6e00-148">Toutefois, étant donné que le redimensionnement peut générer des artefacts indésirables et une dégradation des images, il est fortement recommandé que l’application fournisse un petit ensemble de ressources d’image qui s’étendent sur différents paramètres ppp couramment utilisés.</span><span class="sxs-lookup"><span data-stu-id="d6e00-148">However, because resizing may yield undesirable artifacts and image degradation, it is highly recommended that the application provide a small set of image resources that span various commonly used dpi settings.</span></span> <span data-ttu-id="d6e00-149">Si aucune correspondance exacte n’est trouvée, l’image la plus proche est mise à l’échelle vers le haut ou le bas.</span><span class="sxs-lookup"><span data-stu-id="d6e00-149">If an exact match is not found, the nearest image will be scaled up or down.</span></span>

<span data-ttu-id="d6e00-150">Pour faciliter cette tâche, les ressources d’image peuvent être déclarées dans le balisage du ruban à l’aide d’un ensemble d’éléments [**image**](windowsribbon-element-image.md) pour chaque élément [**Command**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e00-150">To facilitate this, image resources can be declared in Ribbon markup by using a set of [**Image**](windowsribbon-element-image.md) elements for each [**Command**](windowsribbon-element-command.md) element.</span></span> <span data-ttu-id="d6e00-151">Au moment de l’exécution, l’infrastructure sélectionne l’image à afficher en fonction de l’attribut *MinDPI* de chaque élément **image** .</span><span class="sxs-lookup"><span data-stu-id="d6e00-151">At run time, the framework selects the image to display based on the *MinDPI* attribute of each **Image** element.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="d6e00-152">Lorsqu’une collection de ressources d’image conçues pour prendre en charge des paramètres de résolution d’écran spécifiques est fournie à l’infrastructure du ruban via un ensemble d’éléments d' [**image**](windowsribbon-element-image.md) , l’infrastructure utilise l' **image** avec une valeur d’attribut *MinDPI* qui correspond au paramètre de dpi d’écran actuel.</span><span class="sxs-lookup"><span data-stu-id="d6e00-152">When a collection of image resources that are designed to support specific screen dpi settings is supplied to the Ribbon framework through a set of [**Image**](windowsribbon-element-image.md) elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>
>
> <span data-ttu-id="d6e00-153">Si aucun élément [**image**](windowsribbon-element-image.md) n’est déclaré avec une valeur *MinDPI* qui correspond au paramètre PPP d’écran actuel, l’infrastructure sélectionne l' **image** qui a la valeur *MinDPI* la plus proche inférieure au paramètre PPP d’écran actuel et met à l’échelle la ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="d6e00-153">If no [**Image**](windowsribbon-element-image.md) element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="d6e00-154">Sinon, si aucun élément **image** n’est déclaré avec une valeur d’attribut *MinDPI* inférieure au paramètre PPP d’écran actuel, le Framework choisit la valeur *MinDPI* la plus proche supérieure au paramètre PPP d’écran actuel et met à l’échelle la ressource d’image.</span><span class="sxs-lookup"><span data-stu-id="d6e00-154">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

 

<span data-ttu-id="d6e00-155">L’exemple suivant montre comment déclarer un ensemble d’images pour prendre en charge différentes tailles de ruban et paramètres système.</span><span class="sxs-lookup"><span data-stu-id="d6e00-155">The following example illustrates how to declare a set of images to accommodate various Ribbon sizes and system settings.</span></span>


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



<span data-ttu-id="d6e00-156">Si les images déclarées dans le balisage sont invalidées au moment de l’exécution pour une raison quelconque, l’application hôte est interrogée pour obtenir de nouvelles images.</span><span class="sxs-lookup"><span data-stu-id="d6e00-156">If images declared in markup are invalidated at run time for any reason, the host application is queried for new images.</span></span> <span data-ttu-id="d6e00-157">Lorsque ces images sont générées et chargées par programme, l’application doit tenter de retourner des images dimensionnées en fonction des tailles d’icône système par défaut déterminées par la [ \_ métrique du système CXICON SM](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span><span class="sxs-lookup"><span data-stu-id="d6e00-157">When these images are generated and loaded programmatically, the application should attempt to return images that are sized according to the default system icon sizes determined by the [SM\_CXICON system metric](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span></span>

> [!Note]  
> <span data-ttu-id="d6e00-158">Les images volumineuses ont une taille de SM \_ CXICON par SM \_ CXICON et les petites images ont une taille de SM \_ CXICON/2 par SM \_ CXICON/2.</span><span class="sxs-lookup"><span data-stu-id="d6e00-158">Large images have a size of SM\_CXICON by SM\_CXICON and small images have a size of SM\_CXICON/2 by SM\_CXICON/2.</span></span>

 

## <a name="color-depth-transparency-and-contrast"></a><span data-ttu-id="d6e00-159">Profondeur des couleurs, transparence et contraste</span><span class="sxs-lookup"><span data-stu-id="d6e00-159">Color Depth, Transparency, and Contrast</span></span>

<span data-ttu-id="d6e00-160">Les images normales sont supposées être au format de pixel ARVB 32 bits par pixel (BPP) et être mises à l’échelle en fonction de la taille des icônes système par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6e00-160">Regular images are expected to be in 32 bits per pixel (BPP) ARGB pixel format and scaled to the default system icon size.</span></span> <span data-ttu-id="d6e00-161">Ce format prend en charge la transparence et l’anticrénelage (à l’aide de 8 bits par canal).</span><span class="sxs-lookup"><span data-stu-id="d6e00-161">This format supports both transparency and antialiasing (using 8 bits per channel).</span></span>

> [!WARNING]
> <span data-ttu-id="d6e00-162">De nombreux outils d’édition d’images ne conservent pas le canal alpha 8 bits d’ordre le plus élevé lors du chargement ou de l’enregistrement des images 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="d6e00-162">Many image editing tools do not preserve the highest order 8-bit alpha channel when loading or saving 32 BPP images.</span></span>

 

<span data-ttu-id="d6e00-163">Pour qu’une image s’affiche correctement en mode de contraste élevé, elle doit être dans un format de pixel de palette de 4 BPP.</span><span class="sxs-lookup"><span data-stu-id="d6e00-163">For an image to display correctly in high-contrast mode, it must be in a 4 BPP palletized pixel format.</span></span> <span data-ttu-id="d6e00-164">Lorsque l’image est rendue, l’infrastructure du ruban remappe des couleurs spécifiques en fonction du contexte de contraste élevé de l’image.</span><span class="sxs-lookup"><span data-stu-id="d6e00-164">When the image is rendered, the Ribbon framework remaps specific colors based on the high-contrast context of the image.</span></span>

<span data-ttu-id="d6e00-165">Le tableau suivant répertorie le comportement de rendu des couleurs à contraste élevé de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="d6e00-165">The following table lists the high-contrast color rendering behavior of the framework.</span></span>



<span data-ttu-id="d6e00-166">Couleur du pixel</span><span class="sxs-lookup"><span data-stu-id="d6e00-166">Pixel color</span></span>

<span data-ttu-id="d6e00-167">Valeur RVB</span><span class="sxs-lookup"><span data-stu-id="d6e00-167">RGB value</span></span>

<span data-ttu-id="d6e00-168">Comportement</span><span class="sxs-lookup"><span data-stu-id="d6e00-168">Behavior</span></span>

<span data-ttu-id="d6e00-169">Arrière-plan blanc</span><span class="sxs-lookup"><span data-stu-id="d6e00-169">White background</span></span>

<span data-ttu-id="d6e00-170">Arrière-plan foncé</span><span class="sxs-lookup"><span data-stu-id="d6e00-170">Dark Background</span></span>

<span data-ttu-id="d6e00-171">MARRON</span><span class="sxs-lookup"><span data-stu-id="d6e00-171">MAGENTA</span></span>

<span data-ttu-id="d6e00-172">800080</span><span class="sxs-lookup"><span data-stu-id="d6e00-172">800080</span></span>

<span data-ttu-id="d6e00-173">Mode transparent</span><span class="sxs-lookup"><span data-stu-id="d6e00-173">Transparent</span></span>

<span data-ttu-id="d6e00-174">Mode transparent</span><span class="sxs-lookup"><span data-stu-id="d6e00-174">Transparent</span></span>

<span data-ttu-id="d6e00-175">FOND</span><span class="sxs-lookup"><span data-stu-id="d6e00-175">BLACK</span></span>

<span data-ttu-id="d6e00-176">000000</span><span class="sxs-lookup"><span data-stu-id="d6e00-176">000000</span></span>

<span data-ttu-id="d6e00-177">WINDOWTEXT de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="d6e00-177">COLOR\_WINDOWTEXT</span></span>

<span data-ttu-id="d6e00-178">AJOURÉE</span><span class="sxs-lookup"><span data-stu-id="d6e00-178">WHITE</span></span>

<span data-ttu-id="d6e00-179">AJOURÉE</span><span class="sxs-lookup"><span data-stu-id="d6e00-179">WHITE</span></span>

<span data-ttu-id="d6e00-180">FFFFFF</span><span class="sxs-lookup"><span data-stu-id="d6e00-180">FFFFFF</span></span>

<span data-ttu-id="d6e00-181">fenêtre de couleur \_</span><span class="sxs-lookup"><span data-stu-id="d6e00-181">COLOR\_WINDOW</span></span>

<span data-ttu-id="d6e00-182">FOND</span><span class="sxs-lookup"><span data-stu-id="d6e00-182">BLACK</span></span>

<span data-ttu-id="d6e00-183">GRIS FONCÉ</span><span class="sxs-lookup"><span data-stu-id="d6e00-183">DARK GRAY</span></span>

<span data-ttu-id="d6e00-184">808080</span><span class="sxs-lookup"><span data-stu-id="d6e00-184">808080</span></span>

<span data-ttu-id="d6e00-185">3DSHADOW de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="d6e00-185">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="d6e00-186">3DSHADOW de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="d6e00-186">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="d6e00-187">COCHÉ</span><span class="sxs-lookup"><span data-stu-id="d6e00-187">GRAY</span></span>

<span data-ttu-id="d6e00-188">C0C0C0</span><span class="sxs-lookup"><span data-stu-id="d6e00-188">C0C0C0</span></span>

<span data-ttu-id="d6e00-189">3DFACE de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="d6e00-189">COLOR\_3DFACE</span></span>

<span data-ttu-id="d6e00-190">3DFACE de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="d6e00-190">COLOR\_3DFACE</span></span>

<span data-ttu-id="d6e00-191">GRIS CLAIR</span><span class="sxs-lookup"><span data-stu-id="d6e00-191">LIGHT GRAY</span></span>

<span data-ttu-id="d6e00-192">DFDFDF</span><span class="sxs-lookup"><span data-stu-id="d6e00-192">DFDFDF</span></span>

<span data-ttu-id="d6e00-193">3DLIGHT de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="d6e00-193">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="d6e00-194">3DLIGHT de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="d6e00-194">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="d6e00-195">BLEU FONCÉ</span><span class="sxs-lookup"><span data-stu-id="d6e00-195">DARK BLUE</span></span>

<span data-ttu-id="d6e00-196">000080</span><span class="sxs-lookup"><span data-stu-id="d6e00-196">000080</span></span>

<span data-ttu-id="d6e00-197">n/a</span><span class="sxs-lookup"><span data-stu-id="d6e00-197">n/a</span></span>

<span data-ttu-id="d6e00-198">AJOURÉE</span><span class="sxs-lookup"><span data-stu-id="d6e00-198">WHITE</span></span>



 

<span data-ttu-id="d6e00-199">Pour plus d’informations sur les formats d’image pris en charge par l’infrastructure du ruban, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6e00-199">For more information on the image formats supported by the Ribbon framework, see the following:</span></span>

-   <span data-ttu-id="d6e00-200">[Structure BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) -décrit le format de pixel 32 BPP ARVB.</span><span class="sxs-lookup"><span data-stu-id="d6e00-200">[BITMAPINFOHEADER structure](/previous-versions//dd183376(v=vs.85)) - describes the 32 BPP ARGB pixel format.</span></span>
-   <span data-ttu-id="d6e00-201">[CreateDIBSection fonction](/windows/win32/api/wingdi/nf-wingdi-createdibsection) -décrit comment créer une image au format de pixel ARVB 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="d6e00-201">[CreateDIBSection function](/windows/win32/api/wingdi/nf-wingdi-createdibsection) - describes how to create a 32 BPP ARGB pixel format image.</span></span>
-   <span data-ttu-id="d6e00-202">[LoadImage fonction](/windows/win32/api/winuser/nf-winuser-loadimagea) -décrit comment charger une image au format de pixel ARVB 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="d6e00-202">[LoadImage function](/windows/win32/api/winuser/nf-winuser-loadimagea) - describes how to load a 32 BPP ARGB pixel format image.</span></span>

## <a name="accessibility"></a><span data-ttu-id="d6e00-203">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="d6e00-203">Accessibility</span></span>

<span data-ttu-id="d6e00-204">S’appuyer sur des ressources d’image pour fournir des informations, transmettre des fonctionnalités de contrôle et exposer l’état de l’application, augmente la nécessité d’exigences d’accessibilité lors de la conception et du développement de l’application.</span><span class="sxs-lookup"><span data-stu-id="d6e00-204">Relying on image resources to provide information, convey control functionality, and expose application state, increases the need for accessibility requirements during application design and development.</span></span>

<span data-ttu-id="d6e00-205">Pour la prise en charge du contraste élevé de base, le ruban permet d’afficher un ensemble distinct de fichiers image quand un thème à contraste élevé est actif.</span><span class="sxs-lookup"><span data-stu-id="d6e00-205">For basic high contrast support, the Ribbon allows for a separate set of image files to be displayed when a high-contrast theme is active.</span></span> <span data-ttu-id="d6e00-206">Ces images peuvent être de 32 ou de 4 BPP, avec des couleurs mappées à une palette spéciale dans laquelle les couleurs sombres et claires sont inversées en fonction des couleurs de premier plan et d’arrière-plan du thème actif à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="d6e00-206">These images can be 32 BPP or 4 BPP, with colors mapped to a special palette where dark and light colors are inverted depending on the foreground and background colors of the active high-contrast theme.</span></span>

<span data-ttu-id="d6e00-207">L’exemple suivant montre comment les ressources d’image à contraste élevé sont déclarées dans le balisage du ruban :</span><span class="sxs-lookup"><span data-stu-id="d6e00-207">The following example demonstrates how high-contrast image resources are declared in Ribbon markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="d6e00-208">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6e00-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6e00-209">**Commande. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="d6e00-209">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[<span data-ttu-id="d6e00-210">IU \_ \_ SmallImage</span><span class="sxs-lookup"><span data-stu-id="d6e00-210">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[<span data-ttu-id="d6e00-211">**Commande. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="d6e00-211">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[<span data-ttu-id="d6e00-212">IU \_ \_ LARGEIMAGE</span><span class="sxs-lookup"><span data-stu-id="d6e00-212">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[<span data-ttu-id="d6e00-213">**Commande. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="d6e00-213">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="d6e00-214">IU \_ \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="d6e00-214">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[<span data-ttu-id="d6e00-215">**Commande. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="d6e00-215">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="d6e00-216">IU \_ \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="d6e00-216">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 