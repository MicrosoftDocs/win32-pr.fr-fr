---
description: Le filtre d’encodeur audio Microsoft MPEG-2 encode les couches audio MPEG-1 et II, y compris la prise en charge des extensions LSF (Low échantillonnage Frequency) MPEG-2.
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Encodeur audio Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106538626"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a><span data-ttu-id="4eb8b-103">Encodeur audio Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4eb8b-103">Microsoft MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="4eb8b-104">Le filtre d’encodeur audio Microsoft MPEG-2 encode les couches audio MPEG-1 et II, y compris la prise en charge des extensions LSF (Low échantillonnage Frequency) MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-104">The Microsoft MPEG-2 Audio Encoder filter encodes MPEG-1 audio layers I and II, including support for the MPEG-2 Low Sampling Frequency (LSF) extensions.</span></span>

<span data-ttu-id="4eb8b-105">Pour encoder et multiplexer des flux audio/vidéo, utilisez le filtre d' [**encodeur Microsoft MPEG-2**](microsoft-mpeg-2-encoder.md) , qui encapsule les fonctions de ce filtre et du filtre d' [**encodeur vidéo Microsoft MPEG-2**](microsoft-mpeg-2-video-encoder.md) .</span><span class="sxs-lookup"><span data-stu-id="4eb8b-105">To encode and multiplex audio/video streams, use the [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) filter, which encapsulates the functions of both this filter and the [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="4eb8b-106">Ce filtre n’est pas pris en charge sur les plateformes IA-64.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="4eb8b-107">Informations de filtre</span><span class="sxs-lookup"><span data-stu-id="4eb8b-107">Filter Information</span></span>

<span data-ttu-id="4eb8b-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="4eb8b-108">Filter Interfaces</span></span>

[<span data-ttu-id="4eb8b-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="4eb8b-110">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-110">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="4eb8b-111">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-111">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="4eb8b-112">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-112">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="4eb8b-113">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-113">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="4eb8b-114">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="4eb8b-114">Input Pin Media Types</span></span>

<span data-ttu-id="4eb8b-115">**MediaType \_ Audio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-115">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="4eb8b-116">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="4eb8b-116">Input Pin Interfaces</span></span>

[<span data-ttu-id="4eb8b-117">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-117">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="4eb8b-118">**IPin**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-118">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="4eb8b-119">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-119">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="4eb8b-120">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="4eb8b-120">Output Pin Media Types</span></span>

<span data-ttu-id="4eb8b-121">**MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-121">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="4eb8b-122">**MediaType \_ Flux**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-122">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="4eb8b-123">**MediaType \_ Stream**, **\_ \_ programme MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-123">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span><br/> <span data-ttu-id="4eb8b-124">**MediaType \_ Flux**, **\_ \_ transport MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-124">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span><br/>

<span data-ttu-id="4eb8b-125">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="4eb8b-125">Output Pin Interfaces</span></span>

[<span data-ttu-id="4eb8b-126">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-126">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="4eb8b-127">**IPin**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-127">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="4eb8b-128">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-128">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="4eb8b-129">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="4eb8b-129">Filter CLSID</span></span>

<span data-ttu-id="4eb8b-130">**CLSID \_ CMPEG2EncoderAudioDS** (déclaré dans wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="4eb8b-130">**CLSID\_CMPEG2EncoderAudioDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="4eb8b-131">Exécutable</span><span class="sxs-lookup"><span data-stu-id="4eb8b-131">Executable</span></span>

<span data-ttu-id="4eb8b-132">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="4eb8b-132">msmpeg2enc.dll</span></span>

[<span data-ttu-id="4eb8b-133">Mérite</span><span class="sxs-lookup"><span data-stu-id="4eb8b-133">Merit</span></span>](merit.md)

<span data-ttu-id="4eb8b-134">**MÉRITE \_ n' \_ \_ utilise pas**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-134">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="4eb8b-135">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="4eb8b-135">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="4eb8b-136">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-136">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="4eb8b-137">Notes</span><span class="sxs-lookup"><span data-stu-id="4eb8b-137">Remarks</span></span>

<span data-ttu-id="4eb8b-138">L’encodeur audio MPEG-2 peut générer les types de sortie suivants :</span><span class="sxs-lookup"><span data-stu-id="4eb8b-138">The MPEG-2 Audio Encoder can produce the following kinds of output:</span></span>

-   <span data-ttu-id="4eb8b-139">Flux élémentaire audio</span><span class="sxs-lookup"><span data-stu-id="4eb8b-139">Audio elementary stream</span></span>
-   <span data-ttu-id="4eb8b-140">Audio dans un flux de programme MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4eb8b-140">Audio in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="4eb8b-141">Audio dans un flux de transport MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4eb8b-141">Audio in an MPEG-2 transport stream</span></span>

<span data-ttu-id="4eb8b-142">Il prend en charge les couches MPEG-1 I et II et les extensions LSF (Low échantillonnage Frequency) MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4eb8b-142">It supports MPEG-1 layers I and II and MPEG-2 low sampling frequency (LSF) extensions</span></span>

<span data-ttu-id="4eb8b-143">Les échantillons d’entrée doivent être de 16 bits par échantillon, avec un taux d’échantillonnage audio de 48, 44,1, 32, 22,05 ou 16 KHz.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-143">Input samples must 16 bits per sample, with an audio sampling rate of 48, 44.1, 32, 22.05, or 16 KHz.</span></span> <span data-ttu-id="4eb8b-144">L’encodeur ne peut pas rééchantillonner le flux audio. l’audio encodé présente le même taux d’échantillonnage que l’entrée.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-144">The encoder cannot resample the audio stream; the encoded audio has the same sample rate as the input.</span></span>

<span data-ttu-id="4eb8b-145">Les échantillons d’entrée doivent être mono ou stéréo.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-145">Input samples must be mono or stereo.</span></span> <span data-ttu-id="4eb8b-146">L’audio encodé a le nombre de canaux comme entrée.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-146">The encoded audio has the number of channels as the input.</span></span>

### <a name="limitations"></a><span data-ttu-id="4eb8b-147">Limites</span><span class="sxs-lookup"><span data-stu-id="4eb8b-147">Limitations</span></span>

<span data-ttu-id="4eb8b-148">L’encodeur ne prend pas en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4eb8b-148">The encoder does not support the following:</span></span>

-   <span data-ttu-id="4eb8b-149">Séquences binaires audio MPEG Layer III.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-149">MPEG layer III audio bitstreams.</span></span>
-   <span data-ttu-id="4eb8b-150">Flux de bits d’extension multicanaux MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-150">MPEG-2 multi-channel extension bitstreams.</span></span>
-   <span data-ttu-id="4eb8b-151">Flux de bits AAC MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-151">MPEG-4 AAC bitstreams.</span></span>
-   <span data-ttu-id="4eb8b-152">Flux de bits MPEG-2 NBC (non-backward compatible).</span><span class="sxs-lookup"><span data-stu-id="4eb8b-152">MPEG-2 non-backward compatible (NBC) bitstreams.</span></span>
-   <span data-ttu-id="4eb8b-153">Génération de paquets d’extension de flux élémentaires (PES) paquets.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-153">Generation of packetized elementary stream (PES) packets.</span></span>
-   <span data-ttu-id="4eb8b-154">Encodage Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-154">Dolby Digital encoding.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="4eb8b-155">Propriétés du codec</span><span class="sxs-lookup"><span data-stu-id="4eb8b-155">Codec Properties</span></span>

<span data-ttu-id="4eb8b-156">Le filtre prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="4eb8b-156">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>

-   [<span data-ttu-id="4eb8b-157">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-157">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)
-   [<span data-ttu-id="4eb8b-158">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-158">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)
-   [<span data-ttu-id="4eb8b-159">**AVEncAudioIntervalToEncode**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-159">**AVEncAudioIntervalToEncode**</span></span>](avencaudiointervaltoencode-property.md)
-   [<span data-ttu-id="4eb8b-160">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-160">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
-   [<span data-ttu-id="4eb8b-161">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-161">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="4eb8b-162">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-162">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)
-   [<span data-ttu-id="4eb8b-163">**AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-163">**AVEncMPACopyright**</span></span>](avencmpacopyright-property.md)
-   [<span data-ttu-id="4eb8b-164">**AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-164">**AVEncMPAEmphasisType**</span></span>](avencmpaemphasistype-property.md)
-   [<span data-ttu-id="4eb8b-165">**AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-165">**AVEncMPAEnableRedundancyProtection**</span></span>](avencmpaenableredundancyprotection-property.md)
-   [<span data-ttu-id="4eb8b-166">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-166">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
-   [<span data-ttu-id="4eb8b-167">**AVEncMPAOriginalBitstream**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-167">**AVEncMPAOriginalBitstream**</span></span>](avencmpaoriginalbitstream-property.md)
-   [<span data-ttu-id="4eb8b-168">**AVEncMPAPrivateUserBit**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-168">**AVEncMPAPrivateUserBit**</span></span>](avencmpaprivateuserbit-property.md)

> [!Note]  
> <span data-ttu-id="4eb8b-169">Une version antérieure de la documentation répertorie de manière incorrecte des propriétés supplémentaires qui ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-169">An earlier version of the documentation incorrectly listed some additional properties that are not supported.</span></span>

 

<span data-ttu-id="4eb8b-170">Pour la compatibilité descendante, le filtre prend en charge la propriété suivante par le biais de l’interface **IEncoderAPI** :</span><span class="sxs-lookup"><span data-stu-id="4eb8b-170">For backward compatibility, the filter supports the following property through the **IEncoderAPI** interface:</span></span>



| <span data-ttu-id="4eb8b-171">Propriété</span><span class="sxs-lookup"><span data-stu-id="4eb8b-171">Property</span></span>                 | <span data-ttu-id="4eb8b-172">Description</span><span class="sxs-lookup"><span data-stu-id="4eb8b-172">Description</span></span>                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4eb8b-173">**\_débit binaire ENCAPIPARAM**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-173">**ENCAPIPARAM\_BITRATE**</span></span> | <span data-ttu-id="4eb8b-174">Équivalent à [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span><span class="sxs-lookup"><span data-stu-id="4eb8b-174">Equivalent to [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span></span> |



 

<span data-ttu-id="4eb8b-175">Il est recommandé de définir des propriétés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="4eb8b-175">It is recommended to set properties in the following order:</span></span>

1.  [<span data-ttu-id="4eb8b-176">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-176">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
2.  [<span data-ttu-id="4eb8b-177">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-177">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
3.  [<span data-ttu-id="4eb8b-178">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-178">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
4.  [<span data-ttu-id="4eb8b-179">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-179">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)

<span data-ttu-id="4eb8b-180">Définissez les propriétés restantes dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="4eb8b-180">Set the remaining properties in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb8b-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4eb8b-181">Requirements</span></span>



| <span data-ttu-id="4eb8b-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4eb8b-182">Requirement</span></span> | <span data-ttu-id="4eb8b-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="4eb8b-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb8b-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4eb8b-184">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb8b-185">Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, Windows 7 Édition familiale Premium, Windows 7 professionnel, Windows 7 entreprise, applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4eb8b-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4eb8b-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4eb8b-186">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb8b-187">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4eb8b-187">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="4eb8b-188">En-tête</span><span class="sxs-lookup"><span data-stu-id="4eb8b-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb8b-189"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb8b-189"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="4eb8b-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4eb8b-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb8b-191">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="4eb8b-191">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="4eb8b-192">**Types de média du démultiplexeur MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="4eb8b-192">**MPEG-2 Demultiplexer Media Types**</span></span>](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
