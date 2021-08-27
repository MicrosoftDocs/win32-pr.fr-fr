---
description: Conversions de type de média
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversions de type de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5d91844a062d5d4a1aa98af1a2e77c9cabfadb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474345"
---
# <a name="media-type-conversions"></a>Conversions de type de média

il est parfois nécessaire de procéder à une conversion entre les types de média Media Foundation et les anciennes structures de type de média à partir de DirectShow ou du kit de développement logiciel (SDK) de Format Windows media.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>D’une structure de format à un type de Media Foundation

Les fonctions suivantes initialisent un type de média Media Foundation à partir d’une structure de format. Ces fonctions sont également utiles si un flux de données ou un en-tête de fichier contient une structure de format. Par exemple, l’en-tête de fichier pour les fichiers audio WAVE contient une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .




| Structure à convertir | Fonction | 
|----------------------|----------|
| <a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br /><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (objets multimédia DirectX) <br /><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (kit de développement logiciel (SDK) Windows MEDIA Format) <br /><blockquote>[!Note]<br />Ces structures sont équivalentes.</blockquote><br /><br /> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a> | 
| <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a> | 
| <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a> | 
| <a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> ou <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a> | 




 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>D’un type de Media Foundation à une structure de format

Les fonctions suivantes permettent de créer ou d’initialiser une structure de format à partir d’un type de média Media Foundation.



| Fonction                                                                             | Structure cible                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**Am \_ \_Type de média**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**\_type de média am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MFCreateMFVideoFormatFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ou [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**\_type de média am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Mappages de format

Les tableaux suivants répertorient les attributs de Media Foundation qui correspondent à différentes structures de format. Tous ces attributs ne peuvent pas être traduits directement. Pour effectuer des conversions, vous devez utiliser les fonctions listées dans la section précédente. ces tables sont fournies principalement à des fins de référence.

### <a name="am_media_type"></a>\_type de média am \_



| Membre                   | Attribut                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **bTemporalCompression** | [**MF \_ MT \_ tous les \_ exemples \_ indépendants**](mf-mt-all-samples-independent-attribute.md) |
| **bFixedSizeSamples**    | [**\_exemples de \_ \_ taille fixe \_ MF MF**](mf-mt-fixed-size-samples-attribute.md)           |
| **lSampleSize**          | [**taille de l’échantillon MF MF \_ \_ \_**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>WAVEFORMATEX, WAVEFORMATEXTENSIBLE



| Membre                  | Attribut                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wFormatTag**          | [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)<br/> Si **wFormatTag** est \_ un format Wave \_ extensible, le sous-type se trouve dans le membre **subformat** .<br/> |
| **nChannels**           | [**\_canaux de \_ \_ numéros audio MF MT \_**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nSamplesPerSec**      | [**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **nAvgBytesPerSec**     | [**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**\_alignement de \_ \_ bloc audio MF MT \_**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wBitsPerSample**      | [**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wValidBitsPerSample** | [**\_bits de \_ sortie audio MF- \_ octets valides \_ \_ par \_ exemple**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wSamplesPerBlock**    | [**\_ \_ échantillons audio MF \_ MT \_ par \_ bloc**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwChannelMask**       | [**\_masque de \_ \_ canal audio MF MT \_**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **SubFormat**           | [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Données supplémentaires              | [**\_ \_ données utilisateur MF \_ MT**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>VIDEOINFOHEADER, VIDEOINFOHEADER2



| Membre                                         | Attribut                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwBitRate**                                  | [**\_vitesse de \_ \_ transmission moy. MF**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwBitErrorRate**                             | [**\_taux d' \_ \_ erreur de bits Moy \_ \_ . MF**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **AvgTimePerFrame**                            | [**MF \_ \_ \_ Fréquence d’images MT**](mf-mt-frame-rate-attribute.md); utilisez [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) pour calculer cette valeur.                                                                             |
| **dwInterlaceFlags**                           | [**\_ \_ mode entrelacé MF-MT \_**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwCopyProtectFlags**                         | Aucun équivalent défini                                                                                                                                                                                                                            |
| **dwPictAspectRatioX**, **dwPictAspectRatioY** | [**MF \_ Proportions de \_ pixels MT \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md); doit passer des proportions d’image aux proportions d’image.                                                                                                      |
| **dwControlFlags**                             | [**MF \_ \_indicateurs de \_ contrôle \_ du PAD MT**](mf-mt-pad-control-flags-attribute.md). Si l’indicateur **AMCONTROL \_ COLORINFO \_ présent** est présent, définissez les attributs de couleur étendus décrits dans [informations sur la couleur étendue](extended-color-information.md). |
| **bmiHeader. bilargeur**, **BmiHeader. bihauteur**  | [**\_taille de \_ trame MF MF \_**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiHeader.biBitCount**                       | Implicite dans le sous-type ([**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **bmiHeader. bicompression**                    | Implicite dans le sous-type.                                                                                                                                                                                                                         |
| **bmiHeader.biSizeImage**                      | [**taille de l’échantillon MF MF \_ \_ \_**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Informations sur la palette                            | [**\_palette MF MT \_**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Les attributs suivants peuvent être déduits à partir de la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , mais ils nécessitent également une connaissance des détails de format. Par exemple, différents formats YUV ont des exigences Stride différentes.

-   [**\_Stride MT \_ par défaut \_**](mf-mt-default-stride-attribute.md)
-   [**\_ouverture de \_ l' \_ affichage \_ de la version MF**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Membre                                   | Attribut                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**                      | [**\_code d' \_ heure de début du MPEG MF MT \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bSequenceHeader**                      | [**\_ \_ \_ en-tête de séquence MPEG MF MT \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **biXPelsPerMeter**, **biYPelsPerMeter** | [**\_ \_ \_ rapport hauteur/largeur des pixels \_ MF**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Membre               | Attribut                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**  | [**\_code d' \_ heure de début du MPEG MF MT \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwSequenceHeader** | [**\_ \_ \_ en-tête de séquence MPEG MF MT \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwProfile**        | [**\_Profil de \_ MPEG2 \_ MT pour MF**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwLevel**          | [**\_ \_ Niveau MPEG2 MT \_ MPEG2**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**\_ \_ Indicateurs MPEG2 MT \_ MPEG2**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Exemples

Le code suivant remplit une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) à partir d’un type de média vidéo. Notez que ces conversions perdent certaines des informations de format (entrelacement, fréquence d’images, données de couleur étendues). Toutefois, il peut être utile lors de l’enregistrement d’une image bitmap à partir d’une image vidéo, par exemple.


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 
