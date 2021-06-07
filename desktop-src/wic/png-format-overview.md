---
description: Cette rubrique fournit des informations sur le codec PNG natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Vue d’ensemble du format PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444440"
---
# <a name="png-format-overview"></a><span data-ttu-id="bab22-103">Vue d’ensemble du format PNG</span><span class="sxs-lookup"><span data-stu-id="bab22-103">PNG Format Overview</span></span>

<span data-ttu-id="bab22-104">Cette rubrique fournit des informations sur le codec PNG natif disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="bab22-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="bab22-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="bab22-105">Codec Identity</span></span>

<span data-ttu-id="bab22-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="bab22-106">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="bab22-107">Composant</span><span class="sxs-lookup"><span data-stu-id="bab22-107">Component</span></span>          | <span data-ttu-id="bab22-108">Description</span><span class="sxs-lookup"><span data-stu-id="bab22-108">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="bab22-109">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="bab22-109">Formal Name(s)</span></span>         | <span data-ttu-id="bab22-110">format PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="bab22-110">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="bab22-111">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="bab22-111">File Name Extension(s)</span></span> | <span data-ttu-id="bab22-112">png</span><span class="sxs-lookup"><span data-stu-id="bab22-112">png</span></span>                             |
| <span data-ttu-id="bab22-113">type MIME</span><span class="sxs-lookup"><span data-stu-id="bab22-113">MIME type</span></span>              | <span data-ttu-id="bab22-114">image/png</span><span class="sxs-lookup"><span data-stu-id="bab22-114">image/png</span></span>                       |
| <span data-ttu-id="bab22-115">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="bab22-115">Specification Support</span></span>  | <span data-ttu-id="bab22-116">Spécification PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="bab22-116">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="bab22-117">Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec PNG natifs.</span><span class="sxs-lookup"><span data-stu-id="bab22-117">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="bab22-118">Composant</span><span class="sxs-lookup"><span data-stu-id="bab22-118">Component</span></span>        | <span data-ttu-id="bab22-119">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="bab22-119">Friendly Name</span></span>            | <span data-ttu-id="bab22-120">GUID</span><span class="sxs-lookup"><span data-stu-id="bab22-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="bab22-121">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="bab22-121">Container Format</span></span> | <span data-ttu-id="bab22-122">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="bab22-122">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="bab22-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="bab22-123">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="bab22-124">Décodeur</span><span class="sxs-lookup"><span data-stu-id="bab22-124">Decoder</span></span>          | <span data-ttu-id="bab22-125">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="bab22-125">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="bab22-126">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="bab22-126">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="bab22-127">Encodeur</span><span class="sxs-lookup"><span data-stu-id="bab22-127">Encoder</span></span>          | <span data-ttu-id="bab22-128">CLSID \_ WICPngEncoder</span><span class="sxs-lookup"><span data-stu-id="bab22-128">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="bab22-129">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="bab22-129">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="bab22-130">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="bab22-130">Windows 8 and later</span></span>

<span data-ttu-id="bab22-131">À compter de Windows 8 WIC, vous disposez d’un décodeur PNG supplémentaire</span><span class="sxs-lookup"><span data-stu-id="bab22-131">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="bab22-132">Encodage</span><span class="sxs-lookup"><span data-stu-id="bab22-132">Encoding</span></span>

<span data-ttu-id="bab22-133">L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="bab22-133">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="bab22-134">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="bab22-134">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="bab22-135">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="bab22-135">Encoder Options</span></span>

<span data-ttu-id="bab22-136">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="bab22-136">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="bab22-137">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="bab22-137">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="bab22-138">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="bab22-138">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="bab22-139">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bab22-139">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="bab22-140">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="bab22-140">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="bab22-141">Le codec PNG utilise les options de l’encodeur WIC de base.</span><span class="sxs-lookup"><span data-stu-id="bab22-141">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="bab22-142">Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec PNG natif.</span><span class="sxs-lookup"><span data-stu-id="bab22-142">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="bab22-143">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="bab22-143">Property Name</span></span>   | <span data-ttu-id="bab22-144">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bab22-144">VARTYPE</span></span>  | <span data-ttu-id="bab22-145">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="bab22-145">Value Range</span></span>                                                 | <span data-ttu-id="bab22-146">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="bab22-146">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bab22-147">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="bab22-147">InterlaceOption</span></span> | <span data-ttu-id="bab22-148">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="bab22-148">VT\_BOOL</span></span> | <span data-ttu-id="bab22-149">**True** / **Valeur false**</span><span class="sxs-lookup"><span data-stu-id="bab22-149">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="bab22-150">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="bab22-150">**FALSE**</span></span>                                                        |
| <span data-ttu-id="bab22-151">FilterOption</span><span class="sxs-lookup"><span data-stu-id="bab22-151">FilterOption</span></span>    | <span data-ttu-id="bab22-152">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="bab22-152">VT\_UI1</span></span>  | [<span data-ttu-id="bab22-153">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="bab22-153">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="bab22-154">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="bab22-154">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="bab22-155">Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="bab22-155">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="bab22-156">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="bab22-156">InterlaceOption</span></span>

<span data-ttu-id="bab22-157">Spécifie s’il faut encoder les données d’image comme entrelacées.</span><span class="sxs-lookup"><span data-stu-id="bab22-157">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="bab22-158">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bab22-158">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="bab22-159">FilterOption</span><span class="sxs-lookup"><span data-stu-id="bab22-159">FilterOption</span></span>

<span data-ttu-id="bab22-160">Spécifie l’option de filtre à utiliser pour la compression d’image.</span><span class="sxs-lookup"><span data-stu-id="bab22-160">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="bab22-161">La valeur par défaut est [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span><span class="sxs-lookup"><span data-stu-id="bab22-161">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="bab22-162">Décodage</span><span class="sxs-lookup"><span data-stu-id="bab22-162">Decoding</span></span>

<span data-ttu-id="bab22-163">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="bab22-163">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="bab22-164">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="bab22-164">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="bab22-165">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="bab22-165">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="bab22-166">Le codec PNG natif prend également en charge le [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sur le décodage de trame qui ajoute des options avancées pour le décodage d’un flux d’image.</span><span class="sxs-lookup"><span data-stu-id="bab22-166">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="bab22-167">Pour plus d’informations sur ces options avancées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="bab22-167">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
