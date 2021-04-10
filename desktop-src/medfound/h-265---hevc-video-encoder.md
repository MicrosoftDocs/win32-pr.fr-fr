---
description: L’encodeur vidéo Media Foundation H. 265 est une transformation Media Foundation qui prend en charge l’encodage de contenu au format H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Encodeur vidéo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951441"
---
# <a name="h265--hevc-video-encoder"></a><span data-ttu-id="35e6a-103">Encodeur vidéo H. 265/HEVC</span><span class="sxs-lookup"><span data-stu-id="35e6a-103">H.265 / HEVC Video Encoder</span></span>

<span data-ttu-id="35e6a-104">L’encodeur vidéo Media Foundation H. 265 est une [transformation Media Foundation](media-foundation-transforms.md) qui prend en charge l’encodage de contenu au format H. 265/HEVC.</span><span class="sxs-lookup"><span data-stu-id="35e6a-104">The Media Foundation H.265 video encoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports encoding content into the H.265/HEVC format.</span></span> <span data-ttu-id="35e6a-105">L’encodeur prend en charge les profils suivants :</span><span class="sxs-lookup"><span data-stu-id="35e6a-105">The encoder supports the following profiles:</span></span>

-   <span data-ttu-id="35e6a-106">Profil Main</span><span class="sxs-lookup"><span data-stu-id="35e6a-106">Main Profile</span></span>

<span data-ttu-id="35e6a-107">L’encodeur vidéo H. 265 expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="35e6a-107">The H.265 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="35e6a-108">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="35e6a-108">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="35e6a-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="35e6a-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="35e6a-110">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="35e6a-110">Input Types</span></span>

