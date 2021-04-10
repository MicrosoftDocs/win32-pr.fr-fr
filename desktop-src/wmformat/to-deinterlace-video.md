---
title: Pour désentrelacer une vidéo
description: Pour désentrelacer une vidéo
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK, vidéo désentrelacée
- Windows Media Format SDK, inversement Telecine
- Kit de développement logiciel (SDK) Windows Media format, télécinéma
- ASF (Advanced Systems Format), vidéo désentrelacée
- ASF (format des systèmes avancés), vidéo désentrelacée
- ASF (Advanced Systems Format), inversement
- ASF (format avancé des systèmes), inversement
- ASF (Advanced Systems Format), télécinéma
- ASF (format avancé des systèmes), télécinéma
- vidéo désentrelacée
- inverser Telecine, à propos de
- télécinéma, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030818"
---
# <a name="to-deinterlace-video"></a><span data-ttu-id="e5b5a-115">Pour désentrelacer une vidéo</span><span class="sxs-lookup"><span data-stu-id="e5b5a-115">To Deinterlace Video</span></span>

<span data-ttu-id="e5b5a-116">Certaines sources de vidéo, telles que les cartes de capture vidéo, fournissent des données vidéo pour l’affichage entrelacé.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-116">Some sources of video, such as video capture cards, deliver video data for interlaced display.</span></span> <span data-ttu-id="e5b5a-117">Chaque image de vidéo entrelacée est composée de deux champs.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-117">Each frame of interlaced video is made up of two fields.</span></span> <span data-ttu-id="e5b5a-118">Le champ du haut contient la première ligne de vidéo et chaque ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-118">The top field contains the first line of video and every other line thereafter.</span></span> <span data-ttu-id="e5b5a-119">Le champ du bas contient la deuxième ligne de vidéo et chaque ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-119">The bottom field contains the second line of video and every other line thereafter.</span></span> <span data-ttu-id="e5b5a-120">Par conséquent, un champ contient toutes les lignes paires numérotées et l’autre contient toutes les lignes impaires.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-120">So one field contains all of the even numbered lines and the other contains all of the odd numbered lines.</span></span> <span data-ttu-id="e5b5a-121">Les champs qui composent un cadre représentent des temps de présentation légèrement différents afin que, lorsqu’ils sont entrelacés, ils ne forment pas une image statique.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-121">The fields that make up a frame represent slightly different presentation times so that, when interleaved, they do not form a static image.</span></span>

<span data-ttu-id="e5b5a-122">Lorsque vous souhaitez afficher une vidéo sur un moniteur d’ordinateur, chaque image de la vidéo doit être affichée sous la forme d’une image (cette méthode d’affichage de la vidéo d’une image complète à la fois est appelée vidéo *progressive* .) Si vous affichez des vidéos entrelacées de façon progressive, les frames peuvent ne pas s’afficher correctement, en raison de la différence de temps entre les deux champs.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-122">When you want to display video on a computer monitor, each frame of the video should be displayed as one image (this method of displaying video one whole frame at a time is called *progressive* video.) If you display interlaced video progressively, the frames may not look right, because of the time difference between the two fields.</span></span> <span data-ttu-id="e5b5a-123">Le codec Windows Media Video et le codec de profil avancé Windows Media Video prennent tous deux en charge une fonctionnalité de prétraitement qui convertit le contenu entrelacé en images progressives.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-123">The Windows Media Video codec and the Windows Media Video Advanced Profile codec both support a preprocessing feature that converts interlaced content into progressive frames.</span></span>

