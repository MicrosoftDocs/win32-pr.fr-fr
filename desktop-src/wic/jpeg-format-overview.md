---
description: Cette rubrique fournit des informations sur le codec JPEG natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Vue d’ensemble du format JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953d1d6a02e47b41d1b7cf872f3381cd640151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519713"
---
# <a name="jpeg-format-overview"></a><span data-ttu-id="5085b-103">Vue d’ensemble du format JPEG</span><span class="sxs-lookup"><span data-stu-id="5085b-103">JPEG Format Overview</span></span>

<span data-ttu-id="5085b-104">Cette rubrique fournit des informations sur le codec JPEG natif disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="5085b-104">This topic provides information about the native JPEG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="5085b-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="5085b-105">Codec Identity</span></span>

<span data-ttu-id="5085b-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="5085b-106">The following table provides codec identification information.</span></span>



|                        |                                         |
|------------------------|-----------------------------------------|
| <span data-ttu-id="5085b-107">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="5085b-107">Formal Name(s)</span></span>         | <span data-ttu-id="5085b-108">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="5085b-108">Joint Photographic Experts Group (JPEG)</span></span> |
| <span data-ttu-id="5085b-109">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="5085b-109">File Name Extension(s)</span></span> | <span data-ttu-id="5085b-110">JPE, JPEG, jpg</span><span class="sxs-lookup"><span data-stu-id="5085b-110">jpe, jpeg, jpg</span></span>                          |
| <span data-ttu-id="5085b-111">type MIME</span><span class="sxs-lookup"><span data-stu-id="5085b-111">MIME type</span></span>              | <span data-ttu-id="5085b-112">image/JPEG, image/JPE, image/jpg</span><span class="sxs-lookup"><span data-stu-id="5085b-112">image/jpeg, image/jpe, image/jpg</span></span>        |
| <span data-ttu-id="5085b-113">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="5085b-113">Specification Support</span></span>  | <span data-ttu-id="5085b-114">Spécification JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="5085b-114">JFIF Specification 1.02</span></span>                 |



 

<span data-ttu-id="5085b-115">Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec JPEG natifs.</span><span class="sxs-lookup"><span data-stu-id="5085b-115">The following table lists the GUIDs used to identify the native JPEG codec components.</span></span>



| <span data-ttu-id="5085b-116">Composant</span><span class="sxs-lookup"><span data-stu-id="5085b-116">Component</span></span>        | <span data-ttu-id="5085b-117">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="5085b-117">Friendly Name</span></span>             | <span data-ttu-id="5085b-118">GUID</span><span class="sxs-lookup"><span data-stu-id="5085b-118">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="5085b-119">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="5085b-119">Container Format</span></span> | <span data-ttu-id="5085b-120">GUID \_ ContainerFormatJpeg</span><span class="sxs-lookup"><span data-stu-id="5085b-120">GUID\_ContainerFormatJpeg</span></span> | <span data-ttu-id="5085b-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span><span class="sxs-lookup"><span data-stu-id="5085b-121">19e4a5aa-5662-4fc5-a0c01758028e1057</span></span> |
| <span data-ttu-id="5085b-122">Décodeur</span><span class="sxs-lookup"><span data-stu-id="5085b-122">Decoder</span></span>          | <span data-ttu-id="5085b-123">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="5085b-123">CLSID\_WICJpegDecoder</span></span>     | <span data-ttu-id="5085b-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span><span class="sxs-lookup"><span data-stu-id="5085b-124">9456a480-e88b-43ea-9e730b2d9b71b1ca</span></span> |
| <span data-ttu-id="5085b-125">Encodeur</span><span class="sxs-lookup"><span data-stu-id="5085b-125">Encoder</span></span>          | <span data-ttu-id="5085b-126">CLSID \_ WICJpegEncoder</span><span class="sxs-lookup"><span data-stu-id="5085b-126">CLSID\_WICJpegEncoder</span></span>     | <span data-ttu-id="5085b-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span><span class="sxs-lookup"><span data-stu-id="5085b-127">1a34f5c1-4a5a-46dc-b6441f4567e7a676</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="5085b-128">Encodage</span><span class="sxs-lookup"><span data-stu-id="5085b-128">Encoding</span></span>

