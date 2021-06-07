---
description: Cette rubrique fournit des informations sur le codec BMP natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Vue d’ensemble du format BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444960"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="c3a6b-103">Vue d’ensemble du format BMP</span><span class="sxs-lookup"><span data-stu-id="c3a6b-103">BMP Format Overview</span></span>

<span data-ttu-id="c3a6b-104">Cette rubrique fournit des informations sur le codec BMP natif disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="c3a6b-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="c3a6b-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="c3a6b-105">Codec Identity</span></span>

<span data-ttu-id="c3a6b-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="c3a6b-107">Composant</span><span class="sxs-lookup"><span data-stu-id="c3a6b-107">Component</span></span>              | <span data-ttu-id="c3a6b-108">Description</span><span class="sxs-lookup"><span data-stu-id="c3a6b-108">Description</span></span>           |
|------------------------|-----------------------|
| <span data-ttu-id="c3a6b-109">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="c3a6b-109">Formal Name(s)</span></span>         | <span data-ttu-id="c3a6b-110">Format bitmap Windows</span><span class="sxs-lookup"><span data-stu-id="c3a6b-110">Windows Bitmap Format</span></span> |
| <span data-ttu-id="c3a6b-111">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="c3a6b-111">File Name Extension(s)</span></span> | <span data-ttu-id="c3a6b-112">BMP, DIB</span><span class="sxs-lookup"><span data-stu-id="c3a6b-112">bmp, dib</span></span>              |
| <span data-ttu-id="c3a6b-113">type MIME</span><span class="sxs-lookup"><span data-stu-id="c3a6b-113">MIME type</span></span>              | <span data-ttu-id="c3a6b-114">image/bmp</span><span class="sxs-lookup"><span data-stu-id="c3a6b-114">image/bmp</span></span>             |
| <span data-ttu-id="c3a6b-115">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="c3a6b-115">Specification Support</span></span>  | <span data-ttu-id="c3a6b-116">BMP spécification v5</span><span class="sxs-lookup"><span data-stu-id="c3a6b-116">BMP Specification v5</span></span>  |



 

<span data-ttu-id="c3a6b-117">Le tableau suivant répertorie les GUID utilisés pour identifier les composants du codec BMP natifs.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-117">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="c3a6b-118">Composant</span><span class="sxs-lookup"><span data-stu-id="c3a6b-118">Component</span></span>        | <span data-ttu-id="c3a6b-119">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="c3a6b-119">Friendly Name</span></span>            | <span data-ttu-id="c3a6b-120">GUID</span><span class="sxs-lookup"><span data-stu-id="c3a6b-120">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="c3a6b-121">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="c3a6b-121">Container Format</span></span> | <span data-ttu-id="c3a6b-122">GUID \_ ContainerFormatBmp</span><span class="sxs-lookup"><span data-stu-id="c3a6b-122">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="c3a6b-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="c3a6b-123">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="c3a6b-124">Décodeur</span><span class="sxs-lookup"><span data-stu-id="c3a6b-124">Decoder</span></span>          | <span data-ttu-id="c3a6b-125">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="c3a6b-125">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="c3a6b-126">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="c3a6b-126">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="c3a6b-127">Encodeur</span><span class="sxs-lookup"><span data-stu-id="c3a6b-127">Encoder</span></span>          | <span data-ttu-id="c3a6b-128">CLSID \_ WICBmpEncoder</span><span class="sxs-lookup"><span data-stu-id="c3a6b-128">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="c3a6b-129">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="c3a6b-129">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="c3a6b-130">Encodage</span><span class="sxs-lookup"><span data-stu-id="c3a6b-130">Encoding</span></span>

<span data-ttu-id="c3a6b-131">L’API d’encodage WIC est conçue pour être indépendante du codec et, par conséquent, l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-131">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c3a6b-132">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c3a6b-132">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="c3a6b-133">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="c3a6b-133">Encoder Options</span></span>

<span data-ttu-id="c3a6b-134">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-134">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="c3a6b-135">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-135">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="c3a6b-136">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-136">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="c3a6b-137">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c3a6b-137">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="c3a6b-138">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="c3a6b-138">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="c3a6b-139">Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec BMP natif.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-139">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="c3a6b-140">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="c3a6b-140">Property Name</span></span>               | <span data-ttu-id="c3a6b-141">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c3a6b-141">VARTYPE</span></span>      | <span data-ttu-id="c3a6b-142">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="c3a6b-142">Value Range</span></span>                      | <span data-ttu-id="c3a6b-143">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c3a6b-143">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="c3a6b-144">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="c3a6b-144">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="c3a6b-145">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c3a6b-145">**VT\_BOOL**</span></span> | <span data-ttu-id="c3a6b-146">**VARIANTE \_ vrai/variante \_ faux**</span><span class="sxs-lookup"><span data-stu-id="c3a6b-146">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="c3a6b-147">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="c3a6b-147">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="c3a6b-148">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="c3a6b-148">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="c3a6b-149">Spécifie s’il faut autoriser l’encodage des données au \_ format de pixel GUID WICPixelFormat32bppBGRA.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-149">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="c3a6b-150">Si cette option a la valeur **Variant \_ true**, le BMP est écrit avec un en-tête BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-150">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="c3a6b-151">La valeur par défaut **est \_ false**.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-151">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="c3a6b-152">Si une option d’encodeur est présente dans la liste d’options IPropertyBag2 que le codec ne prend pas en charge, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-152">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="c3a6b-153">Remarque pour les fichiers Windows BMP 16 bits et 32 bits, le codec BMP ignore tout canal alpha, car de nombreux fichiers image hérités contiennent des données non valides dans ce canal supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-153">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="c3a6b-154">À compter de Windows 8, les fichiers Windows BMP 32 bits écrits à l’aide de **BITMAPV5HEADER** avec un contenu de canal alpha valide sont lus en tant que WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="c3a6b-154">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="c3a6b-155">Décodage</span><span class="sxs-lookup"><span data-stu-id="c3a6b-155">Decoding</span></span>

<span data-ttu-id="c3a6b-156">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="c3a6b-156">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="c3a6b-157">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="c3a6b-157">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="c3a6b-158">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="c3a6b-158">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
