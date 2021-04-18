---
title: Prise en charge du filigrane
description: Prise en charge du filigrane
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media Format SDK, prise en charge du filigrane
- Kit de développement logiciel (SDK) Windows Media format, filigrane numérique
- ASF (Advanced Systems Format), prise en charge du filigrane
- ASF (format des systèmes avancés), prise en charge du filigrane
- ASF (Advanced Systems Format), filigrane numérique
- ASF (format de systèmes avancés), filigrane numérique
- SDK Windows Media format, DMO
- ASF (Advanced Systems Format), DMO
- ASF (format des systèmes avancés), DMO
- Windows Media Format SDK, interface IWMWatermarkInfo
- ASF (Advanced Systems Format), interface IWMWatermarkInfo
- ASF (format des systèmes avancés), interface IWMWatermarkInfo
- filigrane, à propos de
- filigrane numérique
- DirectX Media Object (DMO), à propos de
- DMO (objet multimédia DirectX), à propos de
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511876"
---
# <a name="watermarking-support"></a><span data-ttu-id="4cf79-120">Prise en charge du filigrane</span><span class="sxs-lookup"><span data-stu-id="4cf79-120">Watermarking Support</span></span>

<span data-ttu-id="4cf79-121">Le filigrane numérique est un moyen d’incorporer des droits d’auteur ou d’autres informations dans les données d’un flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="4cf79-121">Digital watermarking is a way to embed copyright or other information in the data of a media stream.</span></span> <span data-ttu-id="4cf79-122">Les techniques de filigrane varient considérablement d’une solution à l’autre.</span><span class="sxs-lookup"><span data-stu-id="4cf79-122">Techniques for watermarking vary widely from one solution to the next.</span></span> <span data-ttu-id="4cf79-123">La forme la plus simple de filigrane est d’ajouter simplement une image d’identification à chaque image d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="4cf79-123">The simplest form of watermarking is simply adding an identifying image to each frame of a video stream.</span></span> <span data-ttu-id="4cf79-124">Les stations de télévision utilisent souvent cette technique pour insérer un logo semi-transparent dans le coin inférieur de leur diffusion.</span><span class="sxs-lookup"><span data-stu-id="4cf79-124">Television stations frequently use this technique to insert a semi-transparent logo in a bottom corner of their broadcast.</span></span> <span data-ttu-id="4cf79-125">Des formes plus sophistiquées de filigrane numérique sont imperceptibles à l’utilisateur qui regarde ou écoute le contenu.</span><span class="sxs-lookup"><span data-stu-id="4cf79-125">More sophisticated forms of digital watermarking are imperceptible to the user watching or listening to the content.</span></span>

<span data-ttu-id="4cf79-126">Le kit de développement logiciel (SDK) Windows Media format prend en charge l’utilisation de [*DMOs*](wmformat-glossary.md)de filigrane numérique.</span><span class="sxs-lookup"><span data-stu-id="4cf79-126">The Windows Media Format SDK supports the use of digital watermarking [*DMOs*](wmformat-glossary.md).</span></span> <span data-ttu-id="4cf79-127">Dans la pratique, un système de filigrane est très similaire à un codec : il prend des exemples de supports, exécute des algorithmes sur les données et génère les exemples modifiés.</span><span class="sxs-lookup"><span data-stu-id="4cf79-127">In practice, a watermarking system is very similar to a codec: it takes media samples, runs algorithms on the data, and outputs the altered samples.</span></span> <span data-ttu-id="4cf79-128">Lorsqu’un système de filigrane est spécifié pour un flux de données, l’objet Writer comprend le module DMO dans son traitement d’exemples d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4cf79-128">When a watermarking system is specified for a stream, the writer object includes the DMO in its processing of input samples.</span></span>

<span data-ttu-id="4cf79-129">Vous devez spécifier les informations de configuration du filigrane lorsque vous configurez un flux pour le filigrane.</span><span class="sxs-lookup"><span data-stu-id="4cf79-129">You must specify watermark configuration information when you configure a stream for watermarking.</span></span> <span data-ttu-id="4cf79-130">Les valeurs de configuration sont différentes en fonction du filigrane DMO.</span><span class="sxs-lookup"><span data-stu-id="4cf79-130">The configuration values will be different depending upon the watermarking DMO.</span></span> <span data-ttu-id="4cf79-131">La DMO que vous utilisez doit être accompagnée d’instructions décrivant les valeurs de configuration qu’elle prend en charge.</span><span class="sxs-lookup"><span data-stu-id="4cf79-131">The DMO you use should come with instructions describing the configuration values it supports.</span></span>

<span data-ttu-id="4cf79-132">Pour plus d’informations sur les paramètres utilisés pour spécifier un système de filigrane, consultez [ **IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span><span class="sxs-lookup"><span data-stu-id="4cf79-132">For information about the settings used to specify a watermarking system, see [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span></span>

<span data-ttu-id="4cf79-133">Vous pouvez programmer votre application pour énumérer les DMOs de filigranes installés sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="4cf79-133">You can program your application to enumerate the watermarking DMOs installed on the client computer.</span></span> <span data-ttu-id="4cf79-134">Pour plus d’informations, consultez l’interface [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .</span><span class="sxs-lookup"><span data-stu-id="4cf79-134">For more information, see the [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cf79-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4cf79-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cf79-136">**Fonctionnalités d’écriture de fichier**</span><span class="sxs-lookup"><span data-stu-id="4cf79-136">**File Writing Features**</span></span>](file-writing-features.md)
</dt> </dl>

 

 




