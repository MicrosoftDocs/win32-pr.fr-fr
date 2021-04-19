---
description: Le Media Foundation le décodeur vidéo H. 264 est une transformation Media Foundation qui prend en charge le décodage des profils de base, principal et élevé, jusqu’au niveau 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Décodeur vidéo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484056"
---
# <a name="h264-video-decoder"></a><span data-ttu-id="3131e-103">Décodeur vidéo H. 264</span><span class="sxs-lookup"><span data-stu-id="3131e-103">H.264 Video Decoder</span></span>

<span data-ttu-id="3131e-104">Le Media Foundation le décodeur vidéo H. 264 est une [transformation Media Foundation](media-foundation-transforms.md) qui prend en charge le décodage des profils de base, principal et élevé, jusqu’au niveau 5,1.</span><span class="sxs-lookup"><span data-stu-id="3131e-104">The Media Foundation H.264 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding of Baseline, Main, and High profiles, up to level 5.1.</span></span>

<span data-ttu-id="3131e-105">Le décodeur vidéo H. 264 expose les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="3131e-105">The H.264 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="3131e-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (pris en charge dans Windows 8)</span><span class="sxs-lookup"><span data-stu-id="3131e-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="3131e-107">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="3131e-107">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="3131e-108">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="3131e-108">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="3131e-109">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="3131e-109">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="3131e-110">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="3131e-110">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="3131e-111">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="3131e-111">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="3131e-112">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="3131e-112">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="3131e-113">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="3131e-113">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="3131e-114">Pour créer une instance du décodeur, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3131e-114">To create an instance of the decoder, do one of the following:</span></span>

-   <span data-ttu-id="3131e-115">Appelez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="3131e-115">Call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>
-   <span data-ttu-id="3131e-116">Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="3131e-116">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="3131e-117">Le CLSID du décodeur est **CLSID \_ CMSH264DecoderMFT**, déclaré dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="3131e-117">The CLSID for the decoder is **CLSID\_CMSH264DecoderMFT**, declared in wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="3131e-118">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="3131e-118">Input Types</span></span>

<span data-ttu-id="3131e-119">Le type d’entrée doit contenir au moins les deux attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="3131e-119">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="3131e-120">Attribut</span><span class="sxs-lookup"><span data-stu-id="3131e-120">Attribute</span></span>                                                 | <span data-ttu-id="3131e-121">Description</span><span class="sxs-lookup"><span data-stu-id="3131e-121">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3131e-122">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="3131e-122">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="3131e-123">**\_Vidéo MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3131e-123">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="3131e-124">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="3131e-124">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="3131e-125">[MFVideoFormat \_ H264 –](video-subtype-guids.md) ou MFVideoFormat \_ H264 – \_ es</span><span class="sxs-lookup"><span data-stu-id="3131e-125">[MFVideoFormat\_H264](video-subtype-guids.md) or MFVideoFormat\_H264\_ES</span></span> |



 