<span data-ttu-id="35e6a-111">Le type de média d’entrée doit avoir l’un des sous-types suivants :</span><span class="sxs-lookup"><span data-stu-id="35e6a-111">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="35e6a-112">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="35e6a-112">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="35e6a-113">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="35e6a-113">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="35e6a-114">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="35e6a-114">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="35e6a-115">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="35e6a-115">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="35e6a-116">Pour plus d’informations sur ces sous-types, consultez [GUID sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="35e6a-116">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="35e6a-117">Le type de sortie doit être défini avant le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="35e6a-117">The output type must be set before the input type.</span></span> <span data-ttu-id="35e6a-118">Tant que le type de sortie n’est pas défini, la méthode [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) de l’encodeur retourne le **type de \_ transformation MF E \_ \_ \_ non \_ défini**.</span><span class="sxs-lookup"><span data-stu-id="35e6a-118">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="35e6a-119">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="35e6a-119">Output Types</span></span>

<span data-ttu-id="35e6a-120">L’encodeur prend en charge un seul sous-type de sortie :</span><span class="sxs-lookup"><span data-stu-id="35e6a-120">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="35e6a-121">**MFVideoFormat \_ H265**</span><span class="sxs-lookup"><span data-stu-id="35e6a-121">**MFVideoFormat\_H265**</span></span>

<span data-ttu-id="35e6a-122">Définissez les attributs suivants sur le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="35e6a-122">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35e6a-123">Attribut</span><span class="sxs-lookup"><span data-stu-id="35e6a-123">Attribute</span></span></th>
<th><span data-ttu-id="35e6a-124">Description</span><span class="sxs-lookup"><span data-stu-id="35e6a-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35e6a-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-126">Type principal.</span><span class="sxs-lookup"><span data-stu-id="35e6a-126">Major type.</span></span> <span data-ttu-id="35e6a-127">Doit être <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="35e6a-127">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-129">Sous-type de vidéo.</span><span class="sxs-lookup"><span data-stu-id="35e6a-129">Video subtype.</span></span> <span data-ttu-id="35e6a-130">Doit être <strong>MFVideoFormat_HEVC</strong>.</span><span class="sxs-lookup"><span data-stu-id="35e6a-130">Must be <strong>MFVideoFormat_HEVC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-132">Vitesse moyenne des bits encodés, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="35e6a-132">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="35e6a-133">Doit être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="35e6a-133">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-135">Fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="35e6a-135">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-137">Taille du frame.</span><span class="sxs-lookup"><span data-stu-id="35e6a-137">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-139">Mode entrelacé.</span><span class="sxs-lookup"><span data-stu-id="35e6a-139">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span></span></td>
<td><span data-ttu-id="35e6a-141">Profil d’encodage H. 265.</span><span class="sxs-lookup"><span data-stu-id="35e6a-141">H.265 encoding profile.</span></span><br/> <span data-ttu-id="35e6a-142">Les valeurs prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="35e6a-142">The supported values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="35e6a-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span><span class="sxs-lookup"><span data-stu-id="35e6a-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-145">Spécifie le niveau de la vidéo codée.</span><span class="sxs-lookup"><span data-stu-id="35e6a-145">Specifies the level of the coded video.</span></span> <span data-ttu-id="35e6a-146">Pour plus d’informations sur les contraintes de profil et de niveau, reportez-vous à l’annexe A de l’ITU-T H. 265.</span><span class="sxs-lookup"><span data-stu-id="35e6a-146">For more information about profile and level constraints, refer to Annex A of ITU-T H.265.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-148">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="35e6a-148">Optional.</span></span> <span data-ttu-id="35e6a-149">Spécifie les proportions en pixels.</span><span class="sxs-lookup"><span data-stu-id="35e6a-149">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="35e6a-150">La valeur par défaut est 1:1.</span><span class="sxs-lookup"><span data-stu-id="35e6a-150">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="35e6a-151">Une fois le type de sortie défini, l’encodeur vidéo met à jour le type en ajoutant l’attribut d' [**\_ \_ \_ \_ en-tête de séquence MPEG MF MT**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="35e6a-151">After the output type is set, the video encoder updates the type by adding the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="35e6a-152">Cet attribut contient l’en-tête de séquence.</span><span class="sxs-lookup"><span data-stu-id="35e6a-152">This attribute contains the sequence header.</span></span>

## <a name="supported-imftransform-methods"></a><span data-ttu-id="35e6a-153">Méthodes IMFTransform prises en charge</span><span class="sxs-lookup"><span data-stu-id="35e6a-153">Supported IMFTransform methods</span></span>

<span data-ttu-id="35e6a-154">Les méthodes suivantes de l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sont prises en charge pour l’encodeur H. 265/HEVC :</span><span class="sxs-lookup"><span data-stu-id="35e6a-154">The following methods of the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="35e6a-155">**GetAttributes,**</span><span class="sxs-lookup"><span data-stu-id="35e6a-155">**GetAttributes**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [<span data-ttu-id="35e6a-156">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="35e6a-156">**GetInputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [<span data-ttu-id="35e6a-157">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="35e6a-157">**GetInputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [<span data-ttu-id="35e6a-158">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="35e6a-158">**GetInputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [<span data-ttu-id="35e6a-159">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="35e6a-159">**GetInputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [<span data-ttu-id="35e6a-160">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="35e6a-160">**GetOutputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [<span data-ttu-id="35e6a-161">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="35e6a-161">**GetOutputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [<span data-ttu-id="35e6a-162">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="35e6a-162">**GetOutputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [<span data-ttu-id="35e6a-163">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="35e6a-163">**GetOutputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [<span data-ttu-id="35e6a-164">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="35e6a-164">**GetStreamCount**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [<span data-ttu-id="35e6a-165">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="35e6a-165">**GetStreamLimits**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [<span data-ttu-id="35e6a-166">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="35e6a-166">**ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [<span data-ttu-id="35e6a-167">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="35e6a-167">**ProcessMessage**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [<span data-ttu-id="35e6a-168">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="35e6a-168">**ProcessInput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [<span data-ttu-id="35e6a-169">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="35e6a-169">**ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [<span data-ttu-id="35e6a-170">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="35e6a-170">**SetInputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [<span data-ttu-id="35e6a-171">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="35e6a-171">**SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [<span data-ttu-id="35e6a-172">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="35e6a-172">**SetOutputBounds**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

<span data-ttu-id="35e6a-173">Toutes les autres méthodes [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retournent l’erreur E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="35e6a-173">All other [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods will return the error E\_NOTIMPL.</span></span>

## <a name="supported-icodecapi-methods"></a><span data-ttu-id="35e6a-174">Méthodes ICodecAPI prises en charge</span><span class="sxs-lookup"><span data-stu-id="35e6a-174">Supported ICodecAPI methods</span></span>

<span data-ttu-id="35e6a-175">Les méthodes suivantes de l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) sont prises en charge pour l’encodeur H. 265/HEVC :</span><span class="sxs-lookup"><span data-stu-id="35e6a-175">The following methods of the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="35e6a-176">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="35e6a-176">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="35e6a-177">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="35e6a-177">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [<span data-ttu-id="35e6a-178">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="35e6a-178">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="35e6a-179">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="35e6a-179">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="35e6a-180">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="35e6a-180">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

<span data-ttu-id="35e6a-181">Toutes les autres méthodes [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retournent l’erreur E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="35e6a-181">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods will return the error E\_NOTIMPL.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="35e6a-182">Propriétés du codec</span><span class="sxs-lookup"><span data-stu-id="35e6a-182">Codec Properties</span></span>

<span data-ttu-id="35e6a-183">L’encodeur H. 265 implémente l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) pour définir les paramètres d’encodage.</span><span class="sxs-lookup"><span data-stu-id="35e6a-183">The H.265 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="35e6a-184">Il prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="35e6a-184">It supports the following properties.</span></span>

<span data-ttu-id="35e6a-185">Pour connaître la configuration requise du codec pour la certification de l’encodeur TPM, **consultez la section** ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="35e6a-185">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35e6a-186">Propriété</span><span class="sxs-lookup"><span data-stu-id="35e6a-186">Property</span></span></th>
<th><span data-ttu-id="35e6a-187">Description</span><span class="sxs-lookup"><span data-stu-id="35e6a-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35e6a-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="35e6a-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span></span></td>
<td><span data-ttu-id="35e6a-189">Définit le mode de contrôle de la fréquence.</span><span class="sxs-lookup"><span data-stu-id="35e6a-189">Sets the rate control mode.</span></span> <span data-ttu-id="35e6a-190">Les modes pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="35e6a-190">The supported modes are:</span></span><br/>
<ul>
<li><span data-ttu-id="35e6a-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span><span class="sxs-lookup"><span data-stu-id="35e6a-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span></span></li>
<li><span data-ttu-id="35e6a-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span><span class="sxs-lookup"><span data-stu-id="35e6a-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span></span></li>
</ul>
<span data-ttu-id="35e6a-193">Si d’autres modes sont spécifiés, le contrôle de taux de <strong>eAVEncCommonRateControlMode_CBR</strong> est utilisé.</span><span class="sxs-lookup"><span data-stu-id="35e6a-193">If other modes are specified, the <strong>eAVEncCommonRateControlMode_CBR</strong> rate control will be used.</span></span><br/> <span data-ttu-id="35e6a-194">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-194">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="35e6a-196">Définit la vitesse de transmission moyenne pour le flux binaire encodé, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="35e6a-196">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <br/> <span data-ttu-id="35e6a-197">La plage valide est [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="35e6a-197">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="35e6a-198">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-198">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="35e6a-200">Définit la taille de la mémoire tampon, en octets, pour l’encodage à débit binaire constant (CBR).</span><span class="sxs-lookup"><span data-stu-id="35e6a-200">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="35e6a-201">La plage valide est [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="35e6a-201">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="35e6a-202">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-202">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="35e6a-204">Définit le débit maximal pour les modes de contrôle de débit qui autorisent une vitesse de transmission maximale.</span><span class="sxs-lookup"><span data-stu-id="35e6a-204">Sets the maximum bitrate for rate control modes that allow a peak bitrate.</span></span> <br/> <span data-ttu-id="35e6a-205">La plage valide est [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="35e6a-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="35e6a-206">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-206">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="35e6a-208">Définit le nombre d’images d’un en-tête GOP sur le suivant, y compris l’ancrage de début, mais pas le suivant.</span><span class="sxs-lookup"><span data-stu-id="35e6a-208">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="35e6a-209">La plage valide est [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="35e6a-209">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="35e6a-210">Si la valeur est zéro, l’encodeur sélectionne la taille de groupe d’images.</span><span class="sxs-lookup"><span data-stu-id="35e6a-210">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="35e6a-211">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="35e6a-211">The default value is zero.</span></span> <br/> <span data-ttu-id="35e6a-212">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-212">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="35e6a-214">Active ou désactive le mode faible latence.</span><span class="sxs-lookup"><span data-stu-id="35e6a-214">Enables or disables low-latency mode.</span></span> <br/> <span data-ttu-id="35e6a-215">Il s’agit d’une valeur VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="35e6a-215">This is a VT_BOOL value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="35e6a-217">Définit le compromis de qualité/vitesse.</span><span class="sxs-lookup"><span data-stu-id="35e6a-217">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="35e6a-218">Cette valeur affecte la façon dont l’encodeur effectue différentes opérations d’encodage, telles que la compensation de mouvement.</span><span class="sxs-lookup"><span data-stu-id="35e6a-218">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="35e6a-219">À des niveaux de complexité plus élevés, l’encodeur s’exécute plus lentement, mais produit une meilleure qualité à la même vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="35e6a-219">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span> <br/> <span data-ttu-id="35e6a-220">La plage valide est comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="35e6a-220">The valid range is 0 – 100.</span></span> <span data-ttu-id="35e6a-221">En interne, cette valeur est mappée à un plus petit ensemble de niveaux de qualité/vitesse pris en charge par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="35e6a-221">Internally, this value is mapped to a smaller set of quality/speed levels supported by the encoder.</span></span><br/> <span data-ttu-id="35e6a-222">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-222">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="35e6a-224">Force l’encodeur à coder le frame suivant comme une image clé.</span><span class="sxs-lookup"><span data-stu-id="35e6a-224">Forces the encoder to code the next frame as a key frame.</span></span><br/> <span data-ttu-id="35e6a-225">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-225">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="35e6a-227">Lorsque cette propriété est définie, l’encodeur utilise le QP spécifié pour encoder le frame suivant et tous les frames suivants jusqu’à ce qu’un nouveau QP soit spécifié.</span><span class="sxs-lookup"><span data-stu-id="35e6a-227">When this property is set it will cause the encoder to use the specified QP to encode the next frame and all subsequent frames until a new QP is specified.</span></span> <br/> <span data-ttu-id="35e6a-228">Plage valide : comprise entre 0 et 51</span><span class="sxs-lookup"><span data-stu-id="35e6a-228">Valid range: 0–51, inclusive</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="35e6a-230">Cette propriété définit une limite au minimum de QP que l’encodeur peut utiliser pendant le RateControl CBR.</span><span class="sxs-lookup"><span data-stu-id="35e6a-230">This property will set a limit on the minimum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="35e6a-231">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-231">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span></span></td>
<td><span data-ttu-id="35e6a-233">Cette propriété définit une limite au maximum de QP que l’encodeur peut utiliser pendant le RateControl CBR.</span><span class="sxs-lookup"><span data-stu-id="35e6a-233">This property will set a limit on the maximum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="35e6a-234">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-234">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35e6a-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span></span></td>
<td><span data-ttu-id="35e6a-236">Définit si le contenu est une vidéo en plein écran, par opposition au contenu d’écran qui peut avoir une fenêtre de vidéo plus petite ou n’avoir aucune vidéo du tout.</span><span class="sxs-lookup"><span data-stu-id="35e6a-236">Sets whether the content is full-screen video, as opposed to screen content that might have a smaller window of video or have no video at all.</span></span><br/> <span data-ttu-id="35e6a-237">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-237">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35e6a-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="35e6a-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="35e6a-239">Définit le nombre de threads utilisés pour effectuer l’opération de compression.</span><span class="sxs-lookup"><span data-stu-id="35e6a-239">Sets the number of threads used to perform the compression operation.</span></span> <span data-ttu-id="35e6a-240">L’encodeur divise le frame en mosaïques, de sorte que le nombre de threads est égal au nombre de vignettes.</span><span class="sxs-lookup"><span data-stu-id="35e6a-240">The encoder will divide the frame into tiles such that the number of threads equals the number of tiles.</span></span><br/>
<ul>
<li><span data-ttu-id="35e6a-241">Nombre de processeurs logiques.</span><span class="sxs-lookup"><span data-stu-id="35e6a-241">The number of logical processors.</span></span> <span data-ttu-id="35e6a-242">Le nombre de threads doit être inférieur ou égal au nombre de processeurs logiques.</span><span class="sxs-lookup"><span data-stu-id="35e6a-242">The number of threads must be less than or equal to the number of logical processors.</span></span></li>
<li><span data-ttu-id="35e6a-243">Taille du frame.</span><span class="sxs-lookup"><span data-stu-id="35e6a-243">The size of the frame.</span></span> <span data-ttu-id="35e6a-244">La taille d’une vignette doit être supérieure ou égale à 265x64 pixels.</span><span class="sxs-lookup"><span data-stu-id="35e6a-244">The size of a tile must bigger than or equal to 265x64 pixels.</span></span></li>
<li><span data-ttu-id="35e6a-245">Parité.</span><span class="sxs-lookup"><span data-stu-id="35e6a-245">Parity.</span></span> <span data-ttu-id="35e6a-246">Le nombre de threads doit être une valeur paire.</span><span class="sxs-lookup"><span data-stu-id="35e6a-246">The number of threads must be an even value.</span></span> <span data-ttu-id="35e6a-247">Si la valeur spécifiée est irrégulière, la valeur paire inférieure suivante sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="35e6a-247">If the specified value is odd then the next lower even value will be used.</span></span></li>
</ul>
<span data-ttu-id="35e6a-248">Il s’agit d’une valeur VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="35e6a-248">This is a VT_UI4 value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a><span data-ttu-id="35e6a-249">Encodeur matériel certifié</span><span class="sxs-lookup"><span data-stu-id="35e6a-249">Certified Hardware Encoder</span></span>

<span data-ttu-id="35e6a-250">Si un encodeur matériel certifié est présent, il est généralement utilisé à la place de l’encodeur système de la boîte de réception pour Media Foundation scénarios associés.</span><span class="sxs-lookup"><span data-stu-id="35e6a-250">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="35e6a-251">Des encodeurs certifiés sont requis pour prendre en charge un certain ensemble de propriétés **ICodecAPI** et peuvent éventuellement prendre en charge un autre ensemble de propriétés.</span><span class="sxs-lookup"><span data-stu-id="35e6a-251">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="35e6a-252">Le processus de certification doit garantir que les propriétés requises sont correctement prises en charge et, si une propriété facultative est prise en charge, qu’elle est également prise en charge correctement.</span><span class="sxs-lookup"><span data-stu-id="35e6a-252">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="35e6a-253">Voici l’ensemble des propriétés **ICodecAPI** obligatoires et facultatives pour que les encodeurs passent la certification de l’encodeur TPM.</span><span class="sxs-lookup"><span data-stu-id="35e6a-253">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

-   [<span data-ttu-id="35e6a-254">CODECAPI \_ AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="35e6a-254">CODECAPI\_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="35e6a-255">CODECAPI \_ AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="35e6a-255">CODECAPI\_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="35e6a-256">CODECAPI \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="35e6a-256">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="35e6a-257">CODECAPI \_ AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="35e6a-257">CODECAPI\_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="35e6a-258">CODECAPI \_ AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="35e6a-258">CODECAPI\_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="35e6a-259">CODECAPI \_ AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="35e6a-259">CODECAPI\_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="35e6a-260">CODECAPI \_ AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="35e6a-260">CODECAPI\_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a><span data-ttu-id="35e6a-261">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35e6a-261">Requirements</span></span>



| <span data-ttu-id="35e6a-262">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35e6a-262">Requirement</span></span> | <span data-ttu-id="35e6a-263">Valeur</span><span class="sxs-lookup"><span data-stu-id="35e6a-263">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e6a-264">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35e6a-264">Minimum supported client</span></span><br/> | <span data-ttu-id="35e6a-265">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35e6a-265">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="35e6a-266">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35e6a-266">Minimum supported server</span></span><br/> | <span data-ttu-id="35e6a-267">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="35e6a-267">None supported</span></span><br/>                                                                |
| <span data-ttu-id="35e6a-268">DLL</span><span class="sxs-lookup"><span data-stu-id="35e6a-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e6a-269"><dt>Mfh265enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35e6a-269"><dt>Mfh265enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35e6a-270">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35e6a-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e6a-271">Objets codec</span><span class="sxs-lookup"><span data-stu-id="35e6a-271">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