<span data-ttu-id="5085b-129">L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="5085b-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="5085b-130">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="5085b-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="5085b-131">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="5085b-131">Encoder Options</span></span>

<span data-ttu-id="5085b-132">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="5085b-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="5085b-133">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="5085b-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="5085b-134">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="5085b-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="5085b-135">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5085b-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="5085b-136">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="5085b-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="5085b-137">Le codec JPEG utilise les options de base du WIC.</span><span class="sxs-lookup"><span data-stu-id="5085b-137">The JPEG codec uses basic WIC options.</span></span> <span data-ttu-id="5085b-138">Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec JPEG natif.</span><span class="sxs-lookup"><span data-stu-id="5085b-138">The following table lists the WIC encoder options supported by the native JPEG codec.</span></span>



| <span data-ttu-id="5085b-139">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="5085b-139">Property Name</span></span>                                        | <span data-ttu-id="5085b-140">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5085b-140">VARTYPE</span></span>           | <span data-ttu-id="5085b-141">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="5085b-141">Value Range</span></span>                                                                       | <span data-ttu-id="5085b-142">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="5085b-142">Default Value</span></span>                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="5085b-143">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="5085b-143">ImageQuality</span></span>](#imagequality-option)                 | <span data-ttu-id="5085b-144">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="5085b-144">VT\_R4</span></span>            | <span data-ttu-id="5085b-145">0-1,0</span><span class="sxs-lookup"><span data-stu-id="5085b-145">0 - 1.0</span></span>                                                                           | <span data-ttu-id="5085b-146">0.9</span><span class="sxs-lookup"><span data-stu-id="5085b-146">0.9</span></span>                                                                            |
| [<span data-ttu-id="5085b-147">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="5085b-147">BitmapTransform</span></span>](#bitmaptransform-option)           | <span data-ttu-id="5085b-148">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="5085b-148">VT\_UI1</span></span>           | [<span data-ttu-id="5085b-149">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="5085b-149">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [<span data-ttu-id="5085b-150">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="5085b-150">**WICBitmapTransformRotate0**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [<span data-ttu-id="5085b-151">Luminance</span><span class="sxs-lookup"><span data-stu-id="5085b-151">Luminance</span></span>](#luminance-option)                       | <span data-ttu-id="5085b-152">\_Groupe VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="5085b-152">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="5085b-153">64 entrées (DCT)</span><span class="sxs-lookup"><span data-stu-id="5085b-153">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="5085b-154">Table de luminance par défaut.</span><span class="sxs-lookup"><span data-stu-id="5085b-154">Default luminance table.</span></span>                                                       |
| [<span data-ttu-id="5085b-155">Chrominance</span><span class="sxs-lookup"><span data-stu-id="5085b-155">Chrominance</span></span>](#chrominance-option)                   | <span data-ttu-id="5085b-156">\_Groupe VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="5085b-156">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="5085b-157">64 entrées (DCT)</span><span class="sxs-lookup"><span data-stu-id="5085b-157">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="5085b-158">Table de chrominance par défaut.</span><span class="sxs-lookup"><span data-stu-id="5085b-158">Default chrominance table.</span></span>                                                     |
| [<span data-ttu-id="5085b-159">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="5085b-159">JpegYCrCbSubsampling</span></span>](#jpegycrcbsubsampling-option) | <span data-ttu-id="5085b-160">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="5085b-160">VT\_UI1</span></span>           | [<span data-ttu-id="5085b-161">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="5085b-161">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [<span data-ttu-id="5085b-162">**WICJpegYCrCbSubsampling420**</span><span class="sxs-lookup"><span data-stu-id="5085b-162">**WICJpegYCrCbSubsampling420**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [<span data-ttu-id="5085b-163">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="5085b-163">SuppressApp0</span></span>](/windows)                       | <span data-ttu-id="5085b-164">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5085b-164">VT\_BOOL</span></span>          | <span data-ttu-id="5085b-165">**True** / **Valeur false**</span><span class="sxs-lookup"><span data-stu-id="5085b-165">**TRUE**/**FALSE**</span></span>                                                                | <span data-ttu-id="5085b-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5085b-166">**FALSE**</span></span>                                                                      |



 

<span data-ttu-id="5085b-167">Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5085b-167">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="imagequality-option"></a><span data-ttu-id="5085b-168">Option ImageQuality</span><span class="sxs-lookup"><span data-stu-id="5085b-168">ImageQuality Option</span></span>

<span data-ttu-id="5085b-169">Spécifie la fidélité de l’image souhaitée.</span><span class="sxs-lookup"><span data-stu-id="5085b-169">Specifies the desired image fidelity.</span></span> <span data-ttu-id="5085b-170">0,0 indique la fidélité la plus faible possible et 1,0 spécifie la fidélité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="5085b-170">0.0 indicates the lowest possible fidelity and 1.0 specifies the highest fidelity.</span></span>

<span data-ttu-id="5085b-171">La valeur par défaut est 0,9.</span><span class="sxs-lookup"><span data-stu-id="5085b-171">The default value is 0.9.</span></span>

### <a name="bitmaptransform-option"></a><span data-ttu-id="5085b-172">Option BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="5085b-172">BitmapTransform Option</span></span>

<span data-ttu-id="5085b-173">Spécifie comment l’image doit être transformée lors du décodage de l’image.</span><span class="sxs-lookup"><span data-stu-id="5085b-173">Specifies how the image is to be transformed during image decoding.</span></span> <span data-ttu-id="5085b-174">Cette option doit être définie sur l’une des valeurs d’énumération [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .</span><span class="sxs-lookup"><span data-stu-id="5085b-174">This option must be set to one of the [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) enumeration values.</span></span>

<span data-ttu-id="5085b-175">La valeur par défaut est [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span><span class="sxs-lookup"><span data-stu-id="5085b-175">The default value is [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).</span></span>

### <a name="luminance-option"></a><span data-ttu-id="5085b-176">Option de luminance</span><span class="sxs-lookup"><span data-stu-id="5085b-176">Luminance Option</span></span>

<span data-ttu-id="5085b-177">Spécifie la table de niveau de luminosité en nuances de gris à utiliser pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="5085b-177">Specifies the grayscale brightness level table to use for encoding.</span></span>

### <a name="chrominance-option"></a><span data-ttu-id="5085b-178">Chrominance (option)</span><span class="sxs-lookup"><span data-stu-id="5085b-178">Chrominance Option</span></span>

<span data-ttu-id="5085b-179">Spécifie la table de chrominance à utiliser pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="5085b-179">Specifies the chrominance table to use for encoding.</span></span>

### <a name="jpegycrcbsubsampling-option"></a><span data-ttu-id="5085b-180">Option JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="5085b-180">JpegYCrCbSubsampling Option</span></span>

<span data-ttu-id="5085b-181">Spécifie le ratio d’échantillonnage à utiliser pour l’encodage YCrCb.</span><span class="sxs-lookup"><span data-stu-id="5085b-181">Specifies the subsampling ratio to use for YCrCb encoding.</span></span>

<span data-ttu-id="5085b-182">La valeur par défaut est [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span><span class="sxs-lookup"><span data-stu-id="5085b-182">The default value is [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).</span></span>

### <a name="suppressapp0-option"></a><span data-ttu-id="5085b-183">Option SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="5085b-183">SuppressApp0 Option</span></span>

<span data-ttu-id="5085b-184">Spécifie s’il faut supprimer l’écriture des métadonnées APP0 lors de l’encodage des données d’image.</span><span class="sxs-lookup"><span data-stu-id="5085b-184">Specifies whether to suppress the write of App0 metadata while encoding the image data.</span></span>

<span data-ttu-id="5085b-185">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="5085b-185">The default value is **FALSE**.</span></span>

## <a name="decoding"></a><span data-ttu-id="5085b-186">Décodage</span><span class="sxs-lookup"><span data-stu-id="5085b-186">Decoding</span></span>

<span data-ttu-id="5085b-187">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="5085b-187">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="5085b-188">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="5085b-188">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="5085b-189">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="5085b-189">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="5085b-190">Le codec JPEG natif prend également en charge l' [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sur le décodage de trame qui ajoute des options avancée pour décoder un flux d’image.</span><span class="sxs-lookup"><span data-stu-id="5085b-190">The native JPEG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advaced options for decoding an image stream.</span></span> <span data-ttu-id="5085b-191">Pour plus d’informations sur ces options avancées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="5085b-191">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
