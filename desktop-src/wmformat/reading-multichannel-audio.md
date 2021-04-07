---
title: Lecture de l’audio multicanal
description: Lecture de l’audio multicanal
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, lecture audio multicanal
- ASF (Advanced Systems Format), lecture audio multicanal
- ASF (format des systèmes avancés), lire l’audio multicanal
- ASF (Advanced Systems Format), audio multicanal
- ASF (format de systèmes avancés), audio multicanal
- codecs, lecture de l’audio multicanal
- audio multicanal, lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729453"
---
# <a name="reading-multichannel-audio"></a><span data-ttu-id="a7f89-110">Lecture de l’audio multicanal</span><span class="sxs-lookup"><span data-stu-id="a7f89-110">Reading Multichannel Audio</span></span>

<span data-ttu-id="a7f89-111">Le codec Windows Media Audio 9 Professional peut encoder l’audio multicanal (plus de deux canaux).</span><span class="sxs-lookup"><span data-stu-id="a7f89-111">The Windows Media Audio 9 Professional codec can encode multichannel audio (more than two channels).</span></span> <span data-ttu-id="a7f89-112">Lors de la lecture d’un fichier à l’aide de l’audio multicanal, vous devez configurer la sortie correctement ou l’audio sera remis à une qualité inférieure et en stéréo.</span><span class="sxs-lookup"><span data-stu-id="a7f89-112">When reading a file with multichannel audio, you must configure the output properly or the audio will be delivered at a lower quality and in stereo.</span></span> <span data-ttu-id="a7f89-113">Pour définir une sortie pour la remise audio multicanal, vous devez définir deux paramètres de sortie : g \_ wszEnableDiscreteOutput et g \_ wszSpeakerConfig.</span><span class="sxs-lookup"><span data-stu-id="a7f89-113">To set an output for multichannel audio delivery, you must set two output settings: g\_wszEnableDiscreteOutput and g\_wszSpeakerConfig.</span></span>

<span data-ttu-id="a7f89-114">Le paramètre g \_ wszEnableDiscreteOutput sur **true** définit le codec pour fournir une sortie audio haute définition.</span><span class="sxs-lookup"><span data-stu-id="a7f89-114">Setting g\_wszEnableDiscreteOutput to **TRUE** sets the codec to deliver high-definition audio output.</span></span> <span data-ttu-id="a7f89-115">Le son haute définition est encodé par le codec Windows Media Audio 9 avec des échantillons de 24 bits en stéréo ou plusieurs canaux.</span><span class="sxs-lookup"><span data-stu-id="a7f89-115">High-definition audio is encoded by the Windows Media Audio 9 codec with 24-bit samples in stereo or multiple channels.</span></span> <span data-ttu-id="a7f89-116">Si ce paramètre a la **valeur false**, seule une sortie stéréo de 16 bits sera remise.</span><span class="sxs-lookup"><span data-stu-id="a7f89-116">If this setting is **FALSE**, only 16-bit stereo output will be delivered.</span></span>

<span data-ttu-id="a7f89-117">Le nombre de haut-parleurs sur l’ordinateur de jeu est défini avec g \_ wszSpeakerConfig.</span><span class="sxs-lookup"><span data-stu-id="a7f89-117">The number of speakers on the playing computer is set with g\_wszSpeakerConfig.</span></span> <span data-ttu-id="a7f89-118">Ce paramètre est une valeur **DWORD** définie sur l’une des constantes de haut-parleur DirectSound indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7f89-118">This setting is a **DWORD** value set to one of the DirectSound speaker constants listed in the following table.</span></span> <span data-ttu-id="a7f89-119">Pour résoudre ces noms de constantes pour votre compilateur, vous devez inclure dsound. h.</span><span class="sxs-lookup"><span data-stu-id="a7f89-119">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="a7f89-120">Constante</span><span class="sxs-lookup"><span data-stu-id="a7f89-120">Constant</span></span>             | <span data-ttu-id="a7f89-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7f89-121">Value</span></span>      | <span data-ttu-id="a7f89-122">Description</span><span class="sxs-lookup"><span data-stu-id="a7f89-122">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a7f89-123">DSSPEAKER \_ DIRECTOUT</span><span class="sxs-lookup"><span data-stu-id="a7f89-123">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="a7f89-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7f89-124">0x00000000</span></span> | <span data-ttu-id="a7f89-125">L’audio est transmis directement, sans être configuré pour les intervenants.</span><span class="sxs-lookup"><span data-stu-id="a7f89-125">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="a7f89-126">\_casque DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="a7f89-126">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="a7f89-127">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a7f89-127">0x00000001</span></span> | <span data-ttu-id="a7f89-128">L’ordinateur client est équipé d’un casque.</span><span class="sxs-lookup"><span data-stu-id="a7f89-128">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="a7f89-129">\_mono DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="a7f89-129">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="a7f89-130">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a7f89-130">0x00000002</span></span> | <span data-ttu-id="a7f89-131">L’ordinateur client est équipé d’un orateur mono.</span><span class="sxs-lookup"><span data-stu-id="a7f89-131">The client computer is equipped with a monaural speaker.</span></span>                     |
| <span data-ttu-id="a7f89-132">DSSPEAKER \_ Quad</span><span class="sxs-lookup"><span data-stu-id="a7f89-132">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="a7f89-133">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a7f89-133">0x00000003</span></span> | <span data-ttu-id="a7f89-134">L’ordinateur client est équipé de haut-parleurs Quadraphonic.</span><span class="sxs-lookup"><span data-stu-id="a7f89-134">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="a7f89-135">\_stéréo DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="a7f89-135">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="a7f89-136">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a7f89-136">0x00000004</span></span> | <span data-ttu-id="a7f89-137">L’ordinateur client est équipé de haut-parleurs stéréo.</span><span class="sxs-lookup"><span data-stu-id="a7f89-137">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="a7f89-138">DSSPEAKER \_ surround</span><span class="sxs-lookup"><span data-stu-id="a7f89-138">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="a7f89-139">0x00000005</span><span class="sxs-lookup"><span data-stu-id="a7f89-139">0x00000005</span></span> | <span data-ttu-id="a7f89-140">L’ordinateur client est équipé de haut-parleurs Surround audio à quatre canaux.</span><span class="sxs-lookup"><span data-stu-id="a7f89-140">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="a7f89-141">DSSPEAKER \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="a7f89-141">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="a7f89-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="a7f89-142">0x00000006</span></span> | <span data-ttu-id="a7f89-143">L’ordinateur client est équipé de cinq enceintes et d’un caisson de basses.</span><span class="sxs-lookup"><span data-stu-id="a7f89-143">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="a7f89-144">DSSPEAKER \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="a7f89-144">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="a7f89-145">0x00000007</span><span class="sxs-lookup"><span data-stu-id="a7f89-145">0x00000007</span></span> | <span data-ttu-id="a7f89-146">L’ordinateur client est équipé de sept haut-parleurs et d’un caisson de basses.</span><span class="sxs-lookup"><span data-stu-id="a7f89-146">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="a7f89-147">Pour définir ces paramètres, utilisez [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="a7f89-147">To set these settings, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span>

