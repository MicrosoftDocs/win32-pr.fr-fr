---
title: Pour utiliser la vidéo entrelacée
description: Pour utiliser la vidéo entrelacée
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media Format SDK, vidéo entrelacée
- Windows Media Format SDK, encodage vidéo entrelacé
- Windows Media Format SDK, encodage vidéo entrelacée
- Windows Media Format SDK, décodage vidéo entrelacée
- Windows Media Format SDK, ordre des champs
- ASF (Advanced Systems Format), vidéo entrelacée
- ASF (format des systèmes avancés), vidéo entrelacée
- ASF (Advanced Systems Format), encodage vidéo entrelacé
- ASF (format des systèmes avancés), encodage vidéo entrelacé
- ASF (Advanced Systems Format), encodage vidéo entrelacée
- ASF (format avancé des systèmes), encodage d’une vidéo entrelacée
- ASF (Advanced Systems Format), décodage de vidéo entrelacée
- ASF (format de systèmes avancés), décodage de vidéo entrelacée
- ASF (Advanced Systems Format), ordre des champs
- ASF (format des systèmes avancés), ordre des champs
- vidéo entrelacée, à propos de
- vidéo entrelacée, encodage
- vidéo entrelacée, décodage
- vidéo entrelacée, ordre des champs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841901"
---
# <a name="to-use-interlaced-video"></a><span data-ttu-id="19a2b-122">Pour utiliser la vidéo entrelacée</span><span class="sxs-lookup"><span data-stu-id="19a2b-122">To Use Interlaced Video</span></span>

<span data-ttu-id="19a2b-123">Il existe deux types de codage vidéo de base : progressif et entrelacé.</span><span class="sxs-lookup"><span data-stu-id="19a2b-123">There are two basic types of video encoding: progressive and interlaced.</span></span> <span data-ttu-id="19a2b-124">Dans l’encodage progressif, chaque frame est une représentation encodée d’un cadre de vidéo.</span><span class="sxs-lookup"><span data-stu-id="19a2b-124">In progressive encoding, each frame is an encoded representation of one frame of video.</span></span> <span data-ttu-id="19a2b-125">Dans l’encodage entrelacé, chaque frame est une représentation encodée de toutes les lignes paires de pixels dans la vidéo, ou de toutes les lignes impaires.</span><span class="sxs-lookup"><span data-stu-id="19a2b-125">In interlaced encoding, each frame is an encoded representation of either all of the even rows of pixels in the video, or all of the odd rows.</span></span> <span data-ttu-id="19a2b-126">Chaque trame entrelacée étant appelée un *champ*, il y a des champs impairs et même des champs.</span><span class="sxs-lookup"><span data-stu-id="19a2b-126">Each interlaced frame is called a *field*, so there are odd fields and even fields.</span></span> <span data-ttu-id="19a2b-127">Un affichage entrelacé (comme une télévision) restitue les champs un par un, en alternant les champs.</span><span class="sxs-lookup"><span data-stu-id="19a2b-127">An interlaced display (like a television) renders the fields one at a time, alternating fields.</span></span> <span data-ttu-id="19a2b-128">Un affichage progressif affiche tous les frames à la fois.</span><span class="sxs-lookup"><span data-stu-id="19a2b-128">A progressive display renders frames all at once.</span></span>

<span data-ttu-id="19a2b-129">Le codec de profil avancé Windows Media Video 9 assure la prise en charge de la gestion de l’entrelacement dans les flux compressés.</span><span class="sxs-lookup"><span data-stu-id="19a2b-129">The Windows Media Video 9 Advanced Profile codec provides support for maintaining interlacing in compressed streams.</span></span>

## <a name="when-to-use-interlaced-video"></a><span data-ttu-id="19a2b-130">Quand utiliser la vidéo entrelacée</span><span class="sxs-lookup"><span data-stu-id="19a2b-130">When to Use Interlaced Video</span></span>

<span data-ttu-id="19a2b-131">L’encodage d’une vidéo entrelacée est utile uniquement lorsque le contenu est affiché sur un appareil entrelacé.</span><span class="sxs-lookup"><span data-stu-id="19a2b-131">Encoding interlaced video is useful only when the content is displayed on an interlaced device.</span></span> <span data-ttu-id="19a2b-132">Le contenu destiné à être affiché sur une télévision (par le biais d’un boîtier décodeur ou d’un autre périphérique) doit peut-être être entrelacé.</span><span class="sxs-lookup"><span data-stu-id="19a2b-132">Content that is intended to be viewed on a television (through a set-top box or other device) may need to be interlaced.</span></span> <span data-ttu-id="19a2b-133">Le contenu destiné à être affiché exclusivement sur un écran d’ordinateur ne doit pas être encodé comme entrelacé.</span><span class="sxs-lookup"><span data-stu-id="19a2b-133">Content that is intended to be viewed exclusively on a computer display should not be encoded as interlaced.</span></span>