<span data-ttu-id="e5b5a-124">Pour que le codec désentrelace la vidéo d’entrée, appelez la méthode [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) .</span><span class="sxs-lookup"><span data-stu-id="e5b5a-124">To have the codec deinterlace input video, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method.</span></span> <span data-ttu-id="e5b5a-125">Le paramètre à utiliser est g \_ wszDeinterlaceMode.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-125">The setting to use is g\_wszDeinterlaceMode.</span></span> <span data-ttu-id="e5b5a-126">Définissez le mode de désentrelacement sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-126">Set the deinterlacing mode to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5b5a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5b5a-127">Value</span></span></th>
<th><span data-ttu-id="e5b5a-128">Description</span><span class="sxs-lookup"><span data-stu-id="e5b5a-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5b5a-129">WM_DM_NOTINTERLACED</span><span class="sxs-lookup"><span data-stu-id="e5b5a-129">WM_DM_NOTINTERLACED</span></span></td>
<td><span data-ttu-id="e5b5a-130">L’entrée est progressive.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-130">Input is progressive.</span></span> <span data-ttu-id="e5b5a-131">Utilisez ce paramètre pour arrêter l’entrelacement lorsque vous avez précédemment défini le mode de désentrelacement sur une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-131">Use this setting to stop deinterlacing when you have previously set the deinterlacing mode to another value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5b5a-132">WM_DM_DEINTERLACE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="e5b5a-132">WM_DM_DEINTERLACE_NORMAL</span></span></td>
<td><span data-ttu-id="e5b5a-133">Sélectionnez ce mode pour fusionner les champs pairs et impairs d’un cadre entrelacé (à l’aide d’un mécanisme de compensation de mouvement). Avantageuse</span><span class="sxs-lookup"><span data-stu-id="e5b5a-133">Select this mode to blend the even and odd fields of an interlaced frame (using a motion compensation mechanism).Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="e5b5a-134">Les artefacts entrelacés de l’affichage progressif sont considérablement réduits.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-134">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
<li><span data-ttu-id="e5b5a-135">Le codec Windows Media Video produit une vidéo compressée de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-135">The Windows Media Video codec produces higher quality compressed video.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5b5a-136">WM_DM_DEINTERLACE_HALFSIZE</span><span class="sxs-lookup"><span data-stu-id="e5b5a-136">WM_DM_DEINTERLACE_HALFSIZE</span></span></td>
<td><span data-ttu-id="e5b5a-137">Sélectionnez ce mode lorsque la résolution de sortie est inférieure ou égale à la résolution d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-137">Select this mode when the output resolution is half, or less, of the input resolution.</span></span> <span data-ttu-id="e5b5a-138">Par exemple, utilisez ce mode lorsque la résolution vidéo d’entrée est de 640 x 480 pixels et que la résolution vidéo de sortie est de 320 x 240 pixels. Avantageuse</span><span class="sxs-lookup"><span data-stu-id="e5b5a-138">For example, use this mode when the input video resolution is 640 x 480 pixels and the output video resolution is 320 x 240 pixels.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="e5b5a-139">Les artefacts entrelacés de l’affichage progressif sont considérablement réduits.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-139">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5b5a-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="e5b5a-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="e5b5a-141">Sélectionnez ce mode lorsque la résolution de sortie est inférieure ou égale à la moitié de la résolution d’entrée et que la <a href="wmformat-glossary.md"><em>fréquence d’images</em></a> de sortie est deux fois supérieure.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-141">Select this mode when the output resolution is half, or less, of the input resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="e5b5a-142">Par exemple, utilisez ce mode lorsque la résolution vidéo d’entrée est de 640 x 480 pixels à 30 images entrelacées/s et que la résolution vidéo en sortie est de 320 x 240 pixels à 60 images/s. Avantageuse</span><span class="sxs-lookup"><span data-stu-id="e5b5a-142">For example, use this mode when the input video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="e5b5a-143">Cela produit des images progressives de haute qualité, car chaque champ est converti en cadre et il n’est donc pas nécessaire de fusionner les informations.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-143">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="e5b5a-144">Le mouvement complet des champs entrelacés est capturé.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-144">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5b5a-145">WM_DM_DEINTERLACE_INVERSETELECINE</span><span class="sxs-lookup"><span data-stu-id="e5b5a-145">WM_DM_DEINTERLACE_INVERSETELECINE</span></span></td>
<td><span data-ttu-id="e5b5a-146">Sélectionnez ce mode pour convertir la vidéo télécinéma 30 images/s en 24 images/s du film d’origine. Avantageuse</span><span class="sxs-lookup"><span data-stu-id="e5b5a-146">Select this mode to convert telecined 30 frames/sec video into the 24 frames/sec of the original film.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="e5b5a-147">La qualité de compression s’améliore de manière significative, car seules 24 images/s au lieu de 30 images/s doivent être encodées.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-147">The compression quality improves significantly because only 24 frames/sec instead of 30 frames/sec need to be encoded.</span></span></li>
<li><span data-ttu-id="e5b5a-148">Étant donné que le résultat est progressif, la même compression et l’affichage des avantages de l’entrelacement sont réalisés.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-148">Because the result is progressive, the same compression and display benefits of deinterlacing are realized.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5b5a-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="e5b5a-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="e5b5a-150">Sélectionnez ce mode lorsque la résolution de sortie verticale est inférieure ou égale à la moitié de la résolution verticale d’entrée et que la <a href="wmformat-glossary.md"><em>fréquence d’images</em></a> de sortie est deux fois supérieure.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-150">Select this mode when the vertical output resolution is half, or less, of the input vertical resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="e5b5a-151">Par exemple, la résolution vidéo verticale d’entrée est de 640 x 480 pixels à 30 images entrelacées/s et la résolution vidéo verticale de sortie est de 320 x 240 pixels à 60 images/s. Avantageuse</span><span class="sxs-lookup"><span data-stu-id="e5b5a-151">For example, the input vertical video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output vertical video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="e5b5a-152">Cela produit des images progressives de haute qualité, car chaque champ est converti en cadre et il n’est donc pas nécessaire de fusionner les informations.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-152">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="e5b5a-153">Le mouvement complet des champs entrelacés est capturé.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-153">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e5b5a-154">Pour le contenu mixte, définissez le mode de désentrelacement en fonction des besoins avant de passer des exemples d’un nouveau type.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-154">For mixed content, set the deinterlacing mode as needed before passing samples of a new type.</span></span> <span data-ttu-id="e5b5a-155">Par exemple, pour démarrer l’encodage avec une entrée progressive, vous n’avez pas besoin de définir de mode de désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-155">For example, to start encoding with progressive input, you don't need to set any deinterlacing mode.</span></span> <span data-ttu-id="e5b5a-156">Si certains exemples requièrent alors une désentrelacement normal, vous devez définir le mode de désentrelacement sur WM \_ DM \_ subentrelacer \_ normal.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-156">If some samples then require normal deinterlacing, you must set the deinterlacing mode to WM\_DM\_DEINTERLACE\_NORMAL.</span></span> <span data-ttu-id="e5b5a-157">Pour traiter ensuite d’autres exemples progressifs, vous devez définir le mode de désentrelacement sur WM \_ DM \_ NOTINTERLACED.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-157">To then process additional progressive samples you must set the deinterlacing mode to WM\_DM\_NOTINTERLACED.</span></span>

