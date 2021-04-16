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
# <a name="uncompressed-video-media-types"></a><span data-ttu-id="3465f-103">Types de médias vidéo non compressés</span><span class="sxs-lookup"><span data-stu-id="3465f-103">Uncompressed Video Media Types</span></span>

<span data-ttu-id="3465f-104">Cette rubrique explique comment créer un type de média qui décrit un format vidéo non compressé.</span><span class="sxs-lookup"><span data-stu-id="3465f-104">This topic describes how to create a media type that describes an uncompressed video format.</span></span> <span data-ttu-id="3465f-105">Pour plus d’informations sur les types de médias, consultez [à propos des types de média](about-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="3465f-105">For more information about media types generally, see [About Media Types](about-media-types.md).</span></span>

<span data-ttu-id="3465f-106">Pour créer un type de vidéo non compressé complet, définissez les attributs suivants sur le pointeur d’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="3465f-106">To create a complete uncompressed video type, set the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="3465f-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="3465f-107">Attribute</span></span>                                                                            | <span data-ttu-id="3465f-108">Description</span><span class="sxs-lookup"><span data-stu-id="3465f-108">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3465f-109">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="3465f-109">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="3465f-110">Type principal.</span><span class="sxs-lookup"><span data-stu-id="3465f-110">Major type.</span></span> <span data-ttu-id="3465f-111">Définissez sur **MFMediaType \_ Video**.</span><span class="sxs-lookup"><span data-stu-id="3465f-111">Set to **MFMediaType\_Video**.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="3465f-112">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="3465f-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                   | <span data-ttu-id="3465f-113">Sous-type.</span><span class="sxs-lookup"><span data-stu-id="3465f-113">Subtype.</span></span> <span data-ttu-id="3465f-114">Consultez [GUID de sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3465f-114">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="3465f-115">**\_Stride MT \_ par défaut \_**</span><span class="sxs-lookup"><span data-stu-id="3465f-115">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)                    | <span data-ttu-id="3465f-116">STRIDE de surface.</span><span class="sxs-lookup"><span data-stu-id="3465f-116">Surface stride.</span></span> <span data-ttu-id="3465f-117">Le *Stride* est le nombre d’octets nécessaires pour passer d’une ligne de pixels à la suivante.</span><span class="sxs-lookup"><span data-stu-id="3465f-117">The *stride* is the number of bytes needed to go from one row of pixels to the next.</span></span> <span data-ttu-id="3465f-118">Définissez cet attribut si le Stride en octets n’est pas le même que la largeur vidéo en octets.</span><span class="sxs-lookup"><span data-stu-id="3465f-118">Set this attribute if the stride in bytes is not the same as the video width in bytes.</span></span> <span data-ttu-id="3465f-119">Sinon, vous pouvez omettre cet attribut.</span><span class="sxs-lookup"><span data-stu-id="3465f-119">Otherwise, you can omit this attribute.</span></span> |
| [<span data-ttu-id="3465f-120">**\_fréquence d' \_ images MF MF \_**</span><span class="sxs-lookup"><span data-stu-id="3465f-120">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)                            | <span data-ttu-id="3465f-121">Fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="3465f-121">Frame rate.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="3465f-122">**\_taille de \_ trame MF MF \_**</span><span class="sxs-lookup"><span data-stu-id="3465f-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                            | <span data-ttu-id="3465f-123">Taille du frame.</span><span class="sxs-lookup"><span data-stu-id="3465f-123">Frame size.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="3465f-124">**\_ \_ mode entrelacé MF-MT \_**</span><span class="sxs-lookup"><span data-stu-id="3465f-124">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                    | <span data-ttu-id="3465f-125">Mode entrelacement.</span><span class="sxs-lookup"><span data-stu-id="3465f-125">Interlacing mode.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="3465f-126">**MF \_ MT \_ tous les \_ exemples \_ indépendants**</span><span class="sxs-lookup"><span data-stu-id="3465f-126">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="3465f-127">Spécifie si chaque échantillon est indépendant.</span><span class="sxs-lookup"><span data-stu-id="3465f-127">Specifies whether each sample is independent.</span></span> <span data-ttu-id="3465f-128">Affectez la valeur **true** pour les formats non compressés.</span><span class="sxs-lookup"><span data-stu-id="3465f-128">Set to **TRUE** for uncompressed formats.</span></span>                                                                                                                                             |
| [<span data-ttu-id="3465f-129">**\_ \_ \_ rapport hauteur/largeur des pixels \_ MF**</span><span class="sxs-lookup"><span data-stu-id="3465f-129">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)           | <span data-ttu-id="3465f-130">Proportions de pixels.</span><span class="sxs-lookup"><span data-stu-id="3465f-130">Pixel aspect ratio.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="3465f-131">En outre, définissez les attributs suivants si vous connaissez les valeurs correctes.</span><span class="sxs-lookup"><span data-stu-id="3465f-131">In addition, set the following attributes if you know the correct values.</span></span> <span data-ttu-id="3465f-132">(Sinon, omettez ces attributs.)</span><span class="sxs-lookup"><span data-stu-id="3465f-132">(Otherwise, omit these attributes.)</span></span>



| <span data-ttu-id="3465f-133">Attribut</span><span class="sxs-lookup"><span data-stu-id="3465f-133">Attribute</span></span>                                                                    | <span data-ttu-id="3465f-134">Description</span><span class="sxs-lookup"><span data-stu-id="3465f-134">Description</span></span>        |
|------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="3465f-135">**\_vidéos de \_ \_ réamorçage de la vidéo MF**</span><span class="sxs-lookup"><span data-stu-id="3465f-135">**MF\_MT\_VIDEO\_PRIMARIES**</span></span>](mf-mt-video-primaries-attribute.md)          | <span data-ttu-id="3465f-136">Couleurs primaires.</span><span class="sxs-lookup"><span data-stu-id="3465f-136">Color primaries.</span></span>   |
| [<span data-ttu-id="3465f-137">**\_fonction de \_ transfert MF-MF \_**</span><span class="sxs-lookup"><span data-stu-id="3465f-137">**MF\_MT\_TRANSFER\_FUNCTION**</span></span>](mf-mt-transfer-function-attribute.md)      | <span data-ttu-id="3465f-138">Fonction de transfert.</span><span class="sxs-lookup"><span data-stu-id="3465f-138">Transfer function.</span></span> |
| [<span data-ttu-id="3465f-139">**\_ \_ matrice YUV MT \_ YUV**</span><span class="sxs-lookup"><span data-stu-id="3465f-139">**MF\_MT\_YUV\_MATRIX**</span></span>](mf-mt-yuv-matrix-attribute.md)                    | <span data-ttu-id="3465f-140">Matrice de transfert.</span><span class="sxs-lookup"><span data-stu-id="3465f-140">Transfer matrix.</span></span>   |
| [<span data-ttu-id="3465f-141">**vidéo MF MT-présentation de \_ \_ \_ chrominance \_**</span><span class="sxs-lookup"><span data-stu-id="3465f-141">**MF\_MT\_VIDEO\_CHROMA\_SITING**</span></span>](mf-mt-video-chroma-siting-attribute.md) | <span data-ttu-id="3465f-142">Emplacement de chrominance.</span><span class="sxs-lookup"><span data-stu-id="3465f-142">Chroma siting.</span></span>     |
| [<span data-ttu-id="3465f-143">**\_ \_ plage nominale de vidéo MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3465f-143">**MF\_MT\_VIDEO\_NOMINAL\_RANGE**</span></span>](mf-mt-video-nominal-range-attribute.md) | <span data-ttu-id="3465f-144">Plage nominale.</span><span class="sxs-lookup"><span data-stu-id="3465f-144">Nominal range.</span></span>     |



 

<span data-ttu-id="3465f-145">Pour plus d’informations, consultez [informations sur les couleurs étendues](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="3465f-145">For more information, see [Extended Color Information](extended-color-information.md).</span></span> <span data-ttu-id="3465f-146">Par exemple, si vous créez un type de média qui décrit une norme vidéo et que la norme définit l’emplacement de chrominance, ajoutez ces informations au type de média.</span><span class="sxs-lookup"><span data-stu-id="3465f-146">For example, if you create a media type that describes a video standard, and the standard defines the chroma siting, add this information to the media type.</span></span> <span data-ttu-id="3465f-147">Cela permet de préserver la fidélité des couleurs dans l’ensemble du pipeline.</span><span class="sxs-lookup"><span data-stu-id="3465f-147">Doing so helps to preserve color fidelity throughout the pipeline.</span></span>

<span data-ttu-id="3465f-148">Les fonctions suivantes peuvent être utiles lors de la création d’un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="3465f-148">The following functions might be useful when creating a video media type.</span></span>



| <span data-ttu-id="3465f-149">Fonction</span><span class="sxs-lookup"><span data-stu-id="3465f-149">Function</span></span>                                                                     | <span data-ttu-id="3465f-150">Description</span><span class="sxs-lookup"><span data-stu-id="3465f-150">Description</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3465f-151">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="3465f-151">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="3465f-152">Calcule la fréquence d’images, en fonction de la durée de trame moyenne.</span><span class="sxs-lookup"><span data-stu-id="3465f-152">Calculates the frame rate, given the average frame duration.</span></span>                                                                                                                         |
| [<span data-ttu-id="3465f-153">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="3465f-153">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="3465f-154">Calcule la taille de l’image pour un format vidéo non compressé.</span><span class="sxs-lookup"><span data-stu-id="3465f-154">Calculates the image size for an uncompressed video format.</span></span>                                                                                                                          |
| [<span data-ttu-id="3465f-155">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="3465f-155">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="3465f-156">Calcule la durée moyenne d’une image vidéo, en fonction de la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="3465f-156">Calculates the average duration of a video frame, given the frame rate.</span></span>                                                                                                              |
| [<span data-ttu-id="3465f-157">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="3465f-157">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="3465f-158">Retourne le Stride de surface minimal pour un format vidéo.</span><span class="sxs-lookup"><span data-stu-id="3465f-158">Returns the minimum surface stride for a video format.</span></span> <span data-ttu-id="3465f-159">Pour plus d’informations, consultez l' [image Stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="3465f-159">For more information, see [Image Stride](image-stride.md).</span></span>                                                                   |
| [<span data-ttu-id="3465f-160">**MFInitVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="3465f-160">**MFInitVideoFormat**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | <span data-ttu-id="3465f-161">Initialise une structure [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) pour certains formats vidéo standard, tels que la télévision NTSC.</span><span class="sxs-lookup"><span data-stu-id="3465f-161">Initializes an [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) structure for some standard video formats, such as NTSC television.</span></span> <span data-ttu-id="3465f-162">Vous pouvez ensuite utiliser la structure pour initialiser un type de média.</span><span class="sxs-lookup"><span data-stu-id="3465f-162">You can then use the structure to initialize a media type.</span></span> |
| [<span data-ttu-id="3465f-163">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="3465f-163">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="3465f-164">Interroge si un format vidéo est un format YUV.</span><span class="sxs-lookup"><span data-stu-id="3465f-164">Queries whether a video format is a YUV format.</span></span>                                                                                                                                      |



 

## <a name="examples"></a><span data-ttu-id="3465f-165">Exemples</span><span class="sxs-lookup"><span data-stu-id="3465f-165">Examples</span></span>

<span data-ttu-id="3465f-166">Cet exemple montre une fonction qui remplit les informations les plus courantes pour un format vidéo non compressé.</span><span class="sxs-lookup"><span data-stu-id="3465f-166">This example shows a function that fills in the most common information for an uncompressed video format.</span></span> <span data-ttu-id="3465f-167">La fonction retourne un pointeur d’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="3465f-167">The function returns an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span> <span data-ttu-id="3465f-168">Vous pouvez ensuite ajouter des attributs supplémentaires au type de média, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3465f-168">You can then add additional attributes to the media type as needed.</span></span>


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



<span data-ttu-id="3465f-169">L’exemple suivant utilise un format vidéo encodé comme entrée et crée un type de vidéo non compressé correspondant.</span><span class="sxs-lookup"><span data-stu-id="3465f-169">The next example takes an encoded video format as input, and creates a matching uncompressed video type.</span></span> <span data-ttu-id="3465f-170">Ce type peut être défini sur un encodeur ou un décodeur, par exemple.</span><span class="sxs-lookup"><span data-stu-id="3465f-170">This type would be suitable to set on an encoder or decoder, for example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3465f-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3465f-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3465f-172">Informations sur les couleurs étendues</span><span class="sxs-lookup"><span data-stu-id="3465f-172">Extended Color Information</span></span>](extended-color-information.md)
</dt> <dt>

[<span data-ttu-id="3465f-173">STRIDE d’image</span><span class="sxs-lookup"><span data-stu-id="3465f-173">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="3465f-174">Types de médias</span><span class="sxs-lookup"><span data-stu-id="3465f-174">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="3465f-175">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="3465f-175">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="3465f-176">GUID de sous-type de vidéo</span><span class="sxs-lookup"><span data-stu-id="3465f-176">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



