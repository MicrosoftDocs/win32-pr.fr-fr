---
description: Montre comment utiliser le traitement vidéo DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Exemple de DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317974"
---
# <a name="dxva2_videoproc-sample"></a><span data-ttu-id="e8203-103">\_Exemple DXVA2 VideoProc</span><span class="sxs-lookup"><span data-stu-id="e8203-103">DXVA2\_VideoProc Sample</span></span>

<span data-ttu-id="e8203-104">Montre comment utiliser le [traitement vidéo DXVA](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="e8203-104">Shows how to use [DXVA Video Processing](dxva-video-processing.md).</span></span>

<span data-ttu-id="e8203-105">Cet exemple génère par programmation une vidéo avec un flux principal et un sous-flux.</span><span class="sxs-lookup"><span data-stu-id="e8203-105">This sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="e8203-106">Le flux principal affiche des barres de couleur SMPTE et le sous-flux est un rectangle semi-transparent.</span><span class="sxs-lookup"><span data-stu-id="e8203-106">The primary stream displays SMPTE color bars, and the substream is a semi-transparent rectangle.</span></span> <span data-ttu-id="e8203-107">La vidéo est ensuite traitée et affichée à l’aide d’un processeur vidéo DXVA.</span><span class="sxs-lookup"><span data-stu-id="e8203-107">The video is then processed and displayed using a DXVA video processor.</span></span> <span data-ttu-id="e8203-108">L’utilisateur peut modifier les valeurs alpha planaires, les rectangles source et de destination, les réglages de couleur et l’espace colorimétrique.</span><span class="sxs-lookup"><span data-stu-id="e8203-108">The user can change the planar alpha values, source and destination rectangles, color adjustments, and color space.</span></span>

![capture d’écran de l' \- exemple dxva2 videoproc](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="e8203-110">API illustrées</span><span class="sxs-lookup"><span data-stu-id="e8203-110">APIs Demonstrated</span></span>

<span data-ttu-id="e8203-111">Cet exemple illustre les interfaces DXVA suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8203-111">This sample demonstrates the following DXVA interfaces:</span></span>

-   [<span data-ttu-id="e8203-112">**IDirectXVideoProcessorService**</span><span class="sxs-lookup"><span data-stu-id="e8203-112">**IDirectXVideoProcessorService**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [<span data-ttu-id="e8203-113">**IDirectXVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="e8203-113">**IDirectXVideoProcessor**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a><span data-ttu-id="e8203-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e8203-114">Usage</span></span>

<span data-ttu-id="e8203-115">L' \_ exemple DXVA2 VideoProc génère une application Windows.</span><span class="sxs-lookup"><span data-stu-id="e8203-115">The DXVA2\_VideoProc sample builds a Windows application.</span></span>

<span data-ttu-id="e8203-116">Options de ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="e8203-116">Command line options:</span></span>



| <span data-ttu-id="e8203-117">Option</span><span class="sxs-lookup"><span data-stu-id="e8203-117">Option</span></span> | <span data-ttu-id="e8203-118">Description</span><span class="sxs-lookup"><span data-stu-id="e8203-118">Description</span></span>                                                                          |
|--------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8203-119">-hh</span><span class="sxs-lookup"><span data-stu-id="e8203-119">-hh</span></span>    | <span data-ttu-id="e8203-120">Force l’application à utiliser un périphérique Direct3D matériel et un périphérique DXVA matériel.</span><span class="sxs-lookup"><span data-stu-id="e8203-120">Forces the application to use a hardware Direct3D device and a hardware DXVA device.</span></span> |
| <span data-ttu-id="e8203-121">-HS</span><span class="sxs-lookup"><span data-stu-id="e8203-121">-hs</span></span>    | <span data-ttu-id="e8203-122">Force l’application à utiliser un périphérique Direct3D matériel et un périphérique DXVA logiciel.</span><span class="sxs-lookup"><span data-stu-id="e8203-122">Forces the application to use a hardware Direct3D device and a software DXVA device.</span></span> |
| <span data-ttu-id="e8203-123">-ss</span><span class="sxs-lookup"><span data-stu-id="e8203-123">-ss</span></span>    | <span data-ttu-id="e8203-124">Force l’application à utiliser un périphérique Direct3D logiciel et un périphérique DXVA logiciel.</span><span class="sxs-lookup"><span data-stu-id="e8203-124">Forces the application to use a software Direct3D device and a software DXVA device.</span></span> |



 

<span data-ttu-id="e8203-125">Commandes du clavier :</span><span class="sxs-lookup"><span data-stu-id="e8203-125">Keyboard commands:</span></span>



| <span data-ttu-id="e8203-126">Clé</span><span class="sxs-lookup"><span data-stu-id="e8203-126">Key</span></span>       | <span data-ttu-id="e8203-127">Description</span><span class="sxs-lookup"><span data-stu-id="e8203-127">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="e8203-128">Alt+Entrée</span><span class="sxs-lookup"><span data-stu-id="e8203-128">ALT+ENTER</span></span> | <span data-ttu-id="e8203-129">Basculer entre le mode fenêtre et le mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="e8203-129">Switch between windowed mode and full-screen mode.</span></span>      |
| <span data-ttu-id="e8203-130">F1-F8</span><span class="sxs-lookup"><span data-stu-id="e8203-130">F1–F8</span></span>     | <span data-ttu-id="e8203-131">Entrez l’un des modes répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e8203-131">Enter one of the modes shown in the following table.</span></span>    |
| <span data-ttu-id="e8203-132">FIN</span><span class="sxs-lookup"><span data-stu-id="e8203-132">END</span></span>       | <span data-ttu-id="e8203-133">Activez ou désactivez la journalisation du débogage des frames supprimés.</span><span class="sxs-lookup"><span data-stu-id="e8203-133">Enable or disable debugging logging for dropped frames.</span></span> |
| <span data-ttu-id="e8203-134">Origine</span><span class="sxs-lookup"><span data-stu-id="e8203-134">HOME</span></span>      | <span data-ttu-id="e8203-135">Réinitialisation d’un paramètre à sa valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="e8203-135">Reset a parameter to its initial value.</span></span>                 |



 

<span data-ttu-id="e8203-136">Chacune des touches de fonction F1 à F8 bascule vers un mode dans lequel les touches de direction peuvent être utilisées pour ajuster un paramètre de rendu particulier.</span><span class="sxs-lookup"><span data-stu-id="e8203-136">Each of the function keys F1 through F8 switches to a mode in which the arrow keys can be used to adjust a particular rendering parameter.</span></span> <span data-ttu-id="e8203-137">En outre, la couleur du sous-flux change.</span><span class="sxs-lookup"><span data-stu-id="e8203-137">In addition, the color of the substream changes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8203-138">Clé</span><span class="sxs-lookup"><span data-stu-id="e8203-138">Key</span></span></th>
<th><span data-ttu-id="e8203-139">Description</span><span class="sxs-lookup"><span data-stu-id="e8203-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8203-140">F1</span><span class="sxs-lookup"><span data-stu-id="e8203-140">F1</span></span></td>
<td><span data-ttu-id="e8203-141">Ajustez les valeurs alpha.</span><span class="sxs-lookup"><span data-stu-id="e8203-141">Adjust the alpha values.</span></span><br/>
<ul>
<li><span data-ttu-id="e8203-142">HAUT : Augmentez l’alpha planaire des deux flux.</span><span class="sxs-lookup"><span data-stu-id="e8203-142">UP: Increase the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="e8203-143">Baisse : diminuez l’alpha planaire des deux flux.</span><span class="sxs-lookup"><span data-stu-id="e8203-143">DOWN: Decrease the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="e8203-144">RIGHT : augmentez le pixel alpha du sous-flux.</span><span class="sxs-lookup"><span data-stu-id="e8203-144">RIGHT: Increase the pixel alpha of the substream.</span></span></li>
<li><span data-ttu-id="e8203-145">GAUCHE : diminuez le pixel alpha du sous-flux.</span><span class="sxs-lookup"><span data-stu-id="e8203-145">LEFT: Decrease the pixel alpha of the substream.</span></span></li>
</ul>
<span data-ttu-id="e8203-146">Couleur de sous-flux : blanc</span><span class="sxs-lookup"><span data-stu-id="e8203-146">Substream color: White</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8203-147">F2</span><span class="sxs-lookup"><span data-stu-id="e8203-147">F2</span></span></td>
<td><span data-ttu-id="e8203-148">Ajustez la zone source du flux principal (zoom).</span><span class="sxs-lookup"><span data-stu-id="e8203-148">Adjust the primary stream's source area (zoom).</span></span><br/>
<ul>
<li><span data-ttu-id="e8203-149">HAUT : augmentez verticalement (zoom avant).</span><span class="sxs-lookup"><span data-stu-id="e8203-149">UP: Increase vertically (zoom in).</span></span></li>
<li><span data-ttu-id="e8203-150">VERS le dessous : diminue verticalement (zoom arrière).</span><span class="sxs-lookup"><span data-stu-id="e8203-150">DOWN: Decrease vertically (zoom out).</span></span></li>
<li><span data-ttu-id="e8203-151">RIGHT : augmenter horizontalement (zoom avant).</span><span class="sxs-lookup"><span data-stu-id="e8203-151">RIGHT: Increase horizontally (zoom in).</span></span></li>
<li><span data-ttu-id="e8203-152">GAUCHE : diminue horizontalement (zoom arrière).</span><span class="sxs-lookup"><span data-stu-id="e8203-152">LEFT: Decrease horizontally (zoom out).</span></span></li>
</ul>
<span data-ttu-id="e8203-153">Couleur de sous-flux : rouge</span><span class="sxs-lookup"><span data-stu-id="e8203-153">Substream color: Red</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8203-154">F3</span><span class="sxs-lookup"><span data-stu-id="e8203-154">F3</span></span></td>
<td><span data-ttu-id="e8203-155">Déplacez la zone source du flux principal.</span><span class="sxs-lookup"><span data-stu-id="e8203-155">Move the primary stream's source area.</span></span><br/>
<ul>
<li><span data-ttu-id="e8203-156">HAUT : vers le haut.</span><span class="sxs-lookup"><span data-stu-id="e8203-156">UP: Move up.</span></span></li>
<li><span data-ttu-id="e8203-157">Descendre : descendre.</span><span class="sxs-lookup"><span data-stu-id="e8203-157">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="e8203-158">RIGHT : déplacer vers la droite.</span><span class="sxs-lookup"><span data-stu-id="e8203-158">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="e8203-159">GAUCHE : déplacer vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="e8203-159">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="e8203-160">Couleur de sous-flux : jaune</span><span class="sxs-lookup"><span data-stu-id="e8203-160">Substream color: Yellow</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8203-161">F4</span><span class="sxs-lookup"><span data-stu-id="e8203-161">F4</span></span></td>
<td><span data-ttu-id="e8203-162">Ajustez la zone de destination du flux principal.</span><span class="sxs-lookup"><span data-stu-id="e8203-162">Adjust the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="e8203-163">HAUT : augmente verticalement.</span><span class="sxs-lookup"><span data-stu-id="e8203-163">UP: Increase vertically.</span></span></li>
<li><span data-ttu-id="e8203-164">VERS le dessous : diminue verticalement.</span><span class="sxs-lookup"><span data-stu-id="e8203-164">DOWN: Decrease vertically.</span></span></li>
<li><span data-ttu-id="e8203-165">RIGHT : augmenter horizontalement.</span><span class="sxs-lookup"><span data-stu-id="e8203-165">RIGHT: Increase horizontally.</span></span></li>
<li><span data-ttu-id="e8203-166">GAUCHE : diminue horizontalement.</span><span class="sxs-lookup"><span data-stu-id="e8203-166">LEFT: Decrease horizontally.</span></span></li>
</ul>
<span data-ttu-id="e8203-167">Couleur de sous-flux : vert</span><span class="sxs-lookup"><span data-stu-id="e8203-167">Substream color: Green</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8203-168">F5</span><span class="sxs-lookup"><span data-stu-id="e8203-168">F5</span></span></td>
<td><span data-ttu-id="e8203-169">Déplacez la zone de destination du flux principal.</span><span class="sxs-lookup"><span data-stu-id="e8203-169">Move the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="e8203-170">HAUT : vers le haut.</span><span class="sxs-lookup"><span data-stu-id="e8203-170">UP: Move up.</span></span></li>
<li><span data-ttu-id="e8203-171">Descendre : descendre.</span><span class="sxs-lookup"><span data-stu-id="e8203-171">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="e8203-172">RIGHT : déplacer vers la droite.</span><span class="sxs-lookup"><span data-stu-id="e8203-172">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="e8203-173">GAUCHE : déplacer vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="e8203-173">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="e8203-174">Couleur de sous-flux : cyan</span><span class="sxs-lookup"><span data-stu-id="e8203-174">Substream color: Cyan</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8203-175">F6</span><span class="sxs-lookup"><span data-stu-id="e8203-175">F6</span></span></td>
<td><span data-ttu-id="e8203-176">Modifiez l’espace colorimétrique ou couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e8203-176">Change background color or color space.</span></span><br/>
<ul>
<li><span data-ttu-id="e8203-177">Haut, vers le haut : parcourir les espaces de couleurs.</span><span class="sxs-lookup"><span data-stu-id="e8203-177">UP, DOWN: Cycle through color spaces.</span></span></li>
<li><span data-ttu-id="e8203-178">DROITE, gauche : parcourir les couleurs d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e8203-178">RIGHT, LEFT: Cycle through background colors.</span></span></li>
</ul>
<span data-ttu-id="e8203-179">Couleur de sous-flux : bleue</span><span class="sxs-lookup"><span data-stu-id="e8203-179">Substream color: Blue</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8203-180">F7</span><span class="sxs-lookup"><span data-stu-id="e8203-180">F7</span></span></td>
<td><span data-ttu-id="e8203-181">Ajustez la luminosité et le contraste.</span><span class="sxs-lookup"><span data-stu-id="e8203-181">Adjust brightness and contrast.</span></span><br/>
<ul>
<li><span data-ttu-id="e8203-182">HAUT : augmentez la luminosité.</span><span class="sxs-lookup"><span data-stu-id="e8203-182">UP: Increase brightness.</span></span></li>
<li><span data-ttu-id="e8203-183">Baisse : réduire la luminosité.</span><span class="sxs-lookup"><span data-stu-id="e8203-183">DOWN: Decrease brightness.</span></span></li>
<li><span data-ttu-id="e8203-184">RIGHT : augmenter le contraste.</span><span class="sxs-lookup"><span data-stu-id="e8203-184">RIGHT: Increase contrast.</span></span></li>
<li><span data-ttu-id="e8203-185">GAUCHE : diminuer le contraste.</span><span class="sxs-lookup"><span data-stu-id="e8203-185">LEFT: Decrease contrast.</span></span></li>
</ul>
<span data-ttu-id="e8203-186">Couleur de sous-flux : magenta</span><span class="sxs-lookup"><span data-stu-id="e8203-186">Substream color: Magenta</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8203-187">F8</span><span class="sxs-lookup"><span data-stu-id="e8203-187">F8</span></span></td>
<td><span data-ttu-id="e8203-188">Ajustez la teinte et la saturation.</span><span class="sxs-lookup"><span data-stu-id="e8203-188">Adjust hue and saturation.</span></span><br/>
<ul>
<li><span data-ttu-id="e8203-189">HAUT : augmentez la teinte.</span><span class="sxs-lookup"><span data-stu-id="e8203-189">UP: Increase hue.</span></span></li>
<li><span data-ttu-id="e8203-190">Baisse : diminuer la teinte.</span><span class="sxs-lookup"><span data-stu-id="e8203-190">DOWN: Decrease hue.</span></span></li>
<li><span data-ttu-id="e8203-191">RIGHT : augmenter la saturation.</span><span class="sxs-lookup"><span data-stu-id="e8203-191">RIGHT: Increase saturation.</span></span></li>
<li><span data-ttu-id="e8203-192">GAUCHE : diminuer la saturation.</span><span class="sxs-lookup"><span data-stu-id="e8203-192">LEFT: Decrease saturation.</span></span></li>
</ul>
<span data-ttu-id="e8203-193">Couleur de sous-flux : noir</span><span class="sxs-lookup"><span data-stu-id="e8203-193">Substream color: Black</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e8203-194">Dans chaque mode, l’appui sur la touche origine rétablit les valeurs initiales des paramètres de ce mode.</span><span class="sxs-lookup"><span data-stu-id="e8203-194">In each mode, pressing the HOME key resets the parameters for that mode to their initial values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8203-195">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8203-195">Requirements</span></span>



| <span data-ttu-id="e8203-196">Produit</span><span class="sxs-lookup"><span data-stu-id="e8203-196">Product</span></span>                                                        | <span data-ttu-id="e8203-197">Version</span><span class="sxs-lookup"><span data-stu-id="e8203-197">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="e8203-198">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="e8203-198">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="e8203-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8203-199">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e8203-200">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e8203-200">Downloading the Sample</span></span>

<span data-ttu-id="e8203-201">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span><span class="sxs-lookup"><span data-stu-id="e8203-201">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8203-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8203-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8203-203">Accélération vidéo DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="e8203-203">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="e8203-204">Traitement vidéo DXVA</span><span class="sxs-lookup"><span data-stu-id="e8203-204">DXVA Video Processing</span></span>](dxva-video-processing.md)
</dt> <dt>

[<span data-ttu-id="e8203-205">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8203-205">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




