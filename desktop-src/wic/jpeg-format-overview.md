---
description: Cette rubrique fournit des informations sur le codec JPEG natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Vue d’ensemble du format JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444190"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="2da55-103">Vue d’ensemble du format JPEG</span><span class="sxs-lookup"><span data-stu-id="2da55-103">JPEG Format Overview</span></span>

<span data-ttu-id="2da55-104">Cette rubrique fournit des informations sur le codec JPEG natif disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="2da55-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="2da55-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="2da55-105">Codec Identity</span></span>

<span data-ttu-id="2da55-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="2da55-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="2da55-107">Composant</span><span class="sxs-lookup"><span data-stu-id="2da55-107">Component</span></span>            | <span data-ttu-id="2da55-108">Description</span><span class="sxs-lookup"><span data-stu-id="2da55-108">Description</span></span>                             |
|------------------------|-----------------------------------------|
| <span data-ttu-id="2da55-109">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="2da55-109">Formal Name(s)</span></span>         | <span data-ttu-id="2da55-110">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="2da55-110">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="2da55-111">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="2da55-111">File Name Extension(s)</span></span> | <span data-ttu-id="2da55-112">JPE, JPEG, jpg</span><span class="sxs-lookup"><span data-stu-id="2da55-112">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="2da55-113">type MIME</span><span class="sxs-lookup"><span data-stu-id="2da55-113">MIME type</span></span>              | <span data-ttu-id="2da55-114">image/JPEG, image/JPE, image/jpg</span><span class="sxs-lookup"><span data-stu-id="2da55-114">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="2da55-115">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="2da55-115">Specification Support</span></span>  | <span data-ttu-id="2da55-116">Spécification JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="2da55-116">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="2da55-117">Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec JPEG natifs.</span><span class="sxs-lookup"><span data-stu-id="2da55-117">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="2da55-118">Composant</span><span class="sxs-lookup"><span data-stu-id="2da55-118">Component</span></span>        | <span data-ttu-id="2da55-119">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="2da55-119">Friendly Name</span></span>             | <span data-ttu-id="2da55-120">GUID</span><span class="sxs-lookup"><span data-stu-id="2da55-120">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="2da55-121">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="2da55-121">Container Format</span></span> | <span data-ttu-id="2da55-122">GUID \_ ContainerFormatJpeg</span><span class="sxs-lookup"><span data-stu-id="2da55-122">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="2da55-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="2da55-123">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="2da55-124">Décodeur</span><span class="sxs-lookup"><span data-stu-id="2da55-124">Decoder</span></span>          | <span data-ttu-id="2da55-125">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="2da55-125">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="2da55-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="2da55-126">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="2da55-127">Encodeur</span><span class="sxs-lookup"><span data-stu-id="2da55-127">Encoder</span></span>          | <span data-ttu-id="2da55-128">CLSID \_ WICJpegEncoder</span><span class="sxs-lookup"><span data-stu-id="2da55-128">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="2da55-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="2da55-129">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="2da55-130">Encodage</span><span class="sxs-lookup"><span data-stu-id="2da55-130">Encoding</span></span>

<span data-ttu-id="2da55-131">L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="2da55-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="2da55-132">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="2da55-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="2da55-133">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="2da55-133">Encoder Options</span></span>

