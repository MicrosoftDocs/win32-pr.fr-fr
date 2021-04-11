---
title: Formats
description: Formats
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK, entrées
- Windows Media Format SDK, flux
- Windows Media Format SDK, sorties
- Windows Media Format SDK, formats
- ASF (Advanced Systems Format), entrées
- ASF (format des systèmes avancés), entrées
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- ASF (Advanced Systems Format), sorties
- ASF (format des systèmes avancés), sorties
- Formats ASF (Advanced Systems Format), formats
- ASF (format des systèmes avancés), formats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310785"
---
# <a name="formats"></a><span data-ttu-id="d41a1-115">Formats</span><span class="sxs-lookup"><span data-stu-id="d41a1-115">Formats</span></span>

<span data-ttu-id="d41a1-116">Les informations contenues dans un format décrivent tout ce que vous devez savoir sur un type de média particulier.</span><span class="sxs-lookup"><span data-stu-id="d41a1-116">The information in a format describes everything you need to know about a particular type of media.</span></span> <span data-ttu-id="d41a1-117">Chaque format a un type majeur, tel que audio ou vidéo, et peut avoir un sous-type.</span><span class="sxs-lookup"><span data-stu-id="d41a1-117">Every format has a major type, like audio or video, and may have a subtype.</span></span> <span data-ttu-id="d41a1-118">Les formats contiennent des informations différentes en fonction du type principal.</span><span class="sxs-lookup"><span data-stu-id="d41a1-118">Formats contain different information based on major type.</span></span> <span data-ttu-id="d41a1-119">Les formats audio et vidéo requièrent bien plus d’informations que d’autres types.</span><span class="sxs-lookup"><span data-stu-id="d41a1-119">Audio and video formats require much more information than other types.</span></span>

<span data-ttu-id="d41a1-120">Tout comme les objets du kit de développement logiciel (SDK) de format Windows Media différencient les numéros d’entrée, les numéros de flux et les numéros de sortie (consultez [entrées, flux et sorties](inputs-streams-and-outputs.md)), il existe des différences importantes entre les formats d’entrée, les formats de flux et les formats de sortie.</span><span class="sxs-lookup"><span data-stu-id="d41a1-120">Just as the objects of the Windows Media Format SDK differentiate between input numbers, stream numbers, and output numbers (see [Inputs, Streams and Outputs](inputs-streams-and-outputs.md)), there are important distinctions between input formats, stream formats, and output formats.</span></span> <span data-ttu-id="d41a1-121">Ces différences sont décrites ici :</span><span class="sxs-lookup"><span data-stu-id="d41a1-121">These differences are described here:</span></span>

## <a name="input-formats"></a><span data-ttu-id="d41a1-122">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="d41a1-122">Input Formats</span></span>

<span data-ttu-id="d41a1-123">Un format d’entrée décrit les médias numériques que vous transmettez à l’objet enregistreur.</span><span class="sxs-lookup"><span data-stu-id="d41a1-123">An input format describes the digital media that you pass to the writer object.</span></span> <span data-ttu-id="d41a1-124">Si un flux de données d’un fichier ASF est compressé à l’aide d’un codec, le codec prend en charge uniquement certains formats d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d41a1-124">If a stream in an ASF file is compressed with a codec, the codec will support only certain input formats.</span></span> <span data-ttu-id="d41a1-125">Lorsque vous utilisez les codecs vidéo et Windows Media Audio, vous pouvez énumérer les formats d’entrée pris en charge à l’aide de l’objet Writer.</span><span class="sxs-lookup"><span data-stu-id="d41a1-125">When using the Windows Media Audio and Video codecs, you can enumerate the supported input formats using the writer object.</span></span> <span data-ttu-id="d41a1-126">Lors de l’écriture d’un fichier, vous êtes responsable de la sélection d’un format d’entrée qui correspond à votre média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d41a1-126">When writing a file, you are responsible for selecting an input format that matches your input media.</span></span>

<span data-ttu-id="d41a1-127">Bien que le format de média d’entrée doive être pris en charge par le codec destiné à compresser les données, certains paramètres de format d’entrée n’ont pas besoin de correspondre au format de flux.</span><span class="sxs-lookup"><span data-stu-id="d41a1-127">Although the input media format must be supported by the codec that will compress the data, some input format settings need not match the stream format.</span></span> <span data-ttu-id="d41a1-128">Par exemple, le format d’entrée d’un flux vidéo peut avoir une taille de trame différente de celle définie dans le format de flux.</span><span class="sxs-lookup"><span data-stu-id="d41a1-128">For example, the input format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="d41a1-129">Dans ce cas, le codec effectue des conversions.</span><span class="sxs-lookup"><span data-stu-id="d41a1-129">The codec will perform conversions in these cases.</span></span>

