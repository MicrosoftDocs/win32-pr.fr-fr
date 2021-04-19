---
description: 'Ce filtre décode les formats audio suivants :'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Décodeur audio Microsoft MPEG-1/DD/AAC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514080"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a><span data-ttu-id="2bd09-103">Décodeur audio Microsoft MPEG-1/DD/AAC</span><span class="sxs-lookup"><span data-stu-id="2bd09-103">Microsoft MPEG-1/DD/AAC Audio Decoder</span></span>

<span data-ttu-id="2bd09-104">Ce filtre décode les formats audio suivants :</span><span class="sxs-lookup"><span data-stu-id="2bd09-104">This filter decodes the following audio formats:</span></span>

-   <span data-ttu-id="2bd09-105">Couches audio MPEG-1 I et II.</span><span class="sxs-lookup"><span data-stu-id="2bd09-105">MPEG-1 audio layers I and II.</span></span>
-   <span data-ttu-id="2bd09-106">MPEG-2 audio à compatibilité descendante, couches I et II (ISO/IEC 13818-3), mono et stéréo uniquement.</span><span class="sxs-lookup"><span data-stu-id="2bd09-106">Backward-compatible MPEG-2 audio, layers I and II (ISO/IEC 13818-3), mono and stereo only.</span></span>
-   <span data-ttu-id="2bd09-107">Profil du codage audio avancé (AAC) faible.</span><span class="sxs-lookup"><span data-stu-id="2bd09-107">Advanced Audio Coding (AAC) Low Complexity (LC) profile.</span></span>
-   <span data-ttu-id="2bd09-108">High-Efficiency AAC (HE-AAC) version 1 et version 2.</span><span class="sxs-lookup"><span data-stu-id="2bd09-108">High-Efficiency AAC (HE-AAC) version 1 and version 2.</span></span>
-   <span data-ttu-id="2bd09-109">Systèmes de cinéma numérique direct (DTS) pour la sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="2bd09-109">Pass-through Digital Theater Systems (DTS) for digital output.</span></span>
-   <span data-ttu-id="2bd09-110">LPCM, mono et stéréo uniquement, avec ou sans en-têtes PES.</span><span class="sxs-lookup"><span data-stu-id="2bd09-110">LPCM, mono and stereo only, with or without PES headers.</span></span>
-   <span data-ttu-id="2bd09-111">Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="2bd09-111">Dolby Digital.</span></span>
-   <span data-ttu-id="2bd09-112">Dolby Digital plus, y compris la conversion de Dolby Digital plus en Dolby Digital pour la sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="2bd09-112">Dolby Digital Plus, including conversion from Dolby Digital Plus to Dolby Digital for digital output.</span></span>

> [!Note]  
> <span data-ttu-id="2bd09-113">L’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2bd09-113">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="2bd09-114">Ce filtre n’est pas pris en charge sur les plateformes IA-64.</span><span class="sxs-lookup"><span data-stu-id="2bd09-114">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="2bd09-115">Le décodage des formats Dolby Digital plus, AAC et HE-AAC requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2bd09-115">Decoding of Dolby Digital Plus, AAC, and HE-AAC formats requires Windows 7.</span></span> <span data-ttu-id="2bd09-116">Le décodage de Dolby Digital ou Dolby Digital plus n’est pas pris en charge sur Windows 7 édition familial Basic ou Windows 7 Édition Starter.</span><span class="sxs-lookup"><span data-stu-id="2bd09-116">Decoding of Dolby Digital or Dolby Digital Plus is not supported on Windows 7 Home Basic or Windows 7 Starter.</span></span>

<span data-ttu-id="2bd09-117">Dans le registre, le nom convivial de ce filtre est « Microsoft DTV-DVD audio décoder ».</span><span class="sxs-lookup"><span data-stu-id="2bd09-117">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Audio Decoder".</span></span>



<span data-ttu-id="2bd09-118">Informations de filtre</span><span class="sxs-lookup"><span data-stu-id="2bd09-118">Filter Information</span></span>

<span data-ttu-id="2bd09-119">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="2bd09-119">Filter Interfaces</span></span>

