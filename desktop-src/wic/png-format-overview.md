---
description: Cette rubrique fournit des informations sur le codec PNG natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Vue d’ensemble du format PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533673"
---
# <a name="png-format-overview"></a><span data-ttu-id="9beec-103">Vue d’ensemble du format PNG</span><span class="sxs-lookup"><span data-stu-id="9beec-103">PNG Format Overview</span></span>

<span data-ttu-id="9beec-104">Cette rubrique fournit des informations sur le codec PNG natif disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="9beec-104">This topic provides information about the native PNG codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="9beec-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="9beec-105">Codec Identity</span></span>

<span data-ttu-id="9beec-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="9beec-106">The following table provides codec identification information.</span></span>



|                        |                                 |
|------------------------|---------------------------------|
| <span data-ttu-id="9beec-107">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="9beec-107">Formal Name(s)</span></span>         | <span data-ttu-id="9beec-108">format PNG (Portable Network Graphics)</span><span class="sxs-lookup"><span data-stu-id="9beec-108">Portable Network Graphics (PNG)</span></span> |
| <span data-ttu-id="9beec-109">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="9beec-109">File Name Extension(s)</span></span> | <span data-ttu-id="9beec-110">png</span><span class="sxs-lookup"><span data-stu-id="9beec-110">png</span></span>                             |
| <span data-ttu-id="9beec-111">type MIME</span><span class="sxs-lookup"><span data-stu-id="9beec-111">MIME type</span></span>              | <span data-ttu-id="9beec-112">image/png</span><span class="sxs-lookup"><span data-stu-id="9beec-112">image/png</span></span>                       |
| <span data-ttu-id="9beec-113">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="9beec-113">Specification Support</span></span>  | <span data-ttu-id="9beec-114">Spécification PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="9beec-114">PNG Specification 1.2</span></span>           |



 

<span data-ttu-id="9beec-115">Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec PNG natifs.</span><span class="sxs-lookup"><span data-stu-id="9beec-115">The following table lists the GUIDs used to identify the native PNG codec components.</span></span>



| <span data-ttu-id="9beec-116">Composant</span><span class="sxs-lookup"><span data-stu-id="9beec-116">Component</span></span>        | <span data-ttu-id="9beec-117">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="9beec-117">Friendly Name</span></span>            | <span data-ttu-id="9beec-118">GUID</span><span class="sxs-lookup"><span data-stu-id="9beec-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="9beec-119">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="9beec-119">Container Format</span></span> | <span data-ttu-id="9beec-120">GUID \_ ContainerFormatPng</span><span class="sxs-lookup"><span data-stu-id="9beec-120">GUID\_ContainerFormatPng</span></span> | <span data-ttu-id="9beec-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span><span class="sxs-lookup"><span data-stu-id="9beec-121">1b7cfaf4-713f-473c-bbcd6137425faeaf</span></span> |
| <span data-ttu-id="9beec-122">Décodeur</span><span class="sxs-lookup"><span data-stu-id="9beec-122">Decoder</span></span>          | <span data-ttu-id="9beec-123">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="9beec-123">CLSID\_WICPngDecoder</span></span>     | <span data-ttu-id="9beec-124">389ea17b-5078-4cde-b6ef25c15175c751</span><span class="sxs-lookup"><span data-stu-id="9beec-124">389ea17b-5078-4cde-b6ef25c15175c751</span></span> |
| <span data-ttu-id="9beec-125">Encodeur</span><span class="sxs-lookup"><span data-stu-id="9beec-125">Encoder</span></span>          | <span data-ttu-id="9beec-126">CLSID \_ WICPngEncoder</span><span class="sxs-lookup"><span data-stu-id="9beec-126">CLSID\_WICPngEncoder</span></span>     | <span data-ttu-id="9beec-127">27949969-876a-41d7-9447568f6a35a4dc</span><span class="sxs-lookup"><span data-stu-id="9beec-127">27949969-876a-41d7-9447568f6a35a4dc</span></span> |



 

### <a name="windows-8-and-later"></a><span data-ttu-id="9beec-128">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="9beec-128">Windows 8 and later</span></span>

<span data-ttu-id="9beec-129">À compter de Windows 8 WIC, vous disposez d’un décodeur PNG supplémentaire</span><span class="sxs-lookup"><span data-stu-id="9beec-129">Starting with Windows 8 WIC provides an additional PNG decoder</span></span>