<span data-ttu-id="a7f89-148">Enfin, pour que les canaux s’affichent discrètement, sans pli vers le stéréo, vous devez définir le type de support approprié sur la sortie en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="a7f89-148">Finally, for the channels to be output discretely, with no fold-down to stereo, you must set the correct media type on the output by following these steps:</span></span>

1.  <span data-ttu-id="a7f89-149">Appelez [**IWMReader :: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) pour obtenir le nombre de formats pris en charge pour la sortie audio appropriée.</span><span class="sxs-lookup"><span data-stu-id="a7f89-149">Call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported formats for the relevant audio output.</span></span> <span data-ttu-id="a7f89-150">Les index de format de sortie sont de base zéro.</span><span class="sxs-lookup"><span data-stu-id="a7f89-150">Output format indexes are zero-based.</span></span>
2.  <span data-ttu-id="a7f89-151">Pour chaque format pris en charge, appelez [**IWMReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) pour récupérer l’interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) sur l’objet Propriétés du média de sortie.</span><span class="sxs-lookup"><span data-stu-id="a7f89-151">For each supported format, call [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) to retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface on the output media properties object.</span></span>
3.  <span data-ttu-id="a7f89-152">Appelez [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) pour récupérer le type de média.</span><span class="sxs-lookup"><span data-stu-id="a7f89-152">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) to retrieve the media type.</span></span>
4.  <span data-ttu-id="a7f89-153">Si le type de média récupéré est le type Multichannel souhaité, définissez-le en appelant [**IWMReader :: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span><span class="sxs-lookup"><span data-stu-id="a7f89-153">If the retrieved media type is the desired multichannel type, then set it by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span></span>

<span data-ttu-id="a7f89-154">Une fois que vous avez défini une sortie discrète et la configuration de l’orateur, les formats de sortie énumérés par le lecteur doivent inclure des formats multicanaux qui utilisent la structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a7f89-154">After you have set discrete output and the speaker configuration, the output formats enumerated by the reader should include multichannel formats that use the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) structure.</span></span> <span data-ttu-id="a7f89-155">Si vous énumérez les formats de sortie avant de définir les propriétés, seuls les formats avec 1 ou 2 canaux et un maximum de 16 bits par canal seront inclus.</span><span class="sxs-lookup"><span data-stu-id="a7f89-155">If you enumerate the output formats before setting the properties, only formats with 1 or 2 channels and a maximum of 16 bits per channel will be included.</span></span> <span data-ttu-id="a7f89-156">Comme pour les autres formats audio, vous devez utiliser uniquement les formats énumérés par le lecteur. ne configurez pas votre propre.</span><span class="sxs-lookup"><span data-stu-id="a7f89-156">As with other audio formats, you should use only the formats enumerated by the reader; do not configure your own.</span></span>

> [!Note]  
> <span data-ttu-id="a7f89-157">Vous pouvez générer l’audio multicanal uniquement si votre application s’exécute sur Microsoft Windows XP ou une version ultérieure de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a7f89-157">You can output multichannel audio only if your application is running on Microsoft Windows XP or a later version of Microsoft Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a7f89-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7f89-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f89-159">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="a7f89-159">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="a7f89-160">**Lecture des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="a7f89-160">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="a7f89-161">**Paramètres de sortie**</span><span class="sxs-lookup"><span data-stu-id="a7f89-161">**Output Settings**</span></span>](output-settings.md)
</dt> <dt>

[<span data-ttu-id="a7f89-162">**Utilisation d' High-Resolution audio PCM**</span><span class="sxs-lookup"><span data-stu-id="a7f89-162">**Working with High-Resolution PCM Audio**</span></span>](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 