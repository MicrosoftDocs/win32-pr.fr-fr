---
description: Cette rubrique fournit des informations sur le codec TIFF natif disponible via WIC (Windows Imaging Component).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Vue d’ensemble du format TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444420"
---
# <a name="tiff-format-overview"></a><span data-ttu-id="3dd3e-103">Vue d’ensemble du format TIFF</span><span class="sxs-lookup"><span data-stu-id="3dd3e-103">TIFF Format Overview</span></span>

<span data-ttu-id="3dd3e-104">Cette rubrique fournit des informations sur le codec TIFF natif disponible via WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="3dd3e-104">This topic provides information about the native TIFF codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="3dd3e-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="3dd3e-105">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="3dd3e-106">Encodage</span><span class="sxs-lookup"><span data-stu-id="3dd3e-106">Encoding</span></span>](#encoding)
    -   [<span data-ttu-id="3dd3e-107">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="3dd3e-107">Encoder Options</span></span>](#encoder-options)
-   [<span data-ttu-id="3dd3e-108">Décodage</span><span class="sxs-lookup"><span data-stu-id="3dd3e-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="3dd3e-109">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="3dd3e-109">Codec Identity</span></span>

<span data-ttu-id="3dd3e-110">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-110">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="3dd3e-111">Composant</span><span class="sxs-lookup"><span data-stu-id="3dd3e-111">Component</span></span>            |   <span data-ttu-id="3dd3e-112">Description</span><span class="sxs-lookup"><span data-stu-id="3dd3e-112">Description</span></span>                   |
|------------------------|---------------------------------|
| <span data-ttu-id="3dd3e-113">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="3dd3e-113">Formal Name(s)</span></span>         | <span data-ttu-id="3dd3e-114">format TIFF (Tagged Image File Format)</span><span class="sxs-lookup"><span data-stu-id="3dd3e-114">Tagged Image File Format (TIFF)</span></span> |
| <span data-ttu-id="3dd3e-115">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="3dd3e-115">File Name Extension(s)</span></span> | <span data-ttu-id="3dd3e-116">TIFF, TIF</span><span class="sxs-lookup"><span data-stu-id="3dd3e-116">tiff, tif</span></span>                       |
| <span data-ttu-id="3dd3e-117">Type (s) MIME</span><span class="sxs-lookup"><span data-stu-id="3dd3e-117">MIME type(s)</span></span>           | <span data-ttu-id="3dd3e-118">image/TIFF, image/TIF</span><span class="sxs-lookup"><span data-stu-id="3dd3e-118">image/tiff, image/tif</span></span>           |
| <span data-ttu-id="3dd3e-119">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="3dd3e-119">Specification Support</span></span>  | <span data-ttu-id="3dd3e-120">Spécification TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="3dd3e-120">TIFF Specification 6.0</span></span>          |



 

<span data-ttu-id="3dd3e-121">Le tableau suivant répertorie les GUID utilisés pour identifier les composants natifs du codec TIFF.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-121">The following table lists the GUIDs used to identify the native TIFF codec components.</span></span>



| <span data-ttu-id="3dd3e-122">Composant</span><span class="sxs-lookup"><span data-stu-id="3dd3e-122">Component</span></span>        | <span data-ttu-id="3dd3e-123">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="3dd3e-123">Friendly Name</span></span>             | <span data-ttu-id="3dd3e-124">GUID</span><span class="sxs-lookup"><span data-stu-id="3dd3e-124">GUID</span></span>                                 |
|------------------|---------------------------|--------------------------------------|
| <span data-ttu-id="3dd3e-125">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="3dd3e-125">Container Format</span></span> | <span data-ttu-id="3dd3e-126">GUID \_ ContainerFormatTiff</span><span class="sxs-lookup"><span data-stu-id="3dd3e-126">GUID\_ContainerFormatTiff</span></span> | <span data-ttu-id="3dd3e-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span><span class="sxs-lookup"><span data-stu-id="3dd3e-127">163bcc30-e2e9-4f0b-961da3e9fdb788a3</span></span>  |
| <span data-ttu-id="3dd3e-128">Décodeur</span><span class="sxs-lookup"><span data-stu-id="3dd3e-128">Decoder</span></span>          | <span data-ttu-id="3dd3e-129">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="3dd3e-129">CLSID\_WICTiffDecoder</span></span>     | <span data-ttu-id="3dd3e-130">b54e85d9-fe23-499f-8b886acea7137502b</span><span class="sxs-lookup"><span data-stu-id="3dd3e-130">b54e85d9-fe23-499f-8b886acea7137502b</span></span> |
| <span data-ttu-id="3dd3e-131">Encodeur</span><span class="sxs-lookup"><span data-stu-id="3dd3e-131">Encoder</span></span>          | <span data-ttu-id="3dd3e-132">CLSID \_ WICTiffEncoder</span><span class="sxs-lookup"><span data-stu-id="3dd3e-132">CLSID\_WICTiffEncoder</span></span>     | <span data-ttu-id="3dd3e-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span><span class="sxs-lookup"><span data-stu-id="3dd3e-133">0131be10-2001-4c5f-a9b0cc88fab64ce8</span></span>  |



 

## <a name="encoding"></a><span data-ttu-id="3dd3e-134">Encodage</span><span class="sxs-lookup"><span data-stu-id="3dd3e-134">Encoding</span></span>

<span data-ttu-id="3dd3e-135">L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-135">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3dd3e-136">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3dd3e-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="3dd3e-137">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="3dd3e-137">Encoder Options</span></span>

<span data-ttu-id="3dd3e-138">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-138">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="3dd3e-139">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-139">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="3dd3e-140">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-140">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="3dd3e-141">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3dd3e-141">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="3dd3e-142">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3dd3e-142">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="3dd3e-143">Le codec TIFF utilise les options de base du WIC.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-143">The TIFF codec uses basic WIC options.</span></span> <span data-ttu-id="3dd3e-144">Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec TIFF natif.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-144">The following table lists the WIC encoder options supported by the native TIFF codec.</span></span>

| <span data-ttu-id="3dd3e-145">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="3dd3e-145">Property Name</span></span>         | <span data-ttu-id="3dd3e-146">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3dd3e-146">VARTYPE</span></span> | <span data-ttu-id="3dd3e-147">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="3dd3e-147">Value Range</span></span> | <span data-ttu-id="3dd3e-148">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="3dd3e-148">Default Value</span></span>    |
|-----------------------|---------|-------------|------------------|
| <span data-ttu-id="3dd3e-149">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="3dd3e-149">CompressionQuality</span></span>    | <span data-ttu-id="3dd3e-150">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="3dd3e-150">VT\_R4</span></span>  | <span data-ttu-id="3dd3e-151">0-1,0</span><span class="sxs-lookup"><span data-stu-id="3dd3e-151">0 - 1.0</span></span>     | <span data-ttu-id="3dd3e-152">0</span><span class="sxs-lookup"><span data-stu-id="3dd3e-152">0</span></span>                |
| <span data-ttu-id="3dd3e-153">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="3dd3e-153">TiffCompressionMethod</span></span> | <span data-ttu-id="3dd3e-154">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="3dd3e-154">VT\_UI1</span></span> | [<span data-ttu-id="3dd3e-155">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="3dd3e-155">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [<span data-ttu-id="3dd3e-156">**WICTiffCompressionDontCare**</span><span class="sxs-lookup"><span data-stu-id="3dd3e-156">**WICTiffCompressionDontCare**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

<span data-ttu-id="3dd3e-157">Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-157">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="compressionquality-option"></a><span data-ttu-id="3dd3e-158">Option CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="3dd3e-158">CompressionQuality Option</span></span>

<span data-ttu-id="3dd3e-159">Spécifie la qualité de compression souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-159">Specifies the desired compression quality.</span></span> <span data-ttu-id="3dd3e-160">0,0 indique le schéma de compression le moins efficace disponible.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-160">0.0 indicates the least efficient compression scheme available.</span></span> <span data-ttu-id="3dd3e-161">En règle générale, ce schéma entraîne un encodage plus rapide mais une sortie plus grande.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-161">Typically, this scheme results in a faster encode but larger output.</span></span> <span data-ttu-id="3dd3e-162">La valeur 1,0 spécifie le schéma de compression le plus efficace disponible.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-162">A value of 1.0 specifies the most efficient compression scheme available.</span></span> <span data-ttu-id="3dd3e-163">En règle générale, ce schéma entraîne un encodage plus long, mais produit une sortie plus petite.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-163">Typically, this scheme results in a longer encode but produces smaller output.</span></span>

<span data-ttu-id="3dd3e-164">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-164">The default value is 0.</span></span>

### <a name="tiffcompressionmethod-option"></a><span data-ttu-id="3dd3e-165">Option TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="3dd3e-165">TiffCompressionMethod Option</span></span>

<span data-ttu-id="3dd3e-166">Spécifie la méthode de compression TIFF.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-166">Specifies the TIFF compression method.</span></span>

<span data-ttu-id="3dd3e-167">La valeur par défaut est [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span><span class="sxs-lookup"><span data-stu-id="3dd3e-167">The default value is [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).</span></span>

## <a name="decoding"></a><span data-ttu-id="3dd3e-168">Décodage</span><span class="sxs-lookup"><span data-stu-id="3dd3e-168">Decoding</span></span>

<span data-ttu-id="3dd3e-169">Les API de décodage WIC sont conçues pour être indépendantes du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="3dd3e-169">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="3dd3e-170">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="3dd3e-170">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="3dd3e-171">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="3dd3e-171">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