## <a name="encoding"></a><span data-ttu-id="9beec-130">Encodage</span><span class="sxs-lookup"><span data-stu-id="9beec-130">Encoding</span></span>

<span data-ttu-id="9beec-131">L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="9beec-131">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9beec-132">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9beec-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="9beec-133">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="9beec-133">Encoder Options</span></span>

<span data-ttu-id="9beec-134">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="9beec-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="9beec-135">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="9beec-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="9beec-136">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="9beec-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="9beec-137">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9beec-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="9beec-138">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="9beec-138">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="9beec-139">Le codec PNG utilise les options de l’encodeur WIC de base.</span><span class="sxs-lookup"><span data-stu-id="9beec-139">The PNG codec uses basic WIC encoder options.</span></span> <span data-ttu-id="9beec-140">Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec PNG natif.</span><span class="sxs-lookup"><span data-stu-id="9beec-140">The following table lists the WIC encoder options supported by the native PNG codec.</span></span>



| <span data-ttu-id="9beec-141">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="9beec-141">Property Name</span></span>   | <span data-ttu-id="9beec-142">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9beec-142">VARTYPE</span></span>  | <span data-ttu-id="9beec-143">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="9beec-143">Value Range</span></span>                                                 | <span data-ttu-id="9beec-144">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="9beec-144">Default Value</span></span>                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9beec-145">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="9beec-145">InterlaceOption</span></span> | <span data-ttu-id="9beec-146">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="9beec-146">VT\_BOOL</span></span> | <span data-ttu-id="9beec-147">**True** / **Valeur false**</span><span class="sxs-lookup"><span data-stu-id="9beec-147">**TRUE**/**FALSE**</span></span>                                          | <span data-ttu-id="9beec-148">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9beec-148">**FALSE**</span></span>                                                        |
| <span data-ttu-id="9beec-149">FilterOption</span><span class="sxs-lookup"><span data-stu-id="9beec-149">FilterOption</span></span>    | <span data-ttu-id="9beec-150">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="9beec-150">VT\_UI1</span></span>  | [<span data-ttu-id="9beec-151">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="9beec-151">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [<span data-ttu-id="9beec-152">**WICPngFilterUnspecified**</span><span class="sxs-lookup"><span data-stu-id="9beec-152">**WICPngFilterUnspecified**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

<span data-ttu-id="9beec-153">Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="9beec-153">If an encoder option is present in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list that the codec does not support, it is ignored.</span></span>

### <a name="interlaceoption"></a><span data-ttu-id="9beec-154">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="9beec-154">InterlaceOption</span></span>

<span data-ttu-id="9beec-155">Spécifie s’il faut encoder les données d’image comme entrelacées.</span><span class="sxs-lookup"><span data-stu-id="9beec-155">Specifies whether to encode the image data as interlaced.</span></span>

<span data-ttu-id="9beec-156">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9beec-156">The default value is **FALSE**.</span></span>

### <a name="filteroption"></a><span data-ttu-id="9beec-157">FilterOption</span><span class="sxs-lookup"><span data-stu-id="9beec-157">FilterOption</span></span>

<span data-ttu-id="9beec-158">Spécifie l’option de filtre à utiliser pour la compression d’image.</span><span class="sxs-lookup"><span data-stu-id="9beec-158">Specifies the filter option to use for image compression.</span></span>

<span data-ttu-id="9beec-159">La valeur par défaut est [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span><span class="sxs-lookup"><span data-stu-id="9beec-159">The default value is [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).</span></span>

## <a name="decoding"></a><span data-ttu-id="9beec-160">Décodage</span><span class="sxs-lookup"><span data-stu-id="9beec-160">Decoding</span></span>

<span data-ttu-id="9beec-161">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="9beec-161">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="9beec-162">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="9beec-162">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="9beec-163">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="9beec-163">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="9beec-164">Le codec PNG natif prend également en charge le [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sur le décodage de trame qui ajoute des options avancées pour le décodage d’un flux d’image.</span><span class="sxs-lookup"><span data-stu-id="9beec-164">The native PNG codec also supports the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) on frame decoding adding advanced options for decoding an image stream.</span></span> <span data-ttu-id="9beec-165">Pour plus d’informations sur ces options avancées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="9beec-165">For more information about these advanced options, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