<span data-ttu-id="3131e-126">Si le type d’entrée contient uniquement ces deux attributs, le décodeur offrira un type de sortie par défaut, qui agit comme un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="3131e-126">If the input type contains only these two attributes, the decoder will offer a default output type, which acts as a placeholder.</span></span> <span data-ttu-id="3131e-127">Quand le décodeur reçoit suffisamment d’échantillons d’entrée pour produire une trame de sortie, il signale une modification de format en retournant le **changement de flux de \_ \_ transformation \_ \_ MF E** à partir de [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="3131e-127">When the decoder receives enough input samples to produce an output frame, it signals a format change by returning **MF\_E\_TRANSFORM\_STREAM\_CHANGE** from [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="3131e-128">Pour plus d’informations sur la gestion des modifications de format, consultez la documentation de **ProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="3131e-128">See the **ProcessOutput** documentation for details about handling format changes.</span></span>

<span data-ttu-id="3131e-129">Pour éviter une modification de format initiale, fournissez autant d’informations que possible dans le type d’entrée, notamment :</span><span class="sxs-lookup"><span data-stu-id="3131e-129">To avoid an initial format change, provide as much information in the input type as possible, including:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3131e-130">Attribut</span><span class="sxs-lookup"><span data-stu-id="3131e-130">Attribute</span></span></th>
<th><span data-ttu-id="3131e-131">Description</span><span class="sxs-lookup"><span data-stu-id="3131e-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3131e-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3131e-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="3131e-133">Fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="3131e-133">Frame rate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3131e-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3131e-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="3131e-135">Dimensions de l’image.</span><span class="sxs-lookup"><span data-stu-id="3131e-135">Frame dimensions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3131e-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3131e-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="3131e-137">Mode entrelacé.</span><span class="sxs-lookup"><span data-stu-id="3131e-137">Interlace mode.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3131e-138">Dans la vidéo H. 264, la structure entrelacée peut changer de manière dynamique, donc la valeur recommandée de cet attribut est <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span><span class="sxs-lookup"><span data-stu-id="3131e-138">In H.264 video, the interlace structure can change dynamically, so the recommended value of this attribute is <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span></span> <span data-ttu-id="3131e-139">Les informations entrelacées dans le flux élémentaire vidéo sont prioritaires sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="3131e-139">Interlace information in the video elementary stream takes precedence over the media type.</span></span> <span data-ttu-id="3131e-140">Pour plus d’informations, consultez l' <a href="video-interlacing.md">entrelacement de vidéos</a>.</span><span class="sxs-lookup"><span data-stu-id="3131e-140">For more information, see <a href="video-interlacing.md">Video Interlacing</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3131e-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="3131e-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="3131e-142">Proportions de pixels.</span><span class="sxs-lookup"><span data-stu-id="3131e-142">Pixel aspect ratio.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3131e-143">Le type d’entrée doit être défini avant le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="3131e-143">The input type must be set before the output type.</span></span> <span data-ttu-id="3131e-144">Tant que le type d’entrée n’est pas défini, la méthode [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) de l’encodeur retourne le **type de \_ transformation MF E \_ \_ \_ non \_ défini**.</span><span class="sxs-lookup"><span data-stu-id="3131e-144">Until the input type is set, the encoder's [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="3131e-145">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="3131e-145">Output Types</span></span>

<span data-ttu-id="3131e-146">Le décodeur prend en charge les sous-types de sortie suivants :</span><span class="sxs-lookup"><span data-stu-id="3131e-146">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="3131e-147">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="3131e-147">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="3131e-148">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="3131e-148">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="3131e-149">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="3131e-149">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="3131e-150">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="3131e-150">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="3131e-151">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="3131e-151">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="3131e-152">Pour plus d’informations sur ces sous-types, consultez [GUID sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3131e-152">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="3131e-153">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="3131e-153">Transform Attributes</span></span>

<span data-ttu-id="3131e-154">Le décodeur H. 264 implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="3131e-154">The H.264 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="3131e-155">Les applications peuvent utiliser cette méthode pour récupérer ou définir les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="3131e-155">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="3131e-156">Attribut</span><span class="sxs-lookup"><span data-stu-id="3131e-156">Attribute</span></span>                                                                                       | <span data-ttu-id="3131e-157">Description</span><span class="sxs-lookup"><span data-stu-id="3131e-157">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3131e-158">CODECAPI \_ AVDecVideoAcceleration \_ H264 –</span><span class="sxs-lookup"><span data-stu-id="3131e-158">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="3131e-159">Active ou désactive l’accélération matérielle.</span><span class="sxs-lookup"><span data-stu-id="3131e-159">Enables or disables hardware acceleration.</span></span>                                                 |
| [<span data-ttu-id="3131e-160">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="3131e-160">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="3131e-161">Active ou désactive le mode de génération de miniatures.</span><span class="sxs-lookup"><span data-stu-id="3131e-161">Enables or disables thumbnail generation mode.</span></span>                                             |
| [<span data-ttu-id="3131e-162">Compatible avec la prise en \_ \_ charge Direct3D MF \_</span><span class="sxs-lookup"><span data-stu-id="3131e-162">MF\_SA\_D3D\_AWARE</span></span>](mf-sa-d3d-aware-attribute.md)                                             | <span data-ttu-id="3131e-163">Indique que le décodeur prend en charge l’accélération vidéo DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="3131e-163">Indicates that the decoder supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="3131e-164">Traiter en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3131e-164">Treat as read-only.</span></span> |



 

<span data-ttu-id="3131e-165">Dans Windows 8, le décodeur H. 264 prend également en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="3131e-165">In Windows 8, the H.264 decoder also supports the following attributes.</span></span>



| <span data-ttu-id="3131e-166">Attribut</span><span class="sxs-lookup"><span data-stu-id="3131e-166">Attribute</span></span>                                                                                                     | <span data-ttu-id="3131e-167">Description</span><span class="sxs-lookup"><span data-stu-id="3131e-167">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3131e-168">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="3131e-168">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="3131e-169">Active ou désactive le mode de décodage à latence faible.</span><span class="sxs-lookup"><span data-stu-id="3131e-169">Enables or disables low-latency decoding mode.</span></span>                                                              |
| [<span data-ttu-id="3131e-170">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="3131e-170">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                                         | <span data-ttu-id="3131e-171">Définit le nombre de threads de travail utilisés par le décodeur.</span><span class="sxs-lookup"><span data-stu-id="3131e-171">Sets the number of worker threads used by the decoder.</span></span>                                                      |
| [<span data-ttu-id="3131e-172">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="3131e-172">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)                                     | <span data-ttu-id="3131e-173">Définit la largeur maximale d’image que le décodeur acceptera comme type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3131e-173">Sets the maximum picture width that the decoder will accept as an input type.</span></span>                               |
| [<span data-ttu-id="3131e-174">CODECAPI \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="3131e-174">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)                                   | <span data-ttu-id="3131e-175">Définit la hauteur d’image maximale que le décodeur acceptera comme type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3131e-175">Sets the maximum picture height that the decoder will accept as an input type.</span></span>                              |
| [<span data-ttu-id="3131e-176">\_ \_ nombre minimal d' \_ échantillons de sortie MF \_ sa \_</span><span class="sxs-lookup"><span data-stu-id="3131e-176">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                               | <span data-ttu-id="3131e-177">Spécifie le nombre maximal d’échantillons de sortie.</span><span class="sxs-lookup"><span data-stu-id="3131e-177">Specifies the maximum number of output samples.</span></span>                                                             |
| [<span data-ttu-id="3131e-178">le \_ DÉcodeur MFT \_ expose les \_ \_ types \_ de sortie dans l' \_ \_ ordre natif</span><span class="sxs-lookup"><span data-stu-id="3131e-178">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="3131e-179">Spécifie si un décodeur expose des types de sortie IYUV/I420 (convenant au transcodage) avant d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="3131e-179">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span> |



 

<span data-ttu-id="3131e-180">Dans Windows 8, le décodeur H. 264 prend en charge l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="3131e-180">In Windows 8, the H.264 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="3131e-181">Cette interface fournit une API alternativate pour définir les propriétés de codec suivantes.</span><span class="sxs-lookup"><span data-stu-id="3131e-181">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="3131e-182">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="3131e-182">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="3131e-183">CODECAPI \_ AVDecVideoAcceleration \_ H264 –</span><span class="sxs-lookup"><span data-stu-id="3131e-183">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)
-   [<span data-ttu-id="3131e-184">CODECAPI \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="3131e-184">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)
-   [<span data-ttu-id="3131e-185">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="3131e-185">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="3131e-186">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="3131e-186">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a><span data-ttu-id="3131e-187">Contraintes de format</span><span class="sxs-lookup"><span data-stu-id="3131e-187">Format Constraints</span></span>

<span data-ttu-id="3131e-188">Le décodeur prend en charge les formats suivants :</span><span class="sxs-lookup"><span data-stu-id="3131e-188">The decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3131e-189">Profils/niveaux</span><span class="sxs-lookup"><span data-stu-id="3131e-189">Profiles/Levels</span></span></td>
<td><span data-ttu-id="3131e-190">Les profils de base, principal et élevé, jusqu’au niveau 5,1.</span><span class="sxs-lookup"><span data-stu-id="3131e-190">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="3131e-191">(Pour plus d’informations, consultez la spécification ITU-T H. 264.)</span><span class="sxs-lookup"><span data-stu-id="3131e-191">(See ITU-T H.264 specification for details.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3131e-192">Formats de chrominance</span><span class="sxs-lookup"><span data-stu-id="3131e-192">Chroma Formats</span></span></td>
<td><span data-ttu-id="3131e-193">4:2:0 Chroma ou monochrome</span><span class="sxs-lookup"><span data-stu-id="3131e-193">4:2:0 chroma or monochrome</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3131e-194">Résolution minimale</span><span class="sxs-lookup"><span data-stu-id="3131e-194">Minimum Resolution</span></span></td>
<td><span data-ttu-id="3131e-195">48 × 48 pixels</span><span class="sxs-lookup"><span data-stu-id="3131e-195">48 × 48 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3131e-196">Résolution maximale</span><span class="sxs-lookup"><span data-stu-id="3131e-196">Maximum Resolution</span></span></td>
<td><span data-ttu-id="3131e-197">4096 × 2304 pixels</span><span class="sxs-lookup"><span data-stu-id="3131e-197">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="3131e-198">La résolution maximale garantie pour l’accélération DXVA est de 1920 × 1088 pixels ; à des résolutions supérieures, le décodage s’effectue avec DXVA, s’il est pris en charge par le matériel sous-jacent ; sinon, le décodage est effectué avec le logiciel.</span><span class="sxs-lookup"><span data-stu-id="3131e-198">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3131e-199">Dans Windows 7, la résolution maximale prise en charge est de 1920 × 1088 pixels pour le décodage logiciel et DXVA.</span><span class="sxs-lookup"><span data-stu-id="3131e-199">In Windows 7, the maximum supported resolution is 1920 × 1088 pixels for both software and DXVA decoding.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3131e-200">DXVA</span><span class="sxs-lookup"><span data-stu-id="3131e-200">DXVA</span></span></td>
<td><span data-ttu-id="3131e-201">Le décodeur prend en charge la version 2 DXVA, mais pas la version 1 de la version DXVA.</span><span class="sxs-lookup"><span data-stu-id="3131e-201">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="3131e-202">Le décodage DXVA est pris en charge uniquement pour les flux de bits de ligne de base, principal et de profil principal compatibles.</span><span class="sxs-lookup"><span data-stu-id="3131e-202">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="3131e-203">(Les flux de bits de base compatibles avec les principaux sont définis comme <strong>profile_idc</strong>= 66 et <strong>constrained_set1_flag</strong>= 1.)</span><span class="sxs-lookup"><span data-stu-id="3131e-203">(Main-compatible Baseline bitstreams are defined as <strong>profile_idc</strong>=66 and <strong>constrained_set1_flag</strong>=1.)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3131e-204">Les données d’entrée doivent être conformes à l’annexe B de la norme ISO/IEC 14496-10.</span><span class="sxs-lookup"><span data-stu-id="3131e-204">Input data must conform to Annex B of ISO/IEC 14496-10.</span></span> <span data-ttu-id="3131e-205">Les données doivent inclure les codes de début.</span><span class="sxs-lookup"><span data-stu-id="3131e-205">The data must include the start codes.</span></span> <span data-ttu-id="3131e-206">Le décodeur ignore les octets jusqu’à ce qu’il trouve un jeu de paramètres de séquence (SPS) et un jeu de paramètres d’image (PPS) valides dans le flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="3131e-206">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

<span data-ttu-id="3131e-207">Le décodeur ne prend pas en charge la technologie de grain de film.</span><span class="sxs-lookup"><span data-stu-id="3131e-207">The decoder does not support Film Grain Technology.</span></span>

> [!Note]  
> <span data-ttu-id="3131e-208">Une version précédente de la documentation indiquait incorrectement que le décodeur est pris en charge sur Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="3131e-208">A previous version of the documentation incorrectly stated that the decoder is supported on Windows Server 2008 R2.</span></span>

 

<span data-ttu-id="3131e-209">Si la mise à jour du supplément Platform pour Windows Vista est installée, le décodeur vidéo H. 264 est disponible sur Windows Vista, mais n’est accessible sur Windows Vista qu’à l’aide du [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="3131e-209">If Platform Update Supplement for Windows Vista is installed, the H.264 video decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3131e-210">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3131e-210">Requirements</span></span>



| <span data-ttu-id="3131e-211">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3131e-211">Requirement</span></span> | <span data-ttu-id="3131e-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="3131e-212">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3131e-213">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3131e-213">Minimum supported client</span></span><br/> | <span data-ttu-id="3131e-214">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3131e-214">Windows 7 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3131e-215">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3131e-215">Minimum supported server</span></span><br/> | <span data-ttu-id="3131e-216">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3131e-216">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="3131e-217">DLL</span><span class="sxs-lookup"><span data-stu-id="3131e-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3131e-218"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3131e-218"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3131e-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3131e-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3131e-220">Objets codec</span><span class="sxs-lookup"><span data-stu-id="3131e-220">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="3131e-221">Prise en charge MPEG-4 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3131e-221">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="3131e-222">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3131e-222">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="3131e-223">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="3131e-223">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