<span data-ttu-id="19a2b-134">Pour encoder une vidéo entrelacée comme vidéo progressive, vous devez configurer les paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="19a2b-134">To encode interlaced video as progressive video, you must configure input settings.</span></span> <span data-ttu-id="19a2b-135">Pour plus d’informations, consultez [pour libérer de la vidéo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="19a2b-135">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>

## <a name="field-order"></a><span data-ttu-id="19a2b-136">Ordre des champs</span><span class="sxs-lookup"><span data-stu-id="19a2b-136">Field Order</span></span>

<span data-ttu-id="19a2b-137">La plupart des sources de vidéo entrelacées, telles que les cartes de capture vidéo, fournissent des exemples de vidéos qui incluent les deux champs entrelacés les uns avec les autres.</span><span class="sxs-lookup"><span data-stu-id="19a2b-137">Most sources of interlaced video, such as video capture cards, deliver video samples that include both fields interleaved with each other.</span></span> <span data-ttu-id="19a2b-138">Le résultat ressemble à une image complète de la vidéo, sauf que les lignes paires et impaires sont décalées légèrement dans le temps.</span><span class="sxs-lookup"><span data-stu-id="19a2b-138">The result is like a complete frame of video, except that the odd and even lines are shifted slightly in time.</span></span> <span data-ttu-id="19a2b-139">Il n’existe pas de norme universelle quant au champ dans lequel l’exemple de vidéo entrelacée se produit pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="19a2b-139">There is no universal standard as to which field in the interleaved video sample occurs first in time.</span></span>

<span data-ttu-id="19a2b-140">Vous devez permettre aux utilisateurs de spécifier l’ordre des champs lors du passage d’échantillons entrelacés à votre application.</span><span class="sxs-lookup"><span data-stu-id="19a2b-140">You should enable users to specify field order when passing interlaced samples to your application.</span></span>

## <a name="encoding-interlaced-video"></a><span data-ttu-id="19a2b-141">Encodage d’une vidéo entrelacée</span><span class="sxs-lookup"><span data-stu-id="19a2b-141">Encoding Interlaced Video</span></span>

<span data-ttu-id="19a2b-142">Pour utiliser l’encodage entrelacé, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="19a2b-142">To use interlaced encoding, perform the following steps:</span></span>

1.  <span data-ttu-id="19a2b-143">Configurez le flux vidéo dans le profil pour utiliser l’extension d’unité de données de type de contenu en appelant la méthode [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="19a2b-143">Configure the video stream in the profile to use the content type data unit extension by calling the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method.</span></span> <span data-ttu-id="19a2b-144">L’exemple de GUID d’extension pour l’extension de type de contenu est WM \_ SampleExtensionsGUID \_ ContentType.</span><span class="sxs-lookup"><span data-stu-id="19a2b-144">The sample extension GUID for the content type extension is WM\_SampleExtensionsGUID\_ContentType.</span></span>
2.  <span data-ttu-id="19a2b-145">Définissez le flux dans le profil et configurez l’enregistreur avec le profil comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="19a2b-145">Set the stream in the profile and configure the writer with the profile as normal.</span></span>
3.  <span data-ttu-id="19a2b-146">Avant de transmettre des échantillons entrelacés au writer, appelez la méthode [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) pour définir le \_ paramètre d’entrée g wszInterlacedCoding sur **true**.</span><span class="sxs-lookup"><span data-stu-id="19a2b-146">Before passing interlaced samples to the writer, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method to set the g\_wszInterlacedCoding input setting to **TRUE**.</span></span>
4.  <span data-ttu-id="19a2b-147">Pour chaque échantillon entrelacé que vous transmettez au writer, appelez la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) pour définir le type de contenu.</span><span class="sxs-lookup"><span data-stu-id="19a2b-147">For every interlaced sample that you pass to the writer, call the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the content type.</span></span> <span data-ttu-id="19a2b-148">Les valeurs de type de contenu sont des combinaisons des indicateurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="19a2b-148">Content type values are combinations of the flags in the following table.</span></span>



| <span data-ttu-id="19a2b-149">Indicateur</span><span class="sxs-lookup"><span data-stu-id="19a2b-149">Flag</span></span>                         | <span data-ttu-id="19a2b-150">Description</span><span class="sxs-lookup"><span data-stu-id="19a2b-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a2b-151">WM \_ CT \_ entrelacé</span><span class="sxs-lookup"><span data-stu-id="19a2b-151">WM\_CT\_INTERLACED</span></span>           | <span data-ttu-id="19a2b-152">Définissez toujours cet indicateur lors de l’encodage du contenu entrelacé.</span><span class="sxs-lookup"><span data-stu-id="19a2b-152">Always set this flag when encoding interlaced content.</span></span> <span data-ttu-id="19a2b-153">Si vous utilisez cet indicateur sans avoir à définir un indicateur d’ordre de champ (le champ WM WM en \_ \_ bas \_ \_ ou \_ \_ le champ supérieur WM CT en \_ \_ premier), le codec suppose que le champ supérieur est tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="19a2b-153">If you use this flag without setting a field-order flag (WM\_CT\_BOTTOM\_FIELD\_FIRST or WM\_CT\_TOP\_FIELD\_FIRST) the codec will assume that the top field is first.</span></span> <span data-ttu-id="19a2b-154">Si le codec utilise un mauvais ordre des champs, il ne doit pas y avoir d’impact sur la qualité de l’image, mais l’efficacité de l’encodage sera affectée.</span><span class="sxs-lookup"><span data-stu-id="19a2b-154">If the codec uses the wrong field order, there should be no impact on image quality, but the encoding efficiency will be affected.</span></span> |
| <span data-ttu-id="19a2b-155">\_champ inférieur WM CT en \_ \_ \_ premier</span><span class="sxs-lookup"><span data-stu-id="19a2b-155">WM\_CT\_BOTTOM\_FIELD\_FIRST</span></span> | <span data-ttu-id="19a2b-156">Lorsqu’il est combiné avec l' \_ indicateur WM CT \_ entrelacé, cet indicateur indique que le champ du bas (le champ commençant par la deuxième ligne de l’exemple) se produit en premier dans le temps.</span><span class="sxs-lookup"><span data-stu-id="19a2b-156">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the bottom field (the field starting with the second line in the sample) occurs first in time.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="19a2b-157">\_champ supérieur WM CT en \_ \_ \_ premier</span><span class="sxs-lookup"><span data-stu-id="19a2b-157">WM\_CT\_TOP\_FIELD\_FIRST</span></span>    | <span data-ttu-id="19a2b-158">Lorsqu’il est combiné avec l' \_ indicateur WM CT \_ entrelacé, cet indicateur indique que le champ supérieur (le champ commençant par la première ligne de l’exemple) se produit en premier dans le temps.</span><span class="sxs-lookup"><span data-stu-id="19a2b-158">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the top field (the field starting with the first line in the sample) occurs first in time.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="19a2b-159">WM \_ CT- \_ répéter le \_ premier \_ champ</span><span class="sxs-lookup"><span data-stu-id="19a2b-159">WM\_CT\_REPEAT\_FIRST\_FIELD</span></span> | <span data-ttu-id="19a2b-160">Indique que le premier champ de l’échantillon doit être répété lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="19a2b-160">Indicates that the first field in the sample should be repeated on playback.</span></span> <span data-ttu-id="19a2b-161">Cet indicateur est utilisé pour la vidéo qui a été créée à partir d’un film par le processus de télécinéma. Si aucun indicateur d’ordre de champ n’est défini conjointement avec cet indicateur, le champ supérieur est supposé se produire en premier dans le temps.</span><span class="sxs-lookup"><span data-stu-id="19a2b-161">This flag is used for video that has created from film by the telecine process.If no field-order flag is set in conjunction with this flag, the top field is assumed to occur first in time.</span></span><br/>                                                                             |



 

> [!Note]  
> <span data-ttu-id="19a2b-162">Si l' \_ \_ indicateur de l’entrelacement WM CT n’est pas défini, l’échantillon est supposé contenir une image vidéo progressive.</span><span class="sxs-lookup"><span data-stu-id="19a2b-162">If the WM\_CT\_INTERLACED flag is not set, the sample is assumed to contain a progressive video frame.</span></span>

 

## <a name="decoding-interlaced-video"></a><span data-ttu-id="19a2b-163">Décodage d’une vidéo entrelacée</span><span class="sxs-lookup"><span data-stu-id="19a2b-163">Decoding Interlaced Video</span></span>

<span data-ttu-id="19a2b-164">Lors du décodage d’une vidéo entrelacée, vous devez affecter la \_ **valeur true** au paramètre g wszAllowInterlacedOutput à l’aide de la méthode [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="19a2b-164">When decoding interlaced video, you must set the g\_wszAllowInterlacedOutput setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="19a2b-165">Dans le cas contraire, le codec fournira des trames progressives.</span><span class="sxs-lookup"><span data-stu-id="19a2b-165">Otherwise the codec will deliver progressive frames.</span></span>

<span data-ttu-id="19a2b-166">L’extension d’unité de données de type de contenu est conservée dans les exemples de sortie.</span><span class="sxs-lookup"><span data-stu-id="19a2b-166">The content type data unit extension is maintained on the output samples.</span></span> <span data-ttu-id="19a2b-167">Vous devez passer l’orientation du champ à l’appareil de rendu pour garantir une lecture correcte.</span><span class="sxs-lookup"><span data-stu-id="19a2b-167">You should pass the field orientation to the rendering device to ensure proper playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19a2b-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19a2b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a2b-169">**Rubriques avancées**</span><span class="sxs-lookup"><span data-stu-id="19a2b-169">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





