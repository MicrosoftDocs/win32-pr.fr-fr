---
description: Types de médias vidéo non compressés
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: Types de médias vidéo non compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c90a48aed62f22a492ac22dae93761c1046750a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530489"
---
# <a name="uncompressed-video-media-types"></a>Types de médias vidéo non compressés

Cette rubrique explique comment créer un type de média qui décrit un format vidéo non compressé. Pour plus d’informations sur les types de médias, consultez [à propos des types de média](about-media-types.md).

Pour créer un type de vidéo non compressé complet, définissez les attributs suivants sur le pointeur d’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .



| Attribut                                                                            | Description                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                            | Type principal. Définissez sur **MFMediaType \_ Video**.                                                                                                                                                                                          |
| [**\_sous- \_ type MF MT**](mf-mt-subtype-attribute.md)                                   | Sous-type. Consultez [GUID de sous-type de vidéo](video-subtype-guids.md).                                                                                                                                                                        |
| [**\_Stride MT \_ par défaut \_**](mf-mt-default-stride-attribute.md)                    | STRIDE de surface. Le *Stride* est le nombre d’octets nécessaires pour passer d’une ligne de pixels à la suivante. Définissez cet attribut si le Stride en octets n’est pas le même que la largeur vidéo en octets. Sinon, vous pouvez omettre cet attribut. |
| [**\_fréquence d' \_ images MF MF \_**](mf-mt-frame-rate-attribute.md)                            | Fréquence d’images.                                                                                                                                                                                                                         |
| [**\_taille de \_ trame MF MF \_**](mf-mt-frame-size-attribute.md)                            | Taille du frame.                                                                                                                                                                                                                         |
| [**\_ \_ mode entrelacé MF-MT \_**](mf-mt-interlace-mode-attribute.md)                    | Mode entrelacement.                                                                                                                                                                                                                   |
| [**MF \_ MT \_ tous les \_ exemples \_ indépendants**](mf-mt-all-samples-independent-attribute.md) | Spécifie si chaque échantillon est indépendant. Affectez la valeur **true** pour les formats non compressés.                                                                                                                                             |
| [**\_ \_ \_ rapport hauteur/largeur des pixels \_ MF**](mf-mt-pixel-aspect-ratio-attribute.md)           | Proportions de pixels.                                                                                                                                                                                                                 |



 

En outre, définissez les attributs suivants si vous connaissez les valeurs correctes. (Sinon, omettez ces attributs.)



| Attribut                                                                    | Description        |
|------------------------------------------------------------------------------|--------------------|
| [**\_vidéos de \_ \_ réamorçage de la vidéo MF**](mf-mt-video-primaries-attribute.md)          | Couleurs primaires.   |
| [**\_fonction de \_ transfert MF-MF \_**](mf-mt-transfer-function-attribute.md)      | Fonction de transfert. |
| [**\_ \_ matrice YUV MT \_ YUV**](mf-mt-yuv-matrix-attribute.md)                    | Matrice de transfert.   |
| [**vidéo MF MT-présentation de \_ \_ \_ chrominance \_**](mf-mt-video-chroma-siting-attribute.md) | Emplacement de chrominance.     |
| [**\_ \_ plage nominale de vidéo MF MT \_ \_**](mf-mt-video-nominal-range-attribute.md) | Plage nominale.     |



 

Pour plus d’informations, consultez [informations sur les couleurs étendues](extended-color-information.md). Par exemple, si vous créez un type de média qui décrit une norme vidéo et que la norme définit l’emplacement de chrominance, ajoutez ces informations au type de média. Cela permet de préserver la fidélité des couleurs dans l’ensemble du pipeline.

Les fonctions suivantes peuvent être utiles lors de la création d’un type de média vidéo.



| Fonction                                                                     | Description                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | Calcule la fréquence d’images, en fonction de la durée de trame moyenne.                                                                                                                         |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | Calcule la taille de l’image pour un format vidéo non compressé.                                                                                                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | Calcule la durée moyenne d’une image vidéo, en fonction de la fréquence d’images.                                                                                                              |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | Retourne le Stride de surface minimal pour un format vidéo. Pour plus d’informations, consultez l' [image Stride](image-stride.md).                                                                   |
| [**MFInitVideoFormat**](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | Initialise une structure [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) pour certains formats vidéo standard, tels que la télévision NTSC. Vous pouvez ensuite utiliser la structure pour initialiser un type de média. |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | Interroge si un format vidéo est un format YUV.                                                                                                                                      |



 

## <a name="examples"></a>Exemples

Cet exemple montre une fonction qui remplit les informations les plus courantes pour un format vidéo non compressé. La fonction retourne un pointeur d’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Vous pouvez ensuite ajouter des attributs supplémentaires au type de média, si nécessaire.


```C++
HRESULT CreateUncompressedVideoType(
    DWORD                fccFormat,  // FOURCC or D3DFORMAT value.     
    UINT32               width, 
    UINT32               height,
    MFVideoInterlaceMode interlaceMode,
    const MFRatio&       frameRate,
    const MFRatio&       par,
    IMFMediaType         **ppType
    )
{
    if (ppType == NULL)
    {
        return E_POINTER;
    }

    GUID    subtype = MFVideoFormat_Base;
    LONG    lStride = 0;
    UINT    cbImage = 0;

    IMFMediaType *pType = NULL;

    // Set the subtype GUID from the FOURCC or D3DFORMAT value.
    subtype.Data1 = fccFormat;

    HRESULT hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_INTERLACE_MODE, interlaceMode);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the default stride value.
    hr = pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the image size in bytes.
    hr = MFCalculateImageSize(subtype, width, height, &cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_SAMPLE_SIZE, cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_FIXED_SIZE_SAMPLES, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Frame rate
    hr = MFSetAttributeRatio(pType, MF_MT_FRAME_RATE, frameRate.Numerator, 
        frameRate.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Pixel aspect ratio
    hr = MFSetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, par.Numerator, 
        par.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



L’exemple suivant utilise un format vidéo encodé comme entrée et crée un type de vidéo non compressé correspondant. Ce type peut être défini sur un encodeur ou un décodeur, par exemple.


```C++
HRESULT ConvertVideoTypeToUncompressedType(
    IMFMediaType *pType,    // Pointer to an encoded video type.
    const GUID& subtype,    // Uncompressed subtype (eg, RGB-32, AYUV)
    IMFMediaType **ppType   // Receives a matching uncompressed video type.
    )
{
    IMFMediaType *pTypeUncomp = NULL;

    HRESULT hr = S_OK;
    GUID majortype = { 0 };
    MFRatio par = { 0 };

    hr = pType->GetMajorType(&majortype);

    if (majortype != MFMediaType_Video)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Create a new media type and copy over all of the items.
    // This ensures that extended color information is retained.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pTypeUncomp);
    }

    if (SUCCEEDED(hr))
    {
        hr = pType->CopyAllItems(pTypeUncomp);
    }

    // Set the subtype.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetGUID(MF_MT_SUBTYPE, subtype);
    }

    // Uncompressed means all samples are independent.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    }

    // Fix up PAR if not set on the original type.
    if (SUCCEEDED(hr))
    {
        hr = MFGetAttributeRatio(
            pTypeUncomp, 
            MF_MT_PIXEL_ASPECT_RATIO, 
            (UINT32*)&par.Numerator, 
            (UINT32*)&par.Denominator
            );

        // Default to square pixels.
        if (FAILED(hr))
        {
            hr = MFSetAttributeRatio(
                pTypeUncomp, 
                MF_MT_PIXEL_ASPECT_RATIO, 
                1, 1
                );
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppType = pTypeUncomp;
        (*ppType)->AddRef();
    }

    SafeRelease(&pTypeUncomp);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations sur les couleurs étendues](extended-color-information.md)
</dt> <dt>

[STRIDE d’image](image-stride.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> <dt>

[Types de média vidéo](video-media-types.md)
</dt> <dt>

[GUID de sous-type de vidéo](video-subtype-guids.md)
</dt> </dl>

 

 



