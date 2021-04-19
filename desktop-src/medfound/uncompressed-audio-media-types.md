---
description: Types de média audio non compressés
ms.assetid: 130a18a9-1c86-4d16-a8ae-ed57bf50f9bb
title: Types de média audio non compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d15f7211ef16d4280476f93744650b88742073
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525791"
---
# <a name="uncompressed-audio-media-types"></a><span data-ttu-id="3c2c0-103">Types de média audio non compressés</span><span class="sxs-lookup"><span data-stu-id="3c2c0-103">Uncompressed Audio Media Types</span></span>

<span data-ttu-id="3c2c0-104">Pour créer un type audio non compressé complet, définissez au moins les attributs suivants sur le pointeur d’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="3c2c0-104">To create a complete uncompressed audio type, set at least the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="3c2c0-105">Attribut</span><span class="sxs-lookup"><span data-stu-id="3c2c0-105">Attribute</span></span>                                                                                    | <span data-ttu-id="3c2c0-106">Description</span><span class="sxs-lookup"><span data-stu-id="3c2c0-106">Description</span></span>                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c2c0-107">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-107">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="3c2c0-108">Type principal.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-108">Major type.</span></span> <span data-ttu-id="3c2c0-109">Définissez sur MFMediaType \_ audio.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-109">Set to MFMediaType\_Audio.</span></span>                                                                                       |
| [<span data-ttu-id="3c2c0-110">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-110">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="3c2c0-111">Sous-type.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-111">Subtype.</span></span> <span data-ttu-id="3c2c0-112">Consultez [GUID de sous-type audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3c2c0-112">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>                                                                 |
| [<span data-ttu-id="3c2c0-113">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-113">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="3c2c0-114">Nombre de canaux audio.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-114">Number of audio channels.</span></span>                                                                                                    |
| [<span data-ttu-id="3c2c0-115">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-115">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="3c2c0-116">Nombre d’échantillons audio par seconde.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-116">Number of audio samples per second.</span></span>                                                                                          |
| [<span data-ttu-id="3c2c0-117">**\_alignement de \_ \_ bloc audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-117">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="3c2c0-118">Alignement de bloc.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-118">Block alignment.</span></span>                                                                                                             |
| [<span data-ttu-id="3c2c0-119">**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-119">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="3c2c0-120">Nombre moyen d’octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-120">Average number of bytes per second.</span></span>                                                                                          |
| [<span data-ttu-id="3c2c0-121">**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-121">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="3c2c0-122">Nombre de bits par échantillon audio.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-122">Number of bits per audio sample.</span></span>                                                                                             |
| [<span data-ttu-id="3c2c0-123">**MF \_ MT \_ tous les \_ exemples \_ indépendants**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-123">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="3c2c0-124">Spécifie si chaque échantillon audio est indépendant.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-124">Specifies whether each audio sample is independent.</span></span> <span data-ttu-id="3c2c0-125">Affectez la valeur **true** pour les \_ formats MFAudioFormat PCM et MFAudioFormat \_ float.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-125">Set to **TRUE** for MFAudioFormat\_PCM and MFAudioFormat\_Float formats.</span></span> |



 

<span data-ttu-id="3c2c0-126">En outre, les attributs suivants sont requis pour certains formats audio.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-126">In addition, the following attributes are required for some audio formats.</span></span>



| <span data-ttu-id="3c2c0-127">Attribut</span><span class="sxs-lookup"><span data-stu-id="3c2c0-127">Attribute</span></span>                                                                                      | <span data-ttu-id="3c2c0-128">Description</span><span class="sxs-lookup"><span data-stu-id="3c2c0-128">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c2c0-129">**\_bits de \_ sortie audio MF- \_ octets valides \_ \_ par \_ exemple**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-129">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md) | <span data-ttu-id="3c2c0-130">Nombre de bits de données audio valides dans chaque exemple audio.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-130">Number of valid bits of audio data in each audio sample.</span></span> <span data-ttu-id="3c2c0-131">Définissez cet attribut si les exemples audio ont un remplissage, c’est-à-dire si le nombre de bits valides dans chaque échantillon audio est inférieur à la taille de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-131">Set this attribute if the audio samples have padding—that is, if the number of valid bits in each audio sample is less than the sample size.</span></span> |
| [<span data-ttu-id="3c2c0-132">**\_masque de \_ \_ canal audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="3c2c0-132">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                     | <span data-ttu-id="3c2c0-133">L’attribution de canaux audio aux positions des orateurs.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-133">The assignment of audio channels to speaker positions.</span></span> <span data-ttu-id="3c2c0-134">Définissez cet attribut pour les flux audio multicanaux, par exemple 5,1.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-134">Set this attribute for multichannel audio streams, such as 5.1.</span></span> <span data-ttu-id="3c2c0-135">Cet attribut n’est pas requis pour l’audio mono ou stéréo.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-135">This attribute is not required for mono or stereo audio.</span></span>                       |



 

### <a name="example-code"></a><span data-ttu-id="3c2c0-136">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="3c2c0-136">Example Code</span></span>

<span data-ttu-id="3c2c0-137">Le code suivant montre comment créer un type de média pour un fichier audio PCM non compressé.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-137">The following code shows how to create a media type for uncompressed PCM audio.</span></span>


```C++
HRESULT CreatePCMAudioType(
    UINT32 sampleRate,        // Samples per second
    UINT32 bitsPerSample,     // Bits per sample
    UINT32 cChannels,         // Number of channels
    IMFMediaType **ppType     // Receives a pointer to the media type.
    )
{
    HRESULT hr = S_OK;

    IMFMediaType *pType = NULL;

    // Calculate derived values.
    UINT32 blockAlign = cChannels * (bitsPerSample / 8);
    UINT32 bytesPerSecond = blockAlign * sampleRate;

    // Create the empty media type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set attributes on the type.
    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_NUM_CHANNELS, cChannels);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_SAMPLES_PER_SECOND, sampleRate);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, blockAlign);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_AVG_BYTES_PER_SECOND, bytesPerSecond);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_AUDIO_BITS_PER_SAMPLE, bitsPerSample);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the type to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="3c2c0-138">L’exemple suivant utilise un format audio encodé comme entrée et crée un type audio PCM correspondant.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-138">The next example takes an encoded audio format as input, and creates a matching PCM audio type.</span></span> <span data-ttu-id="3c2c0-139">Ce type peut être défini sur un encodeur ou un décodeur, par exemple.</span><span class="sxs-lookup"><span data-stu-id="3c2c0-139">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
//-------------------------------------------------------------------
// ConvertAudioTypeToPCM
//
// Given an audio media type (which might describe a compressed audio
// format), returns a media type that describes the equivalent
// uncompressed PCM format.
//-------------------------------------------------------------------

HRESULT ConvertAudioTypeToPCM(
    IMFMediaType *pType,        // Pointer to an encoded audio type.
    IMFMediaType **ppType       // Receives a matching PCM audio type.
    )
{
    HRESULT hr = S_OK;

    GUID majortype = { 0 };
    GUID subtype = { 0 };

    UINT32 cChannels = 0;
    UINT32 samplesPerSec = 0;
    UINT32 bitsPerSample = 0;

    hr = pType->GetMajorType(&majortype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (majortype != MFMediaType_Audio)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Get the audio subtype.
    hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
    if (FAILED(hr)) 
    { 
        return hr;
    }

    if (subtype == MFAudioFormat_PCM)
    {
        // This is already a PCM audio type. Return the same pointer.

        *ppType = pType;
        (*ppType)->AddRef();

        return S_OK;
    }

    // Get the sample rate and other information from the audio format.

    cChannels = MFGetAttributeUINT32(pType, MF_MT_AUDIO_NUM_CHANNELS, 0);
    samplesPerSec = MFGetAttributeUINT32(pType, MF_MT_AUDIO_SAMPLES_PER_SECOND, 0);
    bitsPerSample = MFGetAttributeUINT32(pType, MF_MT_AUDIO_BITS_PER_SAMPLE, 16);

    // Note: Some encoded audio formats do not contain a value for bits/sample.
    // In that case, use a default value of 16. Most codecs will accept this value.

    if (cChannels == 0 || samplesPerSec == 0)
    {
        return MF_E_INVALIDTYPE;
    }

    // Create the corresponding PCM audio type.
    hr = CreatePCMAudioType(samplesPerSec, bitsPerSample, cChannels, ppType);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3c2c0-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c2c0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c2c0-141">Types de média audio</span><span class="sxs-lookup"><span data-stu-id="3c2c0-141">Audio Media Types</span></span>](audio-media-types.md)
</dt> </dl>

 

 



