---
description: Le décodeur Windows Media Audio décode les flux audio qui ont été encodés par l’encodeur Windows Media Audio.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Décodeur Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532556"
---
# <a name="windows-media-audio-decoder"></a><span data-ttu-id="ecd09-103">Décodeur Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="ecd09-103">Windows Media Audio Decoder</span></span>

<span data-ttu-id="ecd09-104">Le décodeur Windows Media Audio décode les flux audio qui ont été encodés par l’encodeur [**Windows Media Audio**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="ecd09-104">The Windows Media Audio decoder decodes audio streams that were encoded by the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span> <span data-ttu-id="ecd09-105">Le codeur et le décodeur prennent en charge trois catégories de données audio encodées : Windows Media Audio standard, Windows Media Audio Professional et Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="ecd09-105">The encoder and decoder support three categories of encoded audio: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="ecd09-106">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="ecd09-106">Class Identifier</span></span>

<span data-ttu-id="ecd09-107">L’identificateur de classe (CLSID) du décodeur de Windows Media Audio est représenté par la constante **CLSID \_ CWMADecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="ecd09-107">The class identifier (CLSID) for the Windows Media Audio decoder is represented by the constant **CLSID\_CWMADecMediaObject**.</span></span> <span data-ttu-id="ecd09-108">Vous pouvez créer une instance du décodeur audio en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="ecd09-108">You can create an instance of the audio decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="ecd09-109">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="ecd09-109">Input Formats</span></span>

<span data-ttu-id="ecd09-110">Le tableau suivant répertorie les balises de format audio qui représentent les catégories d’entrée prises en charge par le décodeur Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="ecd09-110">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio decoder.</span></span> <span data-ttu-id="ecd09-111">Pour plus d’informations sur la définition des types d’entrée et de sortie pour le décodeur, consultez [configuration du décodage audio](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="ecd09-111">For information about how to set the input and output types for the decoder, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>



| <span data-ttu-id="ecd09-112">Balise de format, constante</span><span class="sxs-lookup"><span data-stu-id="ecd09-112">Format tag constant</span></span>             | <span data-ttu-id="ecd09-113">Mettre en forme la valeur de balise</span><span class="sxs-lookup"><span data-stu-id="ecd09-113">Format tag value</span></span> | <span data-ttu-id="ecd09-114">Format audio</span><span class="sxs-lookup"><span data-stu-id="ecd09-114">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="ecd09-115">\_WMAUDIO2 format \_ Wave</span><span class="sxs-lookup"><span data-stu-id="ecd09-115">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="ecd09-116">0x0161</span><span class="sxs-lookup"><span data-stu-id="ecd09-116">0x0161</span></span>           | <span data-ttu-id="ecd09-117">Windows Media Audio standard</span><span class="sxs-lookup"><span data-stu-id="ecd09-117">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="ecd09-118">\_WMAUDIO3 format \_ Wave</span><span class="sxs-lookup"><span data-stu-id="ecd09-118">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="ecd09-119">0x0162</span><span class="sxs-lookup"><span data-stu-id="ecd09-119">0x0162</span></span>           | <span data-ttu-id="ecd09-120">Windows Media Audio professionnel</span><span class="sxs-lookup"><span data-stu-id="ecd09-120">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="ecd09-121">WAVE \_ format \_ WMAUDIO \_ Lossless</span><span class="sxs-lookup"><span data-stu-id="ecd09-121">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="ecd09-122">0x0163</span><span class="sxs-lookup"><span data-stu-id="ecd09-122">0x0163</span></span>           | <span data-ttu-id="ecd09-123">Windows Media Audio sans perte</span><span class="sxs-lookup"><span data-stu-id="ecd09-123">Windows Media Audio Lossless</span></span>     |



 

## <a name="output-formats"></a><span data-ttu-id="ecd09-124">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="ecd09-124">Output Formats</span></span>

<span data-ttu-id="ecd09-125">Le tableau suivant répertorie les balises de format audio qui représentent les types de sortie pris en charge par le **décodeur Windows Media Audio**.</span><span class="sxs-lookup"><span data-stu-id="ecd09-125">The following table shows the audio format tags that represent the output types supported by the **Windows Media Audio Decoder**.</span></span> <span data-ttu-id="ecd09-126">Pour plus d’informations sur la définition des types d’entrée et de sortie pour le décodeur, consultez Configuration de l' [encodage audio](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="ecd09-126">For information about how to set the input and output types for the decoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="ecd09-127">Balise de format, constante</span><span class="sxs-lookup"><span data-stu-id="ecd09-127">Format tag constant</span></span>       | <span data-ttu-id="ecd09-128">Mettre en forme la valeur de balise</span><span class="sxs-lookup"><span data-stu-id="ecd09-128">Format tag value</span></span> | <span data-ttu-id="ecd09-129">Format audio</span><span class="sxs-lookup"><span data-stu-id="ecd09-129">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="ecd09-130">\_PCM format \_ Wave</span><span class="sxs-lookup"><span data-stu-id="ecd09-130">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="ecd09-131">0x0001</span><span class="sxs-lookup"><span data-stu-id="ecd09-131">0x0001</span></span>           | <span data-ttu-id="ecd09-132">Format PCM</span><span class="sxs-lookup"><span data-stu-id="ecd09-132">PCM format</span></span>                                            |
| <span data-ttu-id="ecd09-133">\_format Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="ecd09-133">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="ecd09-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="ecd09-134">0x0003</span></span>           | <span data-ttu-id="ecd09-135">Virgule flottante IEEE</span><span class="sxs-lookup"><span data-stu-id="ecd09-135">IEEE floating point</span></span>                                   |
| <span data-ttu-id="ecd09-136">\_format Wave \_ extensible</span><span class="sxs-lookup"><span data-stu-id="ecd09-136">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="ecd09-137">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="ecd09-137">0xFFFE</span></span>           | <span data-ttu-id="ecd09-138">Format PCM/IEEE dans la structure **WAVEFORMATEXTENSIBLE**</span><span class="sxs-lookup"><span data-stu-id="ecd09-138">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="ecd09-139">Interfaces</span><span class="sxs-lookup"><span data-stu-id="ecd09-139">Interfaces</span></span>

<span data-ttu-id="ecd09-140">Un objet décodeur audio expose l’interface **IMediaObject** afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface **IMFTransform** afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="ecd09-140">An audio decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="ecd09-141">Un décodeur Windows Media Audio se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ecd09-141">A Windows Media Audio decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="ecd09-142">Le tableau suivant indique les conditions sous lesquelles un décodeur audio se comporte comme un DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="ecd09-142">The following table shows the conditions under which an audio decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="ecd09-143">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ecd09-143">Operating system</span></span> | <span data-ttu-id="ecd09-144">Comportement du décodeur</span><span class="sxs-lookup"><span data-stu-id="ecd09-144">Decoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd09-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ecd09-145">Windows XP</span></span>       | <span data-ttu-id="ecd09-146">Un décodeur de Windows Media Audio se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="ecd09-146">A Windows Media Audio decoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="ecd09-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecd09-147">Windows Vista</span></span>    | <span data-ttu-id="ecd09-148">Par défaut, un décodeur de Windows Media Audio se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="ecd09-148">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="ecd09-149">Si vous obtenez une interface **IMFTransform** ou une interface **IPropertyStore** sur un décodeur audio, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="ecd09-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="ecd09-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ecd09-150">Windows 7</span></span>        | <span data-ttu-id="ecd09-151">Par défaut, un décodeur de Windows Media Audio se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="ecd09-151">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="ecd09-152">Si vous obtenez une interface **IMFTransform** sur un décodeur audio, elle se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="ecd09-152">If you obtain an **IMFTransform** interface on an audio decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="properties"></a><span data-ttu-id="ecd09-153">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ecd09-153">Properties</span></span>

<span data-ttu-id="ecd09-154">Le décodeur Windows Media Audio prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ecd09-154">The Windows Media Audio decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ecd09-155">Propriété</span><span class="sxs-lookup"><span data-stu-id="ecd09-155">Property</span></span></th>
<th><span data-ttu-id="ecd09-156">Description</span><span class="sxs-lookup"><span data-stu-id="ecd09-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ecd09-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-158">Spécifie le nombre maximal d’échantillons PCM supplémentaires qui peuvent être retournés à la fin du décodage d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="ecd09-158">Specifies the maximum number of additional PCM samples that might be returned at the end of decoding a file.</span></span><br/> <dl> <span data-ttu-id="ecd09-159">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="ecd09-160">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="ecd09-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="ecd09-161">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ecd09-161">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ecd09-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-163">Spécifie le mode de contrôle de plage dynamique qui sera utilisé par le décodeur audio.</span><span class="sxs-lookup"><span data-stu-id="ecd09-163">Specifies the dynamic-range control mode that the audio decoder will use.</span></span><br/> <dl> <span data-ttu-id="ecd09-164">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-164">Windows XP and later.</span></span><br />
<span data-ttu-id="ecd09-165">Standard, professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="ecd09-165">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="ecd09-166">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="ecd09-166">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ecd09-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-168">Spécifie les coefficients de repli pour le décodage de l’audio multicanaux pour un nombre de canaux inférieur à celui contenu dans le flux encodé.</span><span class="sxs-lookup"><span data-stu-id="ecd09-168">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span> <br/> <dl> <span data-ttu-id="ecd09-169">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-169">Windows XP and later.</span></span><br />
<span data-ttu-id="ecd09-170">Professional</span><span class="sxs-lookup"><span data-stu-id="ecd09-170">Professional</span></span><br />
<span data-ttu-id="ecd09-171">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="ecd09-171">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ecd09-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-173">Spécifie si le décodeur audio doit fournir une sortie haute résolution.</span><span class="sxs-lookup"><span data-stu-id="ecd09-173">Specifies whether the audio decoder should deliver high-resolution output.</span></span><br/> <dl> <span data-ttu-id="ecd09-174">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-174">Windows XP and later.</span></span><br />
<span data-ttu-id="ecd09-175">Professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="ecd09-175">Professional, Lossless.</span></span><br />
<span data-ttu-id="ecd09-176">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="ecd09-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ecd09-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-178">Spécifie si le décodeur audio doit effectuer Lt-Rt pli vers le dessous.</span><span class="sxs-lookup"><span data-stu-id="ecd09-178">Specifies whether the audio decoder should perform Lt-Rt fold down.</span></span><br/> <dl> <span data-ttu-id="ecd09-179">Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="ecd09-180">Professionnel.</span><span class="sxs-lookup"><span data-stu-id="ecd09-180">Professional.</span></span><br />
<span data-ttu-id="ecd09-181">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="ecd09-181">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ecd09-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-183">Spécifie la configuration de l’orateur sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="ecd09-183">Specifies the speaker configuration on the client computer.</span></span><br/> <dl> <span data-ttu-id="ecd09-184">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-184">Windows XP and later.</span></span><br />
<span data-ttu-id="ecd09-185">Professionnel.</span><span class="sxs-lookup"><span data-stu-id="ecd09-185">Professional.</span></span><br />
<span data-ttu-id="ecd09-186">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="ecd09-186">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ecd09-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-188">Spécifie le niveau de volume moyen de contenu audio.</span><span class="sxs-lookup"><span data-stu-id="ecd09-188">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="ecd09-189">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-189">Windows XP and later.</span></span><br />
<span data-ttu-id="ecd09-190">Professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="ecd09-190">Professional, Lossless.</span></span><br />
<span data-ttu-id="ecd09-191">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ecd09-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ecd09-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-193">Spécifie le niveau de volume moyen souhaité de contenu audio de sortie.</span><span class="sxs-lookup"><span data-stu-id="ecd09-193">Specifies the desired average volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="ecd09-194">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-194">Windows XP and later.</span></span><br />
<span data-ttu-id="ecd09-195">Professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="ecd09-195">Professional, Lossless.</span></span><br />
<span data-ttu-id="ecd09-196">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="ecd09-196">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ecd09-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-198">Spécifie le niveau de volume le plus élevé dans le contenu audio.</span><span class="sxs-lookup"><span data-stu-id="ecd09-198">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="ecd09-199">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-199">Windows XP and later.</span></span><br />
<span data-ttu-id="ecd09-200">Professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="ecd09-200">Professional, Lossless.</span></span><br />
<span data-ttu-id="ecd09-201">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ecd09-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ecd09-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="ecd09-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span></span></td>
<td><span data-ttu-id="ecd09-203">Spécifie le niveau de volume maximal souhaité pour le contenu audio de sortie.</span><span class="sxs-lookup"><span data-stu-id="ecd09-203">Specifies the desired maximum volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="ecd09-204">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecd09-204">Windows XP and later.</span></span><br />
<span data-ttu-id="ecd09-205">Professionnel, sans perte.</span><span class="sxs-lookup"><span data-stu-id="ecd09-205">Professional, Lossless.</span></span><br />
<span data-ttu-id="ecd09-206">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="ecd09-206">Write-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="ecd09-207">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecd09-207">Requirements</span></span>



| <span data-ttu-id="ecd09-208">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecd09-208">Requirement</span></span> | <span data-ttu-id="ecd09-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecd09-209">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd09-210">Client</span><span class="sxs-lookup"><span data-stu-id="ecd09-210">Client</span></span><br/> | <span data-ttu-id="ecd09-211">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="ecd09-211">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="ecd09-212">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecd09-212">Header</span></span><br/> | <dl> <span data-ttu-id="ecd09-213"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd09-213"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="ecd09-214">DLL</span><span class="sxs-lookup"><span data-stu-id="ecd09-214">DLL</span></span><br/>    | <dl> <span data-ttu-id="ecd09-215"><dt>Wmadmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecd09-215"><dt>Wmadmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ecd09-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecd09-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd09-217">Objets codec</span><span class="sxs-lookup"><span data-stu-id="ecd09-217">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="ecd09-218">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="ecd09-218">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




