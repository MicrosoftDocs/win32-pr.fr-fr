---
description: Cette rubrique fournit des informations sur le codec TIFF natif disponible via WIC (Windows Imaging Component).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Vue d’ensemble du format TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521150"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="1cb1b-103">Vue d’ensemble du format TIFF</span><span class="sxs-lookup"><span data-stu-id="1cb1b-103">TIFF Format Overview</span></span>

<span data-ttu-id="1cb1b-104">Cette rubrique fournit des informations sur le codec TIFF natif disponible via WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="1cb1b-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="1cb1b-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="1cb1b-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="1cb1b-106">Encodage</span><span class="sxs-lookup"><span data-stu-id="1cb1b-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="1cb1b-107">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="1cb1b-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="1cb1b-108">Décodage</span><span class="sxs-lookup"><span data-stu-id="1cb1b-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="1cb1b-109">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="1cb1b-109">Codec Identity</span></span>

<span data-ttu-id="1cb1b-110">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-110">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="1cb1b-111">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="1cb1b-111">Formal Name(s)</span></span>         | <span data-ttu-id="1cb1b-112">format TIFF (Tagged Image File Format)</span><span class="sxs-lookup"><span data-stu-id="1cb1b-112">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="1cb1b-113">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="1cb1b-113">File Name Extension(s)</span></span> | <span data-ttu-id="1cb1b-114">TIFF, TIF</span><span class="sxs-lookup"><span data-stu-id="1cb1b-114">tiff, tif</span></span>                       |
| <span data-ttu-id="1cb1b-115">Type (s) MIME</span><span class="sxs-lookup"><span data-stu-id="1cb1b-115">MIME type(s)</span></span>           | <span data-ttu-id="1cb1b-116">image/TIFF, image/TIF</span><span class="sxs-lookup"><span data-stu-id="1cb1b-116">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="1cb1b-117">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="1cb1b-117">Specification Support</span></span>  | <span data-ttu-id="1cb1b-118">Spécification TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="1cb1b-118">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="1cb1b-119">Le tableau suivant répertorie les GUID utilisés pour identifier les composants natifs du codec TIFF.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-119">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="1cb1b-120">Composant</span><span class="sxs-lookup"><span data-stu-id="1cb1b-120">Component</span></span>        | <span data-ttu-id="1cb1b-121">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="1cb1b-121">Friendly Name</span></span>             | <span data-ttu-id="1cb1b-122">GUID</span><span class="sxs-lookup"><span data-stu-id="1cb1b-122">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="1cb1b-123">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="1cb1b-123">Container Format</span></span> | <span data-ttu-id="1cb1b-124">GUID \_ ContainerFormatTiff</span><span class="sxs-lookup"><span data-stu-id="1cb1b-124">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="1cb1b-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="1cb1b-125">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="1cb1b-126">Décodeur</span><span class="sxs-lookup"><span data-stu-id="1cb1b-126">Decoder</span></span>          | <span data-ttu-id="1cb1b-127">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="1cb1b-127">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="1cb1b-128">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="1cb1b-128">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="1cb1b-129">Encodeur</span><span class="sxs-lookup"><span data-stu-id="1cb1b-129">Encoder</span></span>          | <span data-ttu-id="1cb1b-130">CLSID \_ WICTiffEncoder</span><span class="sxs-lookup"><span data-stu-id="1cb1b-130">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="1cb1b-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="1cb1b-131">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="1cb1b-132">Encodage</span><span class="sxs-lookup"><span data-stu-id="1cb1b-132">Encoding</span></span>

<span data-ttu-id="1cb1b-133">L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="1cb1b-134">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="1cb1b-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="1cb1b-135">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="1cb1b-135">Encoder Options</span></span>

<span data-ttu-id="1cb1b-136">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="1cb1b-137">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="1cb1b-138">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="1cb1b-139">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1cb1b-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="1cb1b-140">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="1cb1b-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="1cb1b-141">Le codec TIFF utilise les options de base du WIC.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-141">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="1cb1b-142">Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec TIFF natif.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-142">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="1cb1b-143">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="1cb1b-143">Property Name</span></span>         | <span data-ttu-id="1cb1b-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1cb1b-144">VARTYPE</span></span> | <span data-ttu-id="1cb1b-145">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="1cb1b-145">Value Range</span></span> | <span data-ttu-id="1cb1b-146">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="1cb1b-146">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="1cb1b-147">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="1cb1b-147">CompressionQuality</span></span>    | <span data-ttu-id="1cb1b-148">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="1cb1b-148">VT\_R4</span></span>  | <span data-ttu-id="1cb1b-149">0-1,0</span><span class="sxs-lookup"><span data-stu-id="1cb1b-149">0 - 1.0</span></span>     | <span data-ttu-id="1cb1b-150">0</span><span class="sxs-lookup"><span data-stu-id="1cb1b-150">0</span></span>                |
| <span data-ttu-id="1cb1b-151">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="1cb1b-151">TiffCompressionMethod</span></span> | <span data-ttu-id="1cb1b-152">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="1cb1b-152">VT\_UI1</span></span> | [<span data-ttu-id="1cb1b-153">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="1cb1b-153">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="1cb1b-154">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="1cb1b-154">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="1cb1b-155">Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="1cb1b-156">Option CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="1cb1b-156">CompressionQuality Option</span></span>

<span data-ttu-id="1cb1b-157">Spécifie la qualité de compression souhaitée.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-157">Specifies the desired compression quality.</span></span> <span data-ttu-id="1cb1b-158">0,0 indique le schéma de compression le moins efficace disponible.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-158">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="1cb1b-159">En règle générale, ce schéma entraîne un encodage plus rapide mais une sortie plus grande.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-159">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="1cb1b-160">La valeur 1,0 spécifie le schéma de compression le plus efficace disponible.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-160">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="1cb1b-161">En règle générale, ce schéma entraîne un encodage plus long, mais produit une sortie plus petite.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-161">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="1cb1b-162">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-162">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="1cb1b-163">Option TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="1cb1b-163">TiffCompressionMethod Option</span></span>

<span data-ttu-id="1cb1b-164">Spécifie la méthode de compression TIFF.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-164">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="1cb1b-165">La valeur par défaut est [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span><span class="sxs-lookup"><span data-stu-id="1cb1b-165">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="1cb1b-166">Décodage</span><span class="sxs-lookup"><span data-stu-id="1cb1b-166">Decoding</span></span>

<span data-ttu-id="1cb1b-167">Les API de décodage WIC sont conçues pour être indépendantes du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="1cb1b-167">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="1cb1b-168">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="1cb1b-168">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="1cb1b-169">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="1cb1b-169">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
