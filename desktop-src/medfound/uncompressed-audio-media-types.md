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
# <a name="uncompressed-audio-media-types"></a>Types de média audio non compressés

Pour créer un type audio non compressé complet, définissez au moins les attributs suivants sur le pointeur d’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .



| Attribut                                                                                    | Description                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                                    | Type principal. Définissez sur MFMediaType \_ audio.                                                                                       |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                           | Sous-type. Consultez [GUID de sous-type audio](audio-subtype-guids.md).                                                                 |
| [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)                   | Nombre de canaux audio.                                                                                                    |
| [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md)      | Nombre d’échantillons audio par seconde.                                                                                          |
| [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)             | Alignement de bloc.                                                                                                             |
| [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md) | Nombre moyen d’octets par seconde.                                                                                          |
| [**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md)            | Nombre de bits par échantillon audio.                                                                                             |
| [**MF \_ MT \_ tous les \_ exemples \_ indépendants**](mf-mt-all-samples-independent-attribute.md)         | Spécifie si chaque échantillon audio est indépendant. Affectez la valeur **true** pour les \_ formats MFAudioFormat PCM et MFAudioFormat \_ float. |



 

En outre, les attributs suivants sont requis pour certains formats audio.



| Attribut                                                                                      | Description                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_bits de \_ sortie audio MF- \_ octets valides \_ \_ par \_ exemple**](mf-mt-audio-valid-bits-per-sample-attribute.md) | Nombre de bits de données audio valides dans chaque exemple audio. Définissez cet attribut si les exemples audio ont un remplissage, c’est-à-dire si le nombre de bits valides dans chaque échantillon audio est inférieur à la taille de l’échantillon. |
| [**\_masque de \_ \_ canal audio MF MT \_**](mf-mt-audio-channel-mask-attribute.md)                     | L’attribution de canaux audio aux positions des orateurs. Définissez cet attribut pour les flux audio multicanaux, par exemple 5,1. Cet attribut n’est pas requis pour l’audio mono ou stéréo.                       |



 

### <a name="example-code"></a>Exemple de code

Le code suivant montre comment créer un type de média pour un fichier audio PCM non compressé.


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



L’exemple suivant utilise un format audio encodé comme entrée et crée un type audio PCM correspondant. Ce type peut être défini sur un encodeur ou un décodeur, par exemple.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de média audio](audio-media-types.md)
</dt> </dl>

 

 



