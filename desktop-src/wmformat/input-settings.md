---
title: Paramètres d’entrée
description: Paramètres d’entrée
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media Format SDK, constantes globales
- ASF (Advanced Systems Format), constantes globales
- ASF (format de systèmes avancés), constantes globales
- constantes globales, liste des
- Windows Media Format SDK, constantes
- ASF (Advanced Systems Format), constantes
- ASF (Advanced Systems Format), constantes
- constantes, liste
- Windows Media Format SDK, paramètres d’entrée
- ASF (Advanced Systems Format), paramètres d’entrée
- ASF (format des systèmes avancés), paramètres d’entrée
- paramètres d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030771"
---
# <a name="input-settings"></a><span data-ttu-id="e97d2-115">Paramètres d’entrée</span><span class="sxs-lookup"><span data-stu-id="e97d2-115">Input Settings</span></span>

<span data-ttu-id="e97d2-116">Les constantes globales suivantes sont utilisées pour identifier les paramètres d’entrée pour le writer.</span><span class="sxs-lookup"><span data-stu-id="e97d2-116">The following global constants are used to identify input settings for the writer.</span></span>



| <span data-ttu-id="e97d2-117">Constante globale</span><span class="sxs-lookup"><span data-stu-id="e97d2-117">Global constant</span></span>                        | <span data-ttu-id="e97d2-118">\_type de \_ données attr WMT</span><span class="sxs-lookup"><span data-stu-id="e97d2-118">WMT\_ATTR\_DATATYPE</span></span>                                                                                                                       | <span data-ttu-id="e97d2-119">Description de *pValue*</span><span class="sxs-lookup"><span data-stu-id="e97d2-119">Description of *pValue*</span></span>                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e97d2-120">\_wszDeinterlaceMode g</span><span class="sxs-lookup"><span data-stu-id="e97d2-120">g\_wszDeinterlaceMode</span></span>                  | <span data-ttu-id="e97d2-121">**WMT \_ TAPEZ \_ DWORD** avec l’une des valeurs de la table mode dans la rubrique [pour désentrelacer la vidéo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="e97d2-121">**WMT\_TYPE\_DWORD** set to one of the values in the mode table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span>            | <span data-ttu-id="e97d2-122">Lorsque cette valeur est définie, spécifie le type de contenu entrelacé de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="e97d2-122">When set, specifies the type of interlaced content of the input.</span></span> <span data-ttu-id="e97d2-123">Pour plus d’informations, consultez [pour libérer de la vidéo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="e97d2-123">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>                                                                                                                            |
| <span data-ttu-id="e97d2-124">\_wszFixedFrameRate g</span><span class="sxs-lookup"><span data-stu-id="e97d2-124">g\_wszFixedFrameRate</span></span>                   | <span data-ttu-id="e97d2-125">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="e97d2-125">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="e97d2-126">Lorsque la valeur est définie sur true, le codec ne supprime pas les frames pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="e97d2-126">When set to True, instructs the codec not to drop any frames during encoding.</span></span> <span data-ttu-id="e97d2-127">La [*fréquence d’images*](wmformat-glossary.md) du flux vidéo de sortie est alors constante.</span><span class="sxs-lookup"><span data-stu-id="e97d2-127">This will cause the [*frame rate*](wmformat-glossary.md) of the output video stream to be constant.</span></span> <span data-ttu-id="e97d2-128">La fréquence d’images du flux d’entrée n’a pas besoin d’être constante.</span><span class="sxs-lookup"><span data-stu-id="e97d2-128">The frame rate of the input stream does not need to be constant.</span></span> |
| <span data-ttu-id="e97d2-129">\_wszInitialPatternForInverseTelecine g</span><span class="sxs-lookup"><span data-stu-id="e97d2-129">g\_wszInitialPatternForInverseTelecine</span></span> | <span data-ttu-id="e97d2-130">**WMT \_ TAPEZ \_ DWORD** défini sur l’une des valeurs de la table de modèles initiale dans la rubrique [pour désentrelacer la vidéo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="e97d2-130">**WMT\_TYPE\_DWORD** set to one of the values in the initial pattern table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span> | <span data-ttu-id="e97d2-131">Lorsque le mode de désentrelacement est défini sur WM \_ DM \_ désentrelacer \_ INVERSETELECINE, vous pouvez définir cette valeur pour spécifier le modèle de l’entrée [*Telecine*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="e97d2-131">When the deinterlace mode is set to WM\_DM\_DEINTERLACE\_INVERSETELECINE, this can be set to specify the pattern of the [*telecine*](wmformat-glossary.md) input.</span></span> <span data-ttu-id="e97d2-132">Pour plus d’informations, consultez [pour libérer de la vidéo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="e97d2-132">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>        |
| <span data-ttu-id="e97d2-133">\_wszInterlacedCoding g</span><span class="sxs-lookup"><span data-stu-id="e97d2-133">g\_wszInterlacedCoding</span></span>                 | <span data-ttu-id="e97d2-134">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="e97d2-134">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="e97d2-135">Quand la valeur est true, spécifie que le codec doit encoder le flux en tant que contenu entrelacé.</span><span class="sxs-lookup"><span data-stu-id="e97d2-135">When set to True, specifies that that the codec should encode the stream as interlaced content.</span></span> <span data-ttu-id="e97d2-136">Pour plus d’informations, consultez [pour utiliser une vidéo entrelacée](to-use-interlaced-video.md).</span><span class="sxs-lookup"><span data-stu-id="e97d2-136">For more information, see [To Use Interlaced Video](to-use-interlaced-video.md).</span></span>                                                                                       |
| <span data-ttu-id="e97d2-137">\_wszJPEGCompressionQuality g</span><span class="sxs-lookup"><span data-stu-id="e97d2-137">g\_wszJPEGCompressionQuality</span></span>           | <span data-ttu-id="e97d2-138">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e97d2-138">**WMT\_TYPE\_DWORD**</span></span>                                                                                                                      | <span data-ttu-id="e97d2-139">Spécifie le niveau de qualité JPEG (compris entre 1 et 100) à utiliser sur l’entrée.</span><span class="sxs-lookup"><span data-stu-id="e97d2-139">Specifies the JPEG quality level (from 1 to 100) to be used on the input.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="e97d2-140">\_wszWatermarkCLSID g</span><span class="sxs-lookup"><span data-stu-id="e97d2-140">g\_wszWatermarkCLSID</span></span>                   | <span data-ttu-id="e97d2-141">**\_GUID du type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e97d2-141">**WMT\_TYPE\_GUID**</span></span>                                                                                                                       | <span data-ttu-id="e97d2-142">La valeur est définie sur le GUID de filigrane.</span><span class="sxs-lookup"><span data-stu-id="e97d2-142">The value is set to the watermark GUID.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="e97d2-143">\_wszWatermarkConfig g</span><span class="sxs-lookup"><span data-stu-id="e97d2-143">g\_wszWatermarkConfig</span></span>                  | <span data-ttu-id="e97d2-144">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="e97d2-144">**WMT\_TYPE\_STRING**</span></span>                                                                                                                     | <span data-ttu-id="e97d2-145">La valeur est définie sur la configuration du filigrane.</span><span class="sxs-lookup"><span data-stu-id="e97d2-145">The value is set to the watermark configuration.</span></span> <span data-ttu-id="e97d2-146">Cette valeur varie en fonction du filigrane DMO.</span><span class="sxs-lookup"><span data-stu-id="e97d2-146">This value will vary depending upon the watermarking DMO.</span></span> <span data-ttu-id="e97d2-147">Pour plus d’informations, consultez la documentation du système de filigrane.</span><span class="sxs-lookup"><span data-stu-id="e97d2-147">Consult the documentation of the watermarking system for more information.</span></span>                                                                                   |



 

> [!Note]  
> <span data-ttu-id="e97d2-148">Les paramètres d’entrée configurés pour un flux ne sont pas conservés dans le fichier écrit.</span><span class="sxs-lookup"><span data-stu-id="e97d2-148">The input settings configured for a stream are not persisted in the written file.</span></span> <span data-ttu-id="e97d2-149">Si vous souhaitez que votre lecteur personnalisé ait accès à ces paramètres d’encodage, vous devez créer des attributs personnalisés pour les stocker dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="e97d2-149">If you want your custom reader to have access to these encoding parameters, you must create custom attributes to store them in the file header.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e97d2-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e97d2-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e97d2-151">**IWMWriterAdvanced2::GetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="e97d2-151">**IWMWriterAdvanced2::GetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[<span data-ttu-id="e97d2-152">**IWMWriterAdvanced2::SetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="e97d2-152">**IWMWriterAdvanced2::SetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