## <a name="stream-formats"></a><span data-ttu-id="d41a1-130">Formats de flux</span><span class="sxs-lookup"><span data-stu-id="d41a1-130">Stream Formats</span></span>

<span data-ttu-id="d41a1-131">Un format de flux décrit la forme du support tel qu’il est stocké dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="d41a1-131">A stream format describes the form of the media as it is stored in the ASF file.</span></span> <span data-ttu-id="d41a1-132">Le format de flux est le format décrit dans le profil et peut être ou non le même que le format d’entrée et le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="d41a1-132">The stream format is the format described in the profile, and may or may not be the same as the input format and output format.</span></span> <span data-ttu-id="d41a1-133">Si un codec est utilisé pour compresser les données dans un flux, le format de flux est différent des formats d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="d41a1-133">If a codec is used to compress the data in a stream, the stream format will be different than the input and output formats.</span></span>

<span data-ttu-id="d41a1-134">Lorsque vous utilisez les codecs vidéo et Windows Media Audio, vous devez obtenir une liste des formats de flux pris en charge à partir du codec pour vous assurer que vous n’essayez pas de spécifier un format non pris en charge par le code.</span><span class="sxs-lookup"><span data-stu-id="d41a1-134">When using the Windows Media Audio and Video codecs, you must obtain a list of supported stream formats from the codec to ensure that you are not attempting to specify a format that the code does not support.</span></span> <span data-ttu-id="d41a1-135">Certains paramètres de mise en forme, tels que la taille et la profondeur de couleur d’une image vidéo, doivent être configurés manuellement une fois le format du codec récupéré.</span><span class="sxs-lookup"><span data-stu-id="d41a1-135">Some format settings, such as the size and color depth of a video frame, must be configured manually after the codec format is retrieved.</span></span>

## <a name="output-formats"></a><span data-ttu-id="d41a1-136">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="d41a1-136">Output Formats</span></span>

<span data-ttu-id="d41a1-137">Un format de sortie décrit les supports numériques que le lecteur (ou lecteur synchrone) remet à votre application.</span><span class="sxs-lookup"><span data-stu-id="d41a1-137">An output format describes the digital media that the reader (or synchronous reader) delivers to your application.</span></span> <span data-ttu-id="d41a1-138">Si un flux de fichier ASF est compressé à l’aide d’un codec, le codec prend en charge uniquement certains formats de sortie.</span><span class="sxs-lookup"><span data-stu-id="d41a1-138">If a stream in an ASF file is compressed with a codec, the codec will support only certain output formats.</span></span> <span data-ttu-id="d41a1-139">Lorsque vous utilisez les codecs Windows Media Audio et vidéo, vous pouvez énumérer les formats de sortie pris en charge à l’aide de l’objet Reader.</span><span class="sxs-lookup"><span data-stu-id="d41a1-139">When using the Windows Media Audio and Video codecs, you can enumerate the supported output formats by using the reader object.</span></span> <span data-ttu-id="d41a1-140">Chacun des codecs Windows Media a un format de sortie par défaut, mais vous pouvez sélectionner n’importe quel format de sortie pris en charge pour l’exemple de remise.</span><span class="sxs-lookup"><span data-stu-id="d41a1-140">Each of the Windows Media codecs has a default output format, but you can select any supported output format for sample delivery.</span></span>

<span data-ttu-id="d41a1-141">Bien que le format de média de sortie doit être pris en charge par le codec qui a compressé les données, certains paramètres de format de sortie n’ont pas besoin de correspondre au format de flux.</span><span class="sxs-lookup"><span data-stu-id="d41a1-141">Although the output media format must be supported by the codec that compressed the data, some output format settings need not match the stream format.</span></span> <span data-ttu-id="d41a1-142">Par exemple, le format de sortie d’un flux vidéo peut avoir une taille de trame différente de celle définie dans le format de flux.</span><span class="sxs-lookup"><span data-stu-id="d41a1-142">For example, the output format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="d41a1-143">Dans ce cas, le codec effectue des conversions.</span><span class="sxs-lookup"><span data-stu-id="d41a1-143">The codec will perform conversions in these cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d41a1-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d41a1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d41a1-145">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="d41a1-145">**Concepts**</span></span>](concepts.md)
</dt> </dl>

 

 




