---
description: 'Le Microsoft Media Foundation encodeur vidéo H. 264 est une transformation Media Foundation qui prend en charge les profils H. 264 suivants :'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Encodeur vidéo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517567"
---
# <a name="h264-video-encoder"></a><span data-ttu-id="6f7ad-103">Encodeur vidéo H. 264</span><span class="sxs-lookup"><span data-stu-id="6f7ad-103">H.264 Video Encoder</span></span>

<span data-ttu-id="6f7ad-104">Le Microsoft Media Foundation encodeur vidéo H. 264 est une [transformation Media Foundation](media-foundation-transforms.md) qui prend en charge les profils H. 264 suivants :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-104">The Microsoft Media Foundation H.264 video encoder is a [Media Foundation transform](media-foundation-transforms.md) that supports the following H.264 profiles:</span></span>

-   <span data-ttu-id="6f7ad-105">Profil de base</span><span class="sxs-lookup"><span data-stu-id="6f7ad-105">Baseline Profile</span></span>
-   <span data-ttu-id="6f7ad-106">Profil Main</span><span class="sxs-lookup"><span data-stu-id="6f7ad-106">Main Profile</span></span>
-   <span data-ttu-id="6f7ad-107">Profil élevé (nécessite Windows 8)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-107">High profile (requires Windows 8)</span></span>

<span data-ttu-id="6f7ad-108">L’encodeur vidéo H. 264 expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-108">The H.264 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="6f7ad-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-109">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="6f7ad-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="6f7ad-111">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="6f7ad-111">Input Types</span></span>

<span data-ttu-id="6f7ad-112">Le type de média d’entrée doit avoir l’un des sous-types suivants :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-112">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="6f7ad-113">**MFVideoFormat_I420**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-113">**MFVideoFormat_I420**</span></span>
-   <span data-ttu-id="6f7ad-114">**MFVideoFormat_IYUV**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-114">**MFVideoFormat_IYUV**</span></span>
-   <span data-ttu-id="6f7ad-115">**MFVideoFormat_NV12**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-115">**MFVideoFormat_NV12**</span></span>
-   <span data-ttu-id="6f7ad-116">**MFVideoFormat_YUY2**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-116">**MFVideoFormat_YUY2**</span></span>
-   <span data-ttu-id="6f7ad-117">**MFVideoFormat_YV12**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-117">**MFVideoFormat_YV12**</span></span>