[<span data-ttu-id="2bd09-120">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="2bd09-120">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="2bd09-121">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2bd09-121">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="2bd09-122">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="2bd09-122">Input Pin Media Types</span></span>

<span data-ttu-id="2bd09-123">Dans Windows Vista et versions ultérieures, le filtre prend en charge les types d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="2bd09-123">In Windows Vista and later, the filter supports the following input types:</span></span><br/>

-   <span data-ttu-id="2bd09-124">**MediaType \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3** (voir la remarque 1.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-124">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="2bd09-125">**MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-125">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="2bd09-126">**MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG1Payload**</span><span class="sxs-lookup"><span data-stu-id="2bd09-126">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Payload**</span></span>
-   <span data-ttu-id="2bd09-127">**MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-127">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="2bd09-128">**MediaType \_ \_ \_ Pack chiffré de DVD**, **MEDIASUBTYPE \_ Dolby \_ AC3** (voir la remarque 1.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-128">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="2bd09-129">**MediaType \_ \_ \_ Pack chiffré de DVD**, **MEDIASUBTYPE \_ DTS** (voir la remarque 2.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-129">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="2bd09-130">**MediaType \_ \_ \_ Pack chiffré DVD**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-130">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="2bd09-131">**MediaType \_ \_ \_ Pack chiffré DVD**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-131">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="2bd09-132">**MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ Dolby \_ AC3** (voir la remarque 1.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-132">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="2bd09-133">**MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DTS** (voir la remarque 2.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-133">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="2bd09-134">**MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-134">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="2bd09-135">**MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-135">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="2bd09-136">**MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3** (voir la remarque 1.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-136">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="2bd09-137">**MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-137">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="2bd09-138">**MediaType \_ Flux**, **MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-138">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>

<span data-ttu-id="2bd09-139">À compter de Windows 7, le filtre prend également en charge les types d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="2bd09-139">Starting in Windows 7, the filter also supports the following input types:</span></span><br/>

-   <span data-ttu-id="2bd09-140">**MediaType \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ DDplus** (voir la remarque 1.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-140">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="2bd09-141">**MediaType \_ Audio**, **MEDIASUBTYPE \_ DTS2** (voir la remarque 2.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-141">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DTS2** (See Note 2.)</span></span>
-   <span data-ttu-id="2bd09-142">**MediaType \_ Audio**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-142">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="2bd09-143">**MediaType \_ Audio**, **MEDIASUBTYPE \_ DVM** (voir la remarque 1.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-143">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVM** (See Note 1.)</span></span>
-   <span data-ttu-id="2bd09-144">**MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="2bd09-144">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="2bd09-145">**MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG \_ garantie**</span><span class="sxs-lookup"><span data-stu-id="2bd09-145">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>
-   <span data-ttu-id="2bd09-146">**MediaType \_ Audio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**</span><span class="sxs-lookup"><span data-stu-id="2bd09-146">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1AudioPayload**</span></span>
-   <span data-ttu-id="2bd09-147">**MediaType \_ Audio**, **MEDIASUBTYPE \_ RAW \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="2bd09-147">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_RAW\_AAC1**</span></span>
-   <span data-ttu-id="2bd09-148">**MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ DDplus** (voir la remarque 1.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="2bd09-149">**MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="2bd09-149">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="2bd09-150">**MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ garantie**</span><span class="sxs-lookup"><span data-stu-id="2bd09-150">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>

<span data-ttu-id="2bd09-151">Le type d’entrée peut changer dynamiquement pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="2bd09-151">The input type can change dynamically during streaming.</span></span><br/> <span data-ttu-id="2bd09-152">Pour plus d’informations sur ces types de médias, consultez [**sous-types audio**](audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="2bd09-152">For more information about these media types, see [**Audio Subtypes**](audio-subtypes.md).</span></span><br/>

> [!Note]  
> 1. <span data-ttu-id="2bd09-153">L’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2bd09-153">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

<br/>

> [!Note]  
> 2. <span data-ttu-id="2bd09-154">Pour l’entrée de systèmes de cinéma numérique (DTS), seule la sortie S/PDIF est prise en charge (DTS sur S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="2bd09-154">For Digital Theater Systems (DTS) input, only S/PDIF output is supported (DTS over S/PDIF).</span></span> <span data-ttu-id="2bd09-155">Le décodage audio n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2bd09-155">Audio decoding is not supported.</span></span>

<br/>

<span data-ttu-id="2bd09-156">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="2bd09-156">Input Pin Interfaces</span></span>

[<span data-ttu-id="2bd09-157">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2bd09-157">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="2bd09-158">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="2bd09-158">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="2bd09-159">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="2bd09-159">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="2bd09-160">**IPin**</span><span class="sxs-lookup"><span data-stu-id="2bd09-160">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="2bd09-161">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="2bd09-161">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="2bd09-162">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="2bd09-162">Output Pin Media Types</span></span>

<span data-ttu-id="2bd09-163">Dans Windows Vista et versions ultérieures, le filtre prend en charge les types de sortie suivants :</span><span class="sxs-lookup"><span data-stu-id="2bd09-163">In Windows Vista and later, the filter supports the following output types:</span></span><br/>

-   <span data-ttu-id="2bd09-164">**MediaType \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** (identique au sous- **\_ type KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital**)</span><span class="sxs-lookup"><span data-stu-id="2bd09-164">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3\_SPDIF** (same as **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL**)</span></span>
-   <span data-ttu-id="2bd09-165">**MediaType \_ Audio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="2bd09-165">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="2bd09-166">À compter de Windows 7, le filtre prend également en charge les types de sortie suivants :</span><span class="sxs-lookup"><span data-stu-id="2bd09-166">Starting in Windows 7, the filter also supports the following output types:</span></span><br/>

-   <span data-ttu-id="2bd09-167">**MediaType \_ Audio**, **\_ sous-type KSDATAFORMAT \_ IEC61937 \_ DTS**</span><span class="sxs-lookup"><span data-stu-id="2bd09-167">**MEDIATYPE\_Audio**, **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS**</span></span>
-   <span data-ttu-id="2bd09-168">**MediaType \_ Audio**, **MEDIASUBTYPE \_ IEEE \_ float**</span><span class="sxs-lookup"><span data-stu-id="2bd09-168">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_IEEE\_FLOAT**</span></span>

<span data-ttu-id="2bd09-169">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="2bd09-169">Output Pin Interfaces</span></span>

[<span data-ttu-id="2bd09-170">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="2bd09-170">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="2bd09-171">**IPin**</span><span class="sxs-lookup"><span data-stu-id="2bd09-171">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="2bd09-172">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="2bd09-172">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="2bd09-173">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="2bd09-173">Filter CLSID</span></span>

<span data-ttu-id="2bd09-174">**CLSID \_ CMPEG2AudDecoderDS** (déclaré dans wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="2bd09-174">**CLSID\_CMPEG2AudDecoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="2bd09-175">Exécutable</span><span class="sxs-lookup"><span data-stu-id="2bd09-175">Executable</span></span>

<span data-ttu-id="2bd09-176">msmpeg2adec.dll</span><span class="sxs-lookup"><span data-stu-id="2bd09-176">msmpeg2adec.dll</span></span>

[<span data-ttu-id="2bd09-177">Mérite</span><span class="sxs-lookup"><span data-stu-id="2bd09-177">Merit</span></span>](merit.md)

<span data-ttu-id="2bd09-178">**Mérite \_ NORMAL** -1</span><span class="sxs-lookup"><span data-stu-id="2bd09-178">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="2bd09-179">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="2bd09-179">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="2bd09-180">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="2bd09-180">**CLSID\_LegacyAmFilterCategory**</span></span>



 

> [!Note]  
> <span data-ttu-id="2bd09-181">Une version antérieure de la documentation indiquait que ce filtre peut décoder « audio MPEG-2 ».</span><span class="sxs-lookup"><span data-stu-id="2bd09-181">An earlier version of the documentation stated that this filter can decode "MPEG-2 audio."</span></span> <span data-ttu-id="2bd09-182">Le filtre décode uniquement le son MPEG-2 à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="2bd09-182">The filter decodes only backward-compatible MPEG-2 audio.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="2bd09-183">Notes</span><span class="sxs-lookup"><span data-stu-id="2bd09-183">Remarks</span></span>

<span data-ttu-id="2bd09-184">Les flux mono sont toujours décodés en stéréo.</span><span class="sxs-lookup"><span data-stu-id="2bd09-184">Mono streams are always decoded to stereo.</span></span>

<span data-ttu-id="2bd09-185">Pour les flux avec une configuration de canal de deux ou plusieurs haut-parleurs, le décodeur effectue l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2bd09-185">For streams with a channel configuration of two or more speakers, the decoder does one of the following:</span></span>

-   <span data-ttu-id="2bd09-186">Mixages jusqu’à six canaux, à l’aide de la configuration de l’orateur 5,1 courant.</span><span class="sxs-lookup"><span data-stu-id="2bd09-186">Up-mixes to six channels, using the common 5.1 speaker configuration.</span></span>
-   <span data-ttu-id="2bd09-187">Downmixes en stéréo.</span><span class="sxs-lookup"><span data-stu-id="2bd09-187">Downmixes to stereo.</span></span>

<span data-ttu-id="2bd09-188">Pour choisir entre ces deux options, utilisez l’interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) pour définir la propriété [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) , avant de connecter les broches.</span><span class="sxs-lookup"><span data-stu-id="2bd09-188">To select between these two options, use the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to set the [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property, before connecting the pins.</span></span> <span data-ttu-id="2bd09-189">En guise d’alternative, lorsque l’application génère le graphique de filtre, elle peut définir le type de média souhaité sur la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="2bd09-189">Alternatively, when the application builds the filter graph, it can set the desired media type on the output pin.</span></span>

### <a name="aac-decoding"></a><span data-ttu-id="2bd09-190">Décodage AAC</span><span class="sxs-lookup"><span data-stu-id="2bd09-190">AAC Decoding</span></span>

<span data-ttu-id="2bd09-191">Pour AAC, le décodeur a certaines contraintes de format sur l’entrée AAC compressée.</span><span class="sxs-lookup"><span data-stu-id="2bd09-191">For AAC, the decoder has certain format constraints on the compressed AAC input.</span></span> <span data-ttu-id="2bd09-192">Ces contraintes de format sont les mêmes que le [**décodeur Media Foundation AAC**](../medfound/aac-decoder.md)et sont documentées dans la section «[**contraintes de format**](../medfound/aac-decoder.md)».</span><span class="sxs-lookup"><span data-stu-id="2bd09-192">These format constraints are the same as the Media Foundation [**AAC Decoder**](../medfound/aac-decoder.md), and are documented in the section "[**Format Constraints**](../medfound/aac-decoder.md)".</span></span>

<span data-ttu-id="2bd09-193">Le décodeur DirectShow accepte également différents types d’entrée que le décodeur Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2bd09-193">The DirectShow decoder also accepts different input types than the Media Foundation decoder.</span></span> <span data-ttu-id="2bd09-194">Le décodeur DirectShow prend en charge les types d’entrée AAC suivants :</span><span class="sxs-lookup"><span data-stu-id="2bd09-194">The DirectShow decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="2bd09-195">**MEDIASUBTYPE \_ \_AAC1 brut**: AAC brut, généralement trouvé dans AVI ou Matroska (. MKV).</span><span class="sxs-lookup"><span data-stu-id="2bd09-195">**MEDIASUBTYPE\_RAW\_AAC1**: Raw AAC, typically found in AVI or Matroska (.MKV) files.</span></span>
-   <span data-ttu-id="2bd09-196">**MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**: AAC dans un flux de transport de données audio (ADTS) pour la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="2bd09-196">**MEDIASUBTYPE\_MPEG\_ADTS\_AAC**: AAC in an Audio Data Transport Stream (ADTS) for streaming.</span></span>
-   <span data-ttu-id="2bd09-197">**MEDIASUBTYPE \_ MPEG \_ garantie**: flux de transport avec une couche de synchronisation (garantie) et une couche multiplex (LATM).</span><span class="sxs-lookup"><span data-stu-id="2bd09-197">**MEDIASUBTYPE\_MPEG\_LOAS**: Transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span>

<span data-ttu-id="2bd09-198">Le décodeur Media Foundation prend en charge les types d’entrée AAC suivants :</span><span class="sxs-lookup"><span data-stu-id="2bd09-198">The Media Foundation decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="2bd09-199">MFAudioFormat \_ AAC (identique à **MEDIASUBTYPE \_ MPEG \_ HEAAC**) pour la lecture de fichiers MP4.</span><span class="sxs-lookup"><span data-stu-id="2bd09-199">MFAudioFormat\_AAC (same as **MEDIASUBTYPE\_MPEG\_HEAAC**) for MP4 file playback.</span></span>
-   <span data-ttu-id="2bd09-200">**MEDIASUBTYPE \_ \_AAC1 brut**.</span><span class="sxs-lookup"><span data-stu-id="2bd09-200">**MEDIASUBTYPE\_RAW\_AAC1**.</span></span>

### <a name="property-sets"></a><span data-ttu-id="2bd09-201">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="2bd09-201">Property Sets</span></span>

<span data-ttu-id="2bd09-202">La broche d’entrée du décodeur prend en charge les jeux de propriétés suivants via [**IKsPropertySet**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="2bd09-202">The decoder's input pin supports the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="2bd09-203">**Jeu de propriétés protection de copie de DVD**</span><span class="sxs-lookup"><span data-stu-id="2bd09-203">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="2bd09-204">[**Propriété rate-change définie**](rate-change-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="2bd09-204">[**Rate-Change Property Set**](rate-change-property-set.md).</span></span>

> [!Note]  
> <span data-ttu-id="2bd09-205">À partir de Windows 7, le décodeur prend en charge le mode d’astuce par le biais du jeu de propriétés rate-change.</span><span class="sxs-lookup"><span data-stu-id="2bd09-205">Starting in Windows 7, the decoder supports trick mode through the rate-change property set.</span></span> <span data-ttu-id="2bd09-206">Il prend en charge les vitesses de lecture dans la plage \[ 0,501 – 2,0 \] , où 1,0 est la vitesse de lecture normale et 2,0 est le double de la vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="2bd09-206">It supports playback rates in the range \[0.501 – 2.0\], where 1.0 is normal playback rate, and 2.0 is twice the normal rate.</span></span>

 

### <a name="codec-properties"></a><span data-ttu-id="2bd09-207">Propriétés du codec</span><span class="sxs-lookup"><span data-stu-id="2bd09-207">Codec Properties</span></span>

<span data-ttu-id="2bd09-208">La broche d’entrée du décodeur prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="2bd09-208">The decoder's input pin supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="2bd09-209">Propriété</span><span class="sxs-lookup"><span data-stu-id="2bd09-209">Property</span></span>                                                          | <span data-ttu-id="2bd09-210">Nécessite</span><span class="sxs-lookup"><span data-stu-id="2bd09-210">Requires</span></span>                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="2bd09-211">**AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="2bd09-211">**AVAudioChannelConfig**</span></span>](avaudiochannelconfig-property.md)     | <span data-ttu-id="2bd09-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-212">Windows Vista</span></span>                                            |
| [<span data-ttu-id="2bd09-213">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="2bd09-213">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)       | <span data-ttu-id="2bd09-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-214">Windows Vista</span></span>                                            |
| [<span data-ttu-id="2bd09-215">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="2bd09-215">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)           | <span data-ttu-id="2bd09-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-216">Windows Vista</span></span>                                            |
| [<span data-ttu-id="2bd09-217">**AVDDSurroundMode**</span><span class="sxs-lookup"><span data-stu-id="2bd09-217">**AVDDSurroundMode**</span></span>](avddsurroundmode-property.md)             | <span data-ttu-id="2bd09-218">Windows Vista uniquement ; non pris en charge dans Windows 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2bd09-218">Windows Vista only; not supported in Windows 7 or later.</span></span> |
| [<span data-ttu-id="2bd09-219">**AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="2bd09-219">**AVDecAudioDualMono**</span></span>](avdecaudiodualmono-property.md)         | <span data-ttu-id="2bd09-220">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-220">Windows Vista</span></span>                                            |
| [<span data-ttu-id="2bd09-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="2bd09-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md) | <span data-ttu-id="2bd09-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-222">Windows Vista</span></span>                                            |
| [<span data-ttu-id="2bd09-223">**AVDecCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="2bd09-223">**AVDecCommonMeanBitRate**</span></span>](avdeccommonmeanbitrate.md)          | <span data-ttu-id="2bd09-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2bd09-224">Windows 7</span></span>                                                |



 

<span data-ttu-id="2bd09-225">Le filtre prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="2bd09-225">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="2bd09-226">Propriété</span><span class="sxs-lookup"><span data-stu-id="2bd09-226">Property</span></span>                                                                          | <span data-ttu-id="2bd09-227">Nécessite</span><span class="sxs-lookup"><span data-stu-id="2bd09-227">Requires</span></span>      |
|-----------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="2bd09-228">**AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="2bd09-228">**AVDecAACDownmixMode**</span></span>](avdecaacdownmixmode-property.md)                       | <span data-ttu-id="2bd09-229">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2bd09-229">Windows 7</span></span>     |
| [<span data-ttu-id="2bd09-230">**AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="2bd09-230">**AVDecAudioDualMonoReproMode**</span></span>](avdecaudiodualmonorepromode-property.md)       | <span data-ttu-id="2bd09-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-231">Windows Vista</span></span> |
| <span data-ttu-id="2bd09-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (voir la remarque 3.)</span><span class="sxs-lookup"><span data-stu-id="2bd09-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (See Note 3.)</span></span> | <span data-ttu-id="2bd09-233">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-233">Windows Vista</span></span> |
| [<span data-ttu-id="2bd09-234">**AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="2bd09-234">**AVDecDDDynamicRangeScaleHigh**</span></span>](avdecdddynamicrangescalehigh-property.md)     | <span data-ttu-id="2bd09-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-235">Windows Vista</span></span> |
| [<span data-ttu-id="2bd09-236">**AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="2bd09-236">**AVDecDDDynamicRangeScaleLow**</span></span>](avdecdddynamicrangescalelow-property.md)       | <span data-ttu-id="2bd09-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-237">Windows Vista</span></span> |
| [<span data-ttu-id="2bd09-238">**AVDecDDOperationalMode**</span><span class="sxs-lookup"><span data-stu-id="2bd09-238">**AVDecDDOperationalMode**</span></span>](avdecddoperationalmode-property.md)                 | <span data-ttu-id="2bd09-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-239">Windows Vista</span></span> |
| [<span data-ttu-id="2bd09-240">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="2bd09-240">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                    | <span data-ttu-id="2bd09-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd09-241">Windows Vista</span></span> |
| [<span data-ttu-id="2bd09-242">**AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="2bd09-242">**AVDSPLoudnessEqualization**</span></span>](avdsploudnessequalization-property.md)           | <span data-ttu-id="2bd09-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2bd09-243">Windows 7</span></span>     |
| [<span data-ttu-id="2bd09-244">**AVDSPSpeakerFill**</span><span class="sxs-lookup"><span data-stu-id="2bd09-244">**AVDSPSpeakerFill**</span></span>](avdspspeakerfill-property.md)                             | <span data-ttu-id="2bd09-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2bd09-245">Windows 7</span></span>     |



 

> [!Note]  
> 3. <span data-ttu-id="2bd09-246">La propriété [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) doit être définie avant que la broche de sortie du décodeur soit connectée.</span><span class="sxs-lookup"><span data-stu-id="2bd09-246">The [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property must be set before the decoder's output pin is connected.</span></span> <span data-ttu-id="2bd09-247">Dans le cas contraire, la modification n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="2bd09-247">Otherwise, the change has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2bd09-248">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bd09-248">Requirements</span></span>



| <span data-ttu-id="2bd09-249">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bd09-249">Requirement</span></span> | <span data-ttu-id="2bd09-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bd09-250">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd09-251">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bd09-251">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd09-252">Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, applications de bureau Windows 7 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bd09-252">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2bd09-253">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bd09-253">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd09-254">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bd09-254">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2bd09-255">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bd09-255">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd09-256"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd09-256"><dt>Wmcodecdsp.h</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="2bd09-257">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bd09-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd09-258">**Sous-types audio**</span><span class="sxs-lookup"><span data-stu-id="2bd09-258">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="2bd09-259">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="2bd09-259">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="2bd09-260">**Types de supports DVD**</span><span class="sxs-lookup"><span data-stu-id="2bd09-260">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> </dl>

 

 