## <a name="inverse-telecine-settings"></a><span data-ttu-id="e5b5a-158">Paramètres de télécinéma inverse</span><span class="sxs-lookup"><span data-stu-id="e5b5a-158">Inverse Telecine Settings</span></span>

<span data-ttu-id="e5b5a-159">Pour obtenir une description de télécinéma inverse, consultez [pour utiliser l’inverse de télécinéma](to-use-inverse-telecine.md).</span><span class="sxs-lookup"><span data-stu-id="e5b5a-159">For a description of inverse telecine, see [To Use Inverse Telecine](to-use-inverse-telecine.md).</span></span>

<span data-ttu-id="e5b5a-160">Si vous définissez le mode de désentrelacement sur WM \_ DM \_ désentrelacer \_ INVERSETELECINE, vous pouvez spécifier le modèle de télécinéma de la première trame d’entrée en appelant [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="e5b5a-160">If you set the deinterlacing mode to WM\_DM\_DEINTERLACE\_INVERSETELECINE, you can specify the telecine pattern of the first input frame by calling the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="e5b5a-161">Le paramètre à utiliser est g \_ wszInitialPatternForInverseTelecine.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-161">The setting to use is g\_wszInitialPatternForInverseTelecine.</span></span> <span data-ttu-id="e5b5a-162">Définissez le modèle initial sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-162">Set the initial pattern to one of the following values.</span></span>



| <span data-ttu-id="e5b5a-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5b5a-163">Value</span></span>                                              | <span data-ttu-id="e5b5a-164">Description</span><span class="sxs-lookup"><span data-stu-id="e5b5a-164">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b5a-165">WM \_ DM \_ \_ désactive le \_ mode de cohérence \_</span><span class="sxs-lookup"><span data-stu-id="e5b5a-165">WM\_DM\_IT\_DISABLE\_COHERENT\_MODE</span></span>                | <span data-ttu-id="e5b5a-166">Spécifie que le média d’entrée est passé par le processus de télécinéma, mais que les images ne sont plus dans un modèle prévisible.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-166">Specifies that the input media has gone through the telecine process but that the frames are no longer in a predictable pattern.</span></span> <span data-ttu-id="e5b5a-167">Cela indique généralement que le support a été modifié après le traitement de télécinéma.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-167">This usually indicates that the media was edited after the telecine processing.</span></span> <span data-ttu-id="e5b5a-168">Lorsque vous utilisez ce paramètre, le codec tente de reconstruire les frames d’origine de manière autonome.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-168">When you use this setting, the codec attempts to reconstruct the original frames on its own.</span></span> |
| <span data-ttu-id="e5b5a-169">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ AA en \_ haut</span><span class="sxs-lookup"><span data-stu-id="e5b5a-169">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_TOP</span></span>    | <span data-ttu-id="e5b5a-170">Spécifie que le champ supérieur du cadre AA est le premier échantillon.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-170">Specifies that the top field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="e5b5a-171">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ BB \_ Top</span><span class="sxs-lookup"><span data-stu-id="e5b5a-171">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_TOP</span></span>    | <span data-ttu-id="e5b5a-172">Spécifie que le champ supérieur du cadre BB est le premier échantillon.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-172">Specifies that the top field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="e5b5a-173">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ BC \_ Top</span><span class="sxs-lookup"><span data-stu-id="e5b5a-173">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_TOP</span></span>    | <span data-ttu-id="e5b5a-174">Spécifie que le champ supérieur de la trame BC est le premier échantillon.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-174">Specifies that the top field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="e5b5a-175">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est le \_ CD \_ haut</span><span class="sxs-lookup"><span data-stu-id="e5b5a-175">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_TOP</span></span>    | <span data-ttu-id="e5b5a-176">Spécifie que le champ supérieur du cadre CD est le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-176">Specifies that the top field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="e5b5a-177">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ DD en \_ haut</span><span class="sxs-lookup"><span data-stu-id="e5b5a-177">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_TOP</span></span>    | <span data-ttu-id="e5b5a-178">Spécifie que le champ supérieur du frame DD est le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-178">Specifies that the top field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="e5b5a-179">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ AA en \_ bas</span><span class="sxs-lookup"><span data-stu-id="e5b5a-179">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_BOTTOM</span></span> | <span data-ttu-id="e5b5a-180">Spécifie que le champ inférieur du cadre AA est le premier échantillon.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-180">Specifies that the bottom field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="e5b5a-181">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ BB en \_ bas</span><span class="sxs-lookup"><span data-stu-id="e5b5a-181">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_BOTTOM</span></span> | <span data-ttu-id="e5b5a-182">Spécifie que le champ inférieur du cadre BB est le premier échantillon.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-182">Specifies that the bottom field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="e5b5a-183">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ BC \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="e5b5a-183">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_BOTTOM</span></span> | <span data-ttu-id="e5b5a-184">Spécifie que le champ inférieur de la trame BC est le premier échantillon.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-184">Specifies that the bottom field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="e5b5a-185">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est le \_ CD- \_ bas</span><span class="sxs-lookup"><span data-stu-id="e5b5a-185">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_BOTTOM</span></span> | <span data-ttu-id="e5b5a-186">Spécifie que le champ inférieur du cadre CD est le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-186">Specifies that the bottom field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="e5b5a-187">WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ DD en \_ bas</span><span class="sxs-lookup"><span data-stu-id="e5b5a-187">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_BOTTOM</span></span> | <span data-ttu-id="e5b5a-188">Spécifie que le champ inférieur du frame DD est le premier exemple.</span><span class="sxs-lookup"><span data-stu-id="e5b5a-188">Specifies that the bottom field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="e5b5a-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5b5a-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5b5a-190">**Rubriques avancées**</span><span class="sxs-lookup"><span data-stu-id="e5b5a-190">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