<span data-ttu-id="6f7ad-118">Pour plus d’informations sur ces sous-types, consultez [GUID sous-type de vidéo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6f7ad-118">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="6f7ad-119">Le type de sortie doit être défini avant le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-119">The output type must be set before the input type.</span></span> <span data-ttu-id="6f7ad-120">Tant que le type de sortie n’est pas défini, la méthode [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) de l’encodeur retourne **MF_E_TRANSFORM_TYPE_NOT_SET**.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-120">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF_E_TRANSFORM_TYPE_NOT_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="6f7ad-121">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="6f7ad-121">Output Types</span></span>

<span data-ttu-id="6f7ad-122">L’encodeur prend en charge un seul sous-type de sortie :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-122">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="6f7ad-123">**MFVideoFormat_H264**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-123">**MFVideoFormat_H264**</span></span>

<span data-ttu-id="6f7ad-124">Définissez les attributs suivants sur le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-124">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f7ad-125">Attribut</span><span class="sxs-lookup"><span data-stu-id="6f7ad-125">Attribute</span></span></th>
<th><span data-ttu-id="6f7ad-126">Description</span><span class="sxs-lookup"><span data-stu-id="6f7ad-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f7ad-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-128">Type principal.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-128">Major type.</span></span> <span data-ttu-id="6f7ad-129">Doit être <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-129">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-131">Sous-type de vidéo.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-131">Video subtype.</span></span> <span data-ttu-id="6f7ad-132">Doit être <strong>MFVideoFormat_H264</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-132">Must be <strong>MFVideoFormat_H264</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-134">Vitesse moyenne des bits encodés, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-134">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="6f7ad-135">Doit être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-135">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-137">Fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-137">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-139">Taille du frame.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-139">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-141">Mode entrelacé.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-141">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-143">Profil d’encodage H. 264.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-143">H.264 encoding profile.</span></span><br/> <span data-ttu-id="6f7ad-144">Les valeurs prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-144">The supported values are:</span></span><br/>
<ul>
<li><span data-ttu-id="6f7ad-145"><strong>eAVEncH264VProfile_Base</strong> (par défaut)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-145"><strong>eAVEncH264VProfile_Base</strong> (default)</span></span></li>
<li><span data-ttu-id="6f7ad-146"><strong>eAVEncH264VProfile_Main</strong></span><span class="sxs-lookup"><span data-stu-id="6f7ad-146"><strong>eAVEncH264VProfile_Main</strong></span></span></li>
<li><span data-ttu-id="6f7ad-147"><strong>eAVEncH264VProfile_High</strong> (nécessite Windows 8)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-147"><strong>eAVEncH264VProfile_High</strong> (requires Windows 8)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-149">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-149">Optional.</span></span> <span data-ttu-id="6f7ad-150">Spécifie le niveau d’encodage H. 264.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-150">Specifies the H.264 encoding level.</span></span><br/> <span data-ttu-id="6f7ad-151">La valeur par défaut est – 1, ce qui indique que l’encodeur va sélectionner le niveau d’encodage.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-151">The default value is –1, indicating that the encoder will select the encoding level.</span></span><br/> <span data-ttu-id="6f7ad-152">Il est recommandé de ne pas définir le niveau dans le type de média et de permettre à l’encodeur de sélectionner le niveau.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-152">It is recommended not to set the level in the media type, and allow the encoder to select the level.</span></span> <span data-ttu-id="6f7ad-153">L’encodeur peut dériver le niveau approprié pour un flux vidéo donné, en tenant compte des contraintes de format et des caractéristiques de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-153">The encoder can derive the proper level for a given video stream, taking into account the format constraints and the characteristics of the video.</span></span> <span data-ttu-id="6f7ad-154">Pour plus d’informations sur les contraintes de profil et de niveau, reportez-vous à l’annexe A de l’ITU-T H. 264.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-154">For more information about profile and level constraints, refer to Annex A of ITU-T H.264.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="6f7ad-156">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-156">Optional.</span></span> <span data-ttu-id="6f7ad-157">Spécifie les proportions en pixels.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-157">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="6f7ad-158">La valeur par défaut est 1:1.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-158">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6f7ad-159">Une fois le type de sortie défini, l’encodeur vidéo met à jour le type en ajoutant l’attribut [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-159">After the output type is set, the video encoder updates the type by adding the [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="6f7ad-160">Cet attribut contient l’en-tête de séquence.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-160">This attribute contains the sequence header.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="6f7ad-161">Propriétés du codec</span><span class="sxs-lookup"><span data-stu-id="6f7ad-161">Codec Properties</span></span>

<span data-ttu-id="6f7ad-162">L’encodeur H. 264 implémente l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) pour définir les paramètres d’encodage.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-162">The H.264 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="6f7ad-163">Il prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-163">It supports the following properties.</span></span>

<span data-ttu-id="6f7ad-164">Pour connaître la configuration requise du codec pour la certification de l’encodeur TPM, **consultez la section** ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-164">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>

<span data-ttu-id="6f7ad-165">Les propriétés suivantes sont prises en charge dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-165">The following properties are supported in Windows 7.</span></span>



| <span data-ttu-id="6f7ad-166">Propriété</span><span class="sxs-lookup"><span data-stu-id="6f7ad-166">Property</span></span>                                                                              | <span data-ttu-id="6f7ad-167">Description</span><span class="sxs-lookup"><span data-stu-id="6f7ad-167">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f7ad-168">**CODECAPI_AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-168">**CODECAPI_AVEncCommonRateControlMode**</span></span>](../directshow/avenccommonratecontrolmode-property.md) | <span data-ttu-id="6f7ad-169">Définit le mode de contrôle de la fréquence.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-169">Sets the rate control mode.</span></span> <span data-ttu-id="6f7ad-170">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-170">See Remarks.</span></span> <span data-ttu-id="6f7ad-171">Le mode par défaut est la vitesse de transmission variable (VBR) sans contrainte.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-171">The default mode is unconstrained variable bit rate (VBR).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="6f7ad-172">**CODECAPI_AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-172">**CODECAPI_AVEncCommonQuality**</span></span>](../directshow/avenccommonquality-property.md)                 | <span data-ttu-id="6f7ad-173">Définit le niveau de qualité.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-173">Sets the quality level.</span></span> <span data-ttu-id="6f7ad-174">Cette propriété s’applique lorsque le mode de contrôle de la fréquence est VBR (**eAVEncCommonRateControlMode_Quality**) basé sur la qualité.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-174">This property applies when the rate control mode is quality-based VBR (**eAVEncCommonRateControlMode_Quality**).</span></span> <span data-ttu-id="6f7ad-175">La plage valide est comprise entre 1 et 100.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-175">The valid range is 1–100.</span></span> <span data-ttu-id="6f7ad-176">La valeur par défaut est 70.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-176">The default value is 70.</span></span> <br/> <span data-ttu-id="6f7ad-177">Pour définir ce paramètre, définissez la propriété avant d’appeler [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="6f7ad-177">To set this parameter, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <br/> <span data-ttu-id="6f7ad-178">Pour définir ce paramètre dans Windows 7, définissez la propriété avant d’appeler [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="6f7ad-178">To set this parameter in Windows 7, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="6f7ad-179">L’encodeur ignore les modifications une fois que le type de sortie est défini.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-179">The encoder ignores changes after the output type is set.</span></span> <br/> <span data-ttu-id="6f7ad-180">Dans Windows 8, cette propriété peut être définie à tout moment pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-180">In Windows 8, this property can be set at any time during encoding.</span></span> <span data-ttu-id="6f7ad-181">Les modifications sont appliquées à partir du frame d’entrée suivant.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-181">Changes are applied starting at the next input frame.</span></span> <br/> <span data-ttu-id="6f7ad-182">En interne, l’encodeur convertit cette propriété en valeur [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-182">Internally, the encoder converts this property to an [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) value.</span></span> <br/> |



 

<span data-ttu-id="6f7ad-183">Les propriétés suivantes nécessitent Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-183">The following properties require Windows 8.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f7ad-184">Propriété</span><span class="sxs-lookup"><span data-stu-id="6f7ad-184">Property</span></span></th>
<th><span data-ttu-id="6f7ad-185">Description</span><span class="sxs-lookup"><span data-stu-id="6f7ad-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f7ad-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span></span></td>
<td><span data-ttu-id="6f7ad-187">Définit le mode de codage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-187">Sets the adaptive encoding mode.</span></span> <span data-ttu-id="6f7ad-188">L’encodeur H. 264 prend en charge les modes suivants dans Windows 8 :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-188">The H.264 encoder supports the following modes in Windows 8:</span></span>
<ul>
<li><span data-ttu-id="6f7ad-189"><strong>eAVEncAdaptiveMode_None</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-189"><strong>eAVEncAdaptiveMode_None</strong>.</span></span> <span data-ttu-id="6f7ad-190">Pas d’encodage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-190">No adaptive encoding.</span></span> <span data-ttu-id="6f7ad-191">(valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="6f7ad-191">(Default.)</span></span></li>
<li><span data-ttu-id="6f7ad-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span></span> <span data-ttu-id="6f7ad-193">Modifiez de manière adaptative la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-193">Adaptively change the frame rate.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="6f7ad-195">Définit la taille de la mémoire tampon, en octets, pour l’encodage à débit binaire constant (CBR).</span><span class="sxs-lookup"><span data-stu-id="6f7ad-195">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="6f7ad-196">La plage valide est [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="6f7ad-196">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="6f7ad-197">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-197">Requires Windows 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="6f7ad-199">Pour l’encodage VBR restreint, spécifie la vitesse à laquelle le &quot; compartiment &quot; de fuite est vidé, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-199">For constrained VBR encoding, specifies the rate at which the &quot;leaky bucket&quot; is drained, in bits per second.</span></span> <span data-ttu-id="6f7ad-200">Cette propriété s’applique lorsque le mode de contrôle de la vitesse est <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-200">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span></span> <br/> <span data-ttu-id="6f7ad-201">La plage valide est [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="6f7ad-201">The valid range is [1 ... 2³²–1].</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="6f7ad-203">Définit la vitesse de transmission moyenne pour le flux binaire encodé, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-203">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <span data-ttu-id="6f7ad-204">Cette propriété est ignorée si le mode de contrôle de la vitesse est <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-204">This property is ignored if the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="6f7ad-205">La plage valide est [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="6f7ad-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="6f7ad-206">En mode CBR et sans contrainte, la vitesse de transmission moyenne détermine la taille finale du fichier.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-206">In CBR and unconstrained VBR modes, the average bit rate determines the final size of the file.</span></span> <span data-ttu-id="6f7ad-207">En mode CBR, la vitesse de transmission moyenne est également la vitesse à laquelle les bits compressés sont vidés du &quot; compartiment perdu. &quot; (pour plus d’informations, consultez <a href="the-leaky-bucket-buffer-model.md">modèle de tampon de compartiment</a>perdu.)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-207">In CBR mode, the average bit rate is also the rate at which compressed bits are drained from the &quot;leaky bucket.&quot; (For more information, see <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>.)</span></span> <br/> <span data-ttu-id="6f7ad-208">Dans Windows 7, la vitesse de transmission moyenne est spécifiée par l’attribut <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-208">In Windows 7, the average bit rate is specified by the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute on the media type.</span></span> <br/> <span data-ttu-id="6f7ad-209">Dans Windows 8, vous pouvez définir la vitesse de transmission moyenne à l’aide de l’attribut <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> ou de la propriété <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-209">In Windows 8, you can set the average bit rate using either the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute or the <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> property.</span></span> <span data-ttu-id="6f7ad-210">Si les deux sont définis, CODECAPI_AVEncCommonMeanBitRate remplace.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-210">If both are set, CODECAPI_AVEncCommonMeanBitRate overrides.</span></span> <span data-ttu-id="6f7ad-211">Dans Windows 8, vous pouvez définir la vitesse de transmission moyenne pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-211">In Windows 8, you can set the average bit rate during encoding.</span></span> <span data-ttu-id="6f7ad-212">Si la vitesse de transmission change, l’encodeur utilise l’encodage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-212">If the bit rate changes, the encoder uses adaptive encoding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="6f7ad-214">Définit le compromis de qualité/vitesse.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-214">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="6f7ad-215">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-215">Valid range:</span></span>
<ul>
<li><span data-ttu-id="6f7ad-216">0 – 33 : faible complexité</span><span class="sxs-lookup"><span data-stu-id="6f7ad-216">0–33: Low complexity</span></span></li>
<li><span data-ttu-id="6f7ad-217">34 – 66 : complexité moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-217">34–66: Medium complexity (default)</span></span></li>
<li><span data-ttu-id="6f7ad-218">67 – 100 : complexité élevée</span><span class="sxs-lookup"><span data-stu-id="6f7ad-218">67–100: High complexity</span></span></li>
</ul>
<br/> <span data-ttu-id="6f7ad-219">Cette valeur affecte la façon dont l’encodeur effectue différentes opérations d’encodage, telles que la compensation de mouvement.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-219">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="6f7ad-220">À des niveaux de complexité plus élevés, l’encodeur s’exécute plus lentement, mais produit une meilleure qualité à la même vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-220">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span></span></td>
<td><span data-ttu-id="6f7ad-222">Active ou désactive le codage arithmétique binaire CABAC (Context-adaptative) pour le codage d’entropie H. 264.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-222">Enables or disables CABAC (context-adaptive binary arithmetic coding) for H.264 entropy coding.</span></span> <span data-ttu-id="6f7ad-223">La valeur par défaut est <strong>VARIANT_FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-223">The default value is <strong>VARIANT_FALSE</strong>.</span></span> <br/> <span data-ttu-id="6f7ad-224">CABAC n’est pas utilisé pour le profil de ligne de base.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-224">CABAC is not used for Baseline profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span></span></td>
<td><span data-ttu-id="6f7ad-226">Définit la valeur de <strong>seq_parameter_set_id</strong> dans l’unité de SPS nal du flux binaire H. 264.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-226">Sets the value of <strong>seq_parameter_set_id</strong> in the SPS NAL unit of the H.264 bitstream.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span></span></td>
<td><span data-ttu-id="6f7ad-228">Définit le nombre maximal de frames B consécutifs dans le flux binaire de sortie.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-228">Sets the maximum number of consecutive B frames in the output bitstream.</span></span> <span data-ttu-id="6f7ad-229">Les valeurs autorisées sont :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-229">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="6f7ad-230">0 : n’utilisez pas les frames B (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="6f7ad-230">0: Do not use B frames (default).</span></span></li>
<li><span data-ttu-id="6f7ad-231">1 : utilisez un frame B.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-231">1: Use one B frame.</span></span></li>
<li><span data-ttu-id="6f7ad-232">2 : utilisez deux frames B.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-232">2: Use two B frames.</span></span></li>
</ul>
<span data-ttu-id="6f7ad-233">Pour définir ce paramètre, définissez la propriété avant d’appeler <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform :: SetOutputType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-233">To set this parameter, set the property before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>.</span></span> <br/> <span data-ttu-id="6f7ad-234">Pour le profil de ligne de base, le nombre de frames B est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-234">For Baseline profile, the number of B frames is always zero.</span></span> <span data-ttu-id="6f7ad-235">L’encodeur remplacera les valeurs autres que zéro.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-235">The encoder will override nonzero values.</span></span><br/> <span data-ttu-id="6f7ad-236">Pour les autres profils H. 264, si cette propriété est différente de zéro, le modèle d’encodage est IBBPBBP, où le nombre maximal de frames B consécutifs est égal à <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-236">For other H.264 profiles, if this property is nonzero, the encoding pattern is IBBPBBP, where the maximum number of consecutive B frames is equal to <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="6f7ad-238">Définit le nombre d’images d’un en-tête GOP sur le suivant, y compris l’ancrage de début, mais pas le suivant.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-238">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="6f7ad-239">La plage valide est [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="6f7ad-239">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="6f7ad-240">Si la valeur est zéro, l’encodeur sélectionne la taille de groupe d’images.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-240">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="6f7ad-241">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-241">The default value is zero.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="6f7ad-243">Définit le nombre de threads de travail utilisés par un encodeur.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-243">Sets the number of worker threads used by a encoder.</span></span><br/> <span data-ttu-id="6f7ad-244">La plage valide est comprise entre 0 et 16.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-244">The valid range is 0–16.</span></span> <span data-ttu-id="6f7ad-245">Si la valeur est zéro, l’encodeur sélectionne le nombre de threads.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-245">If zero, the encoder selects the number of threads.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span></span></td>
<td><span data-ttu-id="6f7ad-247">Indique le type de contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-247">Indicates the type of video content.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="6f7ad-249">Plage valide : 16 – 51.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-249">Valid range: 16–51.</span></span> <span data-ttu-id="6f7ad-250">La valeur par défaut est 24.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-250">The default value is 24.</span></span> <br/> <span data-ttu-id="6f7ad-251">Cette propriété s’applique lorsque le mode de contrôle de la vitesse est <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-251">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="6f7ad-252">Cette propriété configure le même paramètre d’encodage que <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-252">This property configures the same encoding setting as <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span></span> <span data-ttu-id="6f7ad-253">Toutefois, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> permet à l’application de spécifier directement la valeur de QP.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-253">However, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> enables the application to specify the value of QP directly.</span></span> <span data-ttu-id="6f7ad-254">Si les deux propriétés sont définies, AVEncVideoEncodeQP remplace.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-254">If both properties are set, AVEncVideoEncodeQP overrides.</span></span> <br/> <span data-ttu-id="6f7ad-255">La valeur par défaut 24 correspond à la valeur par défaut 70 pour le paramètre <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-255">The default value of 24 corresponds to the default value of 70 for the <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="6f7ad-257">Force l’encodeur à coder le frame suivant comme une image clé.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-257">Forces the encoder to code the next frame as a key frame.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f7ad-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="6f7ad-259">Plage valide : comprise entre 0 et 51.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-259">Valid range: 0–51.</span></span> <span data-ttu-id="6f7ad-260">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-260">The default value is 0.</span></span> <br/> <span data-ttu-id="6f7ad-261">Cette propriété s’applique à tous les modes de contrôle de taux.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-261">This property applies to all rate control modes.</span></span> <span data-ttu-id="6f7ad-262">L’encodeur ne doit pas produire une valeur QP inférieure à ce qui est spécifié par la propriété <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-262">The encoder should not produce a QP value lower than what is specified by the <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f7ad-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="6f7ad-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="6f7ad-264">Active ou désactive le mode faible latence.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-264">Enables or disables low-latency mode.</span></span> <span data-ttu-id="6f7ad-265">Consultez &quot; Multithreading &quot; dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-265">See &quot;Multithreading&quot; in the Remarks section.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="6f7ad-266">Notes</span><span class="sxs-lookup"><span data-stu-id="6f7ad-266">Remarks</span></span>

<span data-ttu-id="6f7ad-267">L’encodeur prend en charge les modes de contrôle de taux suivants.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-267">The encoder supports the following rate control modes.</span></span>



| <span data-ttu-id="6f7ad-268">Mode</span><span class="sxs-lookup"><span data-stu-id="6f7ad-268">Mode</span></span>                                  | <span data-ttu-id="6f7ad-269">Constante</span><span class="sxs-lookup"><span data-stu-id="6f7ad-269">Constant</span></span>                                            | <span data-ttu-id="6f7ad-270">Description</span><span class="sxs-lookup"><span data-stu-id="6f7ad-270">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7ad-271">Débit binaire constant (CBR)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-271">Constant bit rate (CBR)</span></span>               | <span data-ttu-id="6f7ad-272">**eAVEncCommonRateControlMode_CBR**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-272">**eAVEncCommonRateControlMode_CBR**</span></span>                | <span data-ttu-id="6f7ad-273">L’encodeur tente d’obtenir une vitesse binaire constante, à l’aide d’un modèle de « compartiment perdu ».</span><span class="sxs-lookup"><span data-stu-id="6f7ad-273">The encoder tries to achieve a constant bit rate, using a "leaky bucket" model.</span></span> <span data-ttu-id="6f7ad-274">La vitesse de transmission cible est donnée par la propriété [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-274">The target bit rate is given by the [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="6f7ad-275">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-275">Requires Windows 8.</span></span> <br/> |
| <span data-ttu-id="6f7ad-276">Taux de bits variable avec restriction (VBR)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-276">Constrained variable bit rate (VBR)</span></span>   | <span data-ttu-id="6f7ad-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span></span> | <span data-ttu-id="6f7ad-278">L’encodeur utilise un modèle de « compartiment perdu » avec une vitesse de transmission de pic.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-278">The encoder uses a "leaky bucket" model with a peak bit rate.</span></span> <span data-ttu-id="6f7ad-279">La vitesse d’écoulement pour le compartiment avec fuite est donnée par la propriété [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-279">The drain rate for the leaky bucket is given by the [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="6f7ad-280">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-280">Requires Windows 8.</span></span> <br/>     |
| <span data-ttu-id="6f7ad-281">Vitesse de transmission variable (VBR) basée sur la qualité</span><span class="sxs-lookup"><span data-stu-id="6f7ad-281">Quality-based variable bit rate (VBR)</span></span> | <span data-ttu-id="6f7ad-282">**eAVEncCommonRateControlMode_Quality**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-282">**eAVEncCommonRateControlMode_Quality**</span></span>            | <span data-ttu-id="6f7ad-283">L’encodeur tente d’obtenir un niveau de qualité constante, en fonction de la propriété [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-283">The encoder tries to achieve a constant quality level, given by the [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) property.</span></span>                                                                                                           |
| <span data-ttu-id="6f7ad-284">VBR non restreint</span><span class="sxs-lookup"><span data-stu-id="6f7ad-284">Unconstrained VBR</span></span>                     | <span data-ttu-id="6f7ad-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span></span>   | <span data-ttu-id="6f7ad-286">L’encodeur tente d’obtenir le débit cible donné par l’attribut [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) dans le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-286">The encoder tries to achieve the target bitrate given by the [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute in the output media type.</span></span> <span data-ttu-id="6f7ad-287">Il s’agit du mode par défaut ;</span><span class="sxs-lookup"><span data-stu-id="6f7ad-287">This is the default mode.</span></span>                                                              |



 

<span data-ttu-id="6f7ad-288">Les modes CBR et restriction VBR nécessitent Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-288">CBR and constrained VBR modes require Windows 8.</span></span>

<span data-ttu-id="6f7ad-289">Dans Windows 8, l’encodeur définit les attributs suivants sur les exemples de sortie :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-289">In Windows 8, the encoder sets the following attributes on the output samples:</span></span>

-   [<span data-ttu-id="6f7ad-290">MFSampleExtension_DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="6f7ad-290">MFSampleExtension_DecodeTimestamp</span></span>](mfsampleextension-decodetimestamp.md)
-   [<span data-ttu-id="6f7ad-291">MFSampleExtension_VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="6f7ad-291">MFSampleExtension_VideoEncodePictureType</span></span>](mfsampleextension-videoencodepicturetype.md)
-   [<span data-ttu-id="6f7ad-292">MFSampleExtension_VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="6f7ad-292">MFSampleExtension_VideoEncodeQP</span></span>](mfsampleextension-videoencodeqp.md)

> [!Note]  
> <span data-ttu-id="6f7ad-293">Une version précédente de la documentation indiquait incorrectement que l’encodeur est pris en charge sur Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-293">A previous version of the documentation incorrectly stated that the encoder is supported on Windows Server 2008 R2.</span></span>

 

### <a name="multithreading"></a><span data-ttu-id="6f7ad-294">Multithreading</span><span class="sxs-lookup"><span data-stu-id="6f7ad-294">Multithreading</span></span>

<span data-ttu-id="6f7ad-295">Dans Windows 8, l’encodeur prend en charge deux modes d’encodage :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-295">In Windows 8, the encoder supports two encoding modes:</span></span>

-   <span data-ttu-id="6f7ad-296">**Encodage de la tranche.**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-296">**Slice encoding.**</span></span> <span data-ttu-id="6f7ad-297">Dans ce mode, les tranches sont encodées en parallèle.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-297">In this mode, slices are encoded in parallel.</span></span> <span data-ttu-id="6f7ad-298">Chaque tranche est encodée sur un thread différent.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-298">Each slice is encoded on a different thread.</span></span> <span data-ttu-id="6f7ad-299">Ce mode a une latence faible, car une image unique est encodée en parallèle.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-299">This mode has low latency, because a single picture is encoded in parallel.</span></span> <span data-ttu-id="6f7ad-300">Toutefois, cette approche n’est pas mise à l’échelle à mesure que le nombre de cœurs augmente, car le nombre de secteurs est limité par le nombre de lignes bloc macro dans l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-300">However, this approach does not scale as the number of cores increases, because the number of slices is bounded by the number of macroblock rows in the input picture.</span></span>
-   <span data-ttu-id="6f7ad-301">**Encodage à plusieurs frames.**</span><span class="sxs-lookup"><span data-stu-id="6f7ad-301">**Multi-frame encoding.**</span></span> <span data-ttu-id="6f7ad-302">Dans ce mode, l’encodeur accepte plusieurs trames d’entrée et les encode en parallèle.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-302">In this mode, the encoder accepts multiple frames of input and encodes them in parallel.</span></span> <span data-ttu-id="6f7ad-303">Ce mode évolue mieux dans un environnement multicœur, mais introduit une latence plus grande.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-303">This mode scales better in a multicore environment, but introduces more latency.</span></span>

<span data-ttu-id="6f7ad-304">Par défaut, l’encodeur découpe l’encodage pour réduire la latence.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-304">The encoder defaults to slice encoding, to minimize latency.</span></span> <span data-ttu-id="6f7ad-305">Pour activer l’encodage à plusieurs frames, affectez à la propriété [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) la valeur **VARIANT_FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-305">To enable multi-frame encoding, set the [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) property to **VARIANT_FALSE**.</span></span>

<span data-ttu-id="6f7ad-306">Pour définir le nombre de threads de travail utilisés par l’encodeur, définissez la propriété [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="6f7ad-306">To set the number of worker threads used by the encoder, set the [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) property.</span></span>

<span data-ttu-id="6f7ad-307">Dans Windows 7, l’encodeur utilise toujours l’encodage de segment.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-307">In Windows 7, the encoder always uses slice encoding.</span></span>

### <a name="certified-hardware-encoder"></a><span data-ttu-id="6f7ad-308">Encodeur matériel certifié</span><span class="sxs-lookup"><span data-stu-id="6f7ad-308">Certified Hardware Encoder</span></span>

<span data-ttu-id="6f7ad-309">Si un encodeur matériel certifié est présent, il est généralement utilisé à la place de l’encodeur système de la boîte de réception pour Media Foundation scénarios associés.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-309">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="6f7ad-310">Des encodeurs certifiés sont requis pour prendre en charge un certain ensemble de propriétés **ICodecAPI** et peuvent éventuellement prendre en charge un autre ensemble de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-310">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="6f7ad-311">Le processus de certification doit garantir que les propriétés requises sont correctement prises en charge et, si une propriété facultative est prise en charge, qu’elle est également prise en charge correctement.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-311">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="6f7ad-312">Voici l’ensemble des propriétés **ICodecAPI** obligatoires et facultatives pour que les encodeurs passent la certification de l’encodeur TPM.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-312">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

<span data-ttu-id="6f7ad-313">Les propriétés Windows 8 et Windows 8.1 **ICodecAPI** suivantes sont requises :</span><span class="sxs-lookup"><span data-stu-id="6f7ad-313">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are required:</span></span>

-   [<span data-ttu-id="6f7ad-314">CODECAPI_AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="6f7ad-314">CODECAPI_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="6f7ad-315">CODECAPI_AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="6f7ad-315">CODECAPI_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="6f7ad-316">CODECAPI_AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="6f7ad-316">CODECAPI_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="6f7ad-317">CODECAPI_AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="6f7ad-317">CODECAPI_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="6f7ad-318">CODECAPI_AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="6f7ad-318">CODECAPI_AVEncCommonMaxBitRate</span></span>](../directshow/avenccommonmaxbitrate-property.md)
-   [<span data-ttu-id="6f7ad-319">CODECAPI_AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="6f7ad-319">CODECAPI_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="6f7ad-320">CODECAPI_AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="6f7ad-320">CODECAPI_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="6f7ad-321">CODECAPI_AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="6f7ad-321">CODECAPI_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="6f7ad-322">CODECAPI_AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="6f7ad-322">CODECAPI_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

<span data-ttu-id="6f7ad-323">Les propriétés de Windows 8.1 **ICodecAPI** suivantes sont facultatives, mais sont testées dans TPM si elles sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-323">The following Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   [<span data-ttu-id="6f7ad-324">CODECAPI_AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="6f7ad-324">CODECAPI_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
-   [<span data-ttu-id="6f7ad-325">CODECAPI_AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="6f7ad-325">CODECAPI_AVEncVideoLTRBufferControl</span></span>](codecapi-avencvideoltrbuffercontrol.md)
-   [<span data-ttu-id="6f7ad-326">CODECAPI_AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="6f7ad-326">CODECAPI_AVEncVideoMarkLTRFrame</span></span>](codecapi-avencvideomarkltrframe.md)
-   [<span data-ttu-id="6f7ad-327">CODECAPI_AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="6f7ad-327">CODECAPI_AVEncVideoUseLTRFrame</span></span>](codecapi-avencvideouseltrframe.md)
-   [<span data-ttu-id="6f7ad-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="6f7ad-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span></span>](codecapi-avencvideoencodeframetypeqp.md)
-   [<span data-ttu-id="6f7ad-329">CODECAPI_AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="6f7ad-329">CODECAPI_AVEncSliceControlMode</span></span>](codecapi-avencslicecontrolmode.md)
-   [<span data-ttu-id="6f7ad-330">CODECAPI_AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="6f7ad-330">CODECAPI_AVEncSliceControlSize</span></span>](codecapi-avencslicecontrolsize.md)
-   [<span data-ttu-id="6f7ad-331">CODECAPI_AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="6f7ad-331">CODECAPI_AVEncVideoMaxNumRefFrame</span></span>](codecapi-avencvideomaxnumrefframe.md)
-   [<span data-ttu-id="6f7ad-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="6f7ad-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span></span>](codecapi-avencvideomeanabsolutedifference.md)
-   [<span data-ttu-id="6f7ad-333">CODECAPI_AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="6f7ad-333">CODECAPI_AVEncVideoMaxQP</span></span>](codecapi-avencvideomaxqp.md)
-   [<span data-ttu-id="6f7ad-334">CODECAPI_AVEncVideoROIEnabled</span><span class="sxs-lookup"><span data-stu-id="6f7ad-334">CODECAPI_AVEncVideoROIEnabled</span></span>](codecapi-avencvideoroienabled.md)
-   <span data-ttu-id="6f7ad-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dynamique)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Dynamic)</span></span>
-   [<span data-ttu-id="6f7ad-336">CODECAPI_AVEncH264CABACEnable</span><span class="sxs-lookup"><span data-stu-id="6f7ad-336">CODECAPI_AVEncH264CABACEnable</span></span>](codecapi-avench264cabacenable.md)

<span data-ttu-id="6f7ad-337">Les propriétés Windows 8 et Windows 8.1 **ICodecAPI** suivantes sont facultatives, mais sont testées dans TPM si elles sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-337">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   <span data-ttu-id="6f7ad-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (statique)</span><span class="sxs-lookup"><span data-stu-id="6f7ad-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Static)</span></span>
-   [<span data-ttu-id="6f7ad-339">CODECAPI_AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="6f7ad-339">CODECAPI_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

<span data-ttu-id="6f7ad-340">Les propriétés **ICodecAPI** suivantes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-340">The following **ICodecAPI** properties are optional.</span></span> <span data-ttu-id="6f7ad-341">Ils ne sont pas testés dans TPM.</span><span class="sxs-lookup"><span data-stu-id="6f7ad-341">They are not tested in HCK.</span></span>

-   [<span data-ttu-id="6f7ad-342">CODECAPI_AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="6f7ad-342">CODECAPI_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a><span data-ttu-id="6f7ad-343">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f7ad-343">Requirements</span></span>



| <span data-ttu-id="6f7ad-344">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f7ad-344">Requirement</span></span> | <span data-ttu-id="6f7ad-345">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f7ad-345">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7ad-346">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7ad-346">Minimum supported client</span></span><br/> | <span data-ttu-id="6f7ad-347">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f7ad-347">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6f7ad-348">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7ad-348">Minimum supported server</span></span><br/> | <span data-ttu-id="6f7ad-349">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f7ad-349">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6f7ad-350">DLL</span><span class="sxs-lookup"><span data-stu-id="6f7ad-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f7ad-351"><dt>Mfh264enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f7ad-351"><dt>Mfh264enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f7ad-352">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f7ad-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f7ad-353">Objets codec</span><span class="sxs-lookup"><span data-stu-id="6f7ad-353">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="6f7ad-354">Prise en charge MPEG-4 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f7ad-354">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6f7ad-355">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6f7ad-355">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6f7ad-356">Types de média vidéo</span><span class="sxs-lookup"><span data-stu-id="6f7ad-356">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