<span data-ttu-id="2da55-134">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="2da55-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="2da55-135">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="2da55-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="2da55-136">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="2da55-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="2da55-137">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2da55-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="2da55-138">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="2da55-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="2da55-139">Le codec JPEG utilise les options de base du WIC.</span><span class="sxs-lookup"><span data-stu-id="2da55-139">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="2da55-140">Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec JPEG natif.</span><span class="sxs-lookup"><span data-stu-id="2da55-140">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="2da55-141">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="2da55-141">Property Name</span></span>                                        | <span data-ttu-id="2da55-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2da55-142">VARTYPE</span></span>           | <span data-ttu-id="2da55-143">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="2da55-143">Value Range</span></span>                                                                       | <span data-ttu-id="2da55-144">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="2da55-144">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="2da55-145">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="2da55-145">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="2da55-146">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="2da55-146">VT\_R4</span></span>            | <span data-ttu-id="2da55-147">0-1,0</span><span class="sxs-lookup"><span data-stu-id="2da55-147">0 - 1.0</span></span>                                                                           | <span data-ttu-id="2da55-148">0.9</span><span class="sxs-lookup"><span data-stu-id="2da55-148">0.9</span></span>                                                                            |
| [<span data-ttu-id="2da55-149">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="2da55-149">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="2da55-150">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="2da55-150">VT\_UI1</span></span>           | [<span data-ttu-id="2da55-151">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="2da55-151">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="2da55-152">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="2da55-152">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="2da55-153">Luminance</span><span class="sxs-lookup"><span data-stu-id="2da55-153">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="2da55-154">\_Groupe VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="2da55-154">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="2da55-155">64 entrées (DCT)</span><span class="sxs-lookup"><span data-stu-id="2da55-155">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="2da55-156">Table de luminance par défaut.</span><span class="sxs-lookup"><span data-stu-id="2da55-156">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="2da55-157">Chrominance</span><span class="sxs-lookup"><span data-stu-id="2da55-157">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="2da55-158">\_Groupe VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="2da55-158">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="2da55-159">64 entrées (DCT)</span><span class="sxs-lookup"><span data-stu-id="2da55-159">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="2da55-160">Table de chrominance par défaut.</span><span class="sxs-lookup"><span data-stu-id="2da55-160">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="2da55-161">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="2da55-161">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="2da55-162">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="2da55-162">VT\_UI1</span></span>           | [<span data-ttu-id="2da55-163">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="2da55-163">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="2da55-164">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="2da55-164">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="2da55-165">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="2da55-165">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="2da55-166">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="2da55-166">VT\_BOOL</span></span>          | <span data-ttu-id="2da55-167">**True** / **Valeur false**</span><span class="sxs-lookup"><span data-stu-id="2da55-167">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="2da55-168">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="2da55-168">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="2da55-169">Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="2da55-169">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="2da55-170">Option ImageQuality</span><span class="sxs-lookup"><span data-stu-id="2da55-170">ImageQuality Option</span></span>

<span data-ttu-id="2da55-171">Spécifie la fidélité de l’image souhaitée.</span><span class="sxs-lookup"><span data-stu-id="2da55-171">Specifies the desired image fidelity.</span></span> <span data-ttu-id="2da55-172">0,0 indique la fidélité la plus faible possible et 1,0 spécifie la fidélité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="2da55-172">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="2da55-173">La valeur par défaut est 0,9.</span><span class="sxs-lookup"><span data-stu-id="2da55-173">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="2da55-174">Option BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="2da55-174">BitmapTransform Option</span></span>

<span data-ttu-id="2da55-175">Spécifie comment l’image doit être transformée lors du décodage de l’image.</span><span class="sxs-lookup"><span data-stu-id="2da55-175">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="2da55-176">Cette option doit être définie sur l’une des valeurs d’énumération [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="2da55-176">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="2da55-177">La valeur par défaut est [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span><span class="sxs-lookup"><span data-stu-id="2da55-177">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="2da55-178">Option de luminance</span><span class="sxs-lookup"><span data-stu-id="2da55-178">Luminance Option</span></span>

<span data-ttu-id="2da55-179">Spécifie la table de niveau de luminosité en nuances de gris à utiliser pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="2da55-179">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="2da55-180">Chrominance (option)</span><span class="sxs-lookup"><span data-stu-id="2da55-180">Chrominance Option</span></span>

<span data-ttu-id="2da55-181">Spécifie la table de chrominance à utiliser pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="2da55-181">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="2da55-182">Option JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="2da55-182">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="2da55-183">Spécifie le ratio d’échantillonnage à utiliser pour l’encodage YCrCb.</span><span class="sxs-lookup"><span data-stu-id="2da55-183">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="2da55-184">La valeur par défaut est [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="2da55-184">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="2da55-185">Option SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="2da55-185">SuppressApp0 Option</span></span>

<span data-ttu-id="2da55-186">Spécifie s’il faut supprimer l’écriture des métadonnées APP0 lors de l’encodage des données d’image.</span><span class="sxs-lookup"><span data-stu-id="2da55-186">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="2da55-187">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2da55-187">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="2da55-188">Décodage</span><span class="sxs-lookup"><span data-stu-id="2da55-188">Decoding</span></span>

<span data-ttu-id="2da55-189">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="2da55-189">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="2da55-190">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="2da55-190">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="2da55-191">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="2da55-191">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="2da55-192">Le codec JPEG natif prend également en charge l' [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sur le décodage de trame qui ajoute des options avancée pour décoder un flux d’image.</span><span class="sxs-lookup"><span data-stu-id="2da55-192">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="2da55-193">Pour plus d’informations sur ces options avancées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="2da55-193">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
