---
description: Cette rubrique fournit des informations sur le codec BMP natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Vue d’ensemble du format BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756910"
---
# <a name="bmp-format-overview"></a><span data-ttu-id="09fa9-103">Vue d’ensemble du format BMP</span><span class="sxs-lookup"><span data-stu-id="09fa9-103">BMP Format Overview</span></span>

<span data-ttu-id="09fa9-104">Cette rubrique fournit des informations sur le codec BMP natif disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="09fa9-104">This topic provides information about the native BMP codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="09fa9-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="09fa9-105">Codec Identity</span></span>

<span data-ttu-id="09fa9-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="09fa9-106">The following table provides codec identification information.</span></span>



|                        |                       |
|------------------------|-----------------------|
| <span data-ttu-id="09fa9-107">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="09fa9-107">Formal Name(s)</span></span>         | <span data-ttu-id="09fa9-108">Format bitmap Windows</span><span class="sxs-lookup"><span data-stu-id="09fa9-108">Windows Bitmap Format</span></span> |
| <span data-ttu-id="09fa9-109">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="09fa9-109">File Name Extension(s)</span></span> | <span data-ttu-id="09fa9-110">BMP, DIB</span><span class="sxs-lookup"><span data-stu-id="09fa9-110">bmp, dib</span></span>              |
| <span data-ttu-id="09fa9-111">type MIME</span><span class="sxs-lookup"><span data-stu-id="09fa9-111">MIME type</span></span>              | <span data-ttu-id="09fa9-112">image/bmp</span><span class="sxs-lookup"><span data-stu-id="09fa9-112">image/bmp</span></span>             |
| <span data-ttu-id="09fa9-113">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="09fa9-113">Specification Support</span></span>  | <span data-ttu-id="09fa9-114">BMP spécification v5</span><span class="sxs-lookup"><span data-stu-id="09fa9-114">BMP Specification v5</span></span>  |



 

<span data-ttu-id="09fa9-115">Le tableau suivant répertorie les GUID utilisés pour identifier les composants du codec BMP natifs.</span><span class="sxs-lookup"><span data-stu-id="09fa9-115">The following table lists the GUIDs used to identify the native BMP codec components.</span></span>



| <span data-ttu-id="09fa9-116">Composant</span><span class="sxs-lookup"><span data-stu-id="09fa9-116">Component</span></span>        | <span data-ttu-id="09fa9-117">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="09fa9-117">Friendly Name</span></span>            | <span data-ttu-id="09fa9-118">GUID</span><span class="sxs-lookup"><span data-stu-id="09fa9-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="09fa9-119">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="09fa9-119">Container Format</span></span> | <span data-ttu-id="09fa9-120">GUID \_ ContainerFormatBmp</span><span class="sxs-lookup"><span data-stu-id="09fa9-120">GUID\_ContainerFormatBmp</span></span> | <span data-ttu-id="09fa9-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span><span class="sxs-lookup"><span data-stu-id="09fa9-121">0af1d87e-fcfe-4188-bdeba7906471cbe3</span></span> |
| <span data-ttu-id="09fa9-122">Décodeur</span><span class="sxs-lookup"><span data-stu-id="09fa9-122">Decoder</span></span>          | <span data-ttu-id="09fa9-123">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="09fa9-123">CLSID\_WICBmpDecoder</span></span>     | <span data-ttu-id="09fa9-124">6b462062-7cbf-400d-9fdb813dd10f2778</span><span class="sxs-lookup"><span data-stu-id="09fa9-124">6b462062-7cbf-400d-9fdb813dd10f2778</span></span> |
| <span data-ttu-id="09fa9-125">Encodeur</span><span class="sxs-lookup"><span data-stu-id="09fa9-125">Encoder</span></span>          | <span data-ttu-id="09fa9-126">CLSID \_ WICBmpEncoder</span><span class="sxs-lookup"><span data-stu-id="09fa9-126">CLSID\_WICBmpEncoder</span></span>     | <span data-ttu-id="09fa9-127">69be8bb4-d66d-47c8-865aed1589433782</span><span class="sxs-lookup"><span data-stu-id="09fa9-127">69be8bb4-d66d-47c8-865aed1589433782</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="09fa9-128">Encodage</span><span class="sxs-lookup"><span data-stu-id="09fa9-128">Encoding</span></span>

<span data-ttu-id="09fa9-129">L’API d’encodage WIC est conçue pour être indépendante du codec et, par conséquent, l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="09fa9-129">The WIC encoding API are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="09fa9-130">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="09fa9-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="09fa9-131">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="09fa9-131">Encoder Options</span></span>

<span data-ttu-id="09fa9-132">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="09fa9-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="09fa9-133">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="09fa9-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="09fa9-134">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="09fa9-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="09fa9-135">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="09fa9-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="09fa9-136">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="09fa9-136">For more information about using the **IPropertyBag2** interface for WIC encoding see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="09fa9-137">Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec BMP natif.</span><span class="sxs-lookup"><span data-stu-id="09fa9-137">The following table lists the WIC encoder options supported by the native BMP codec.</span></span>



| <span data-ttu-id="09fa9-138">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="09fa9-138">Property Name</span></span>               | <span data-ttu-id="09fa9-139">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="09fa9-139">VARTYPE</span></span>      | <span data-ttu-id="09fa9-140">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="09fa9-140">Value Range</span></span>                      | <span data-ttu-id="09fa9-141">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="09fa9-141">Default Value</span></span>      |
|-----------------------------|--------------|----------------------------------|--------------------|
| <span data-ttu-id="09fa9-142">**EnableV5Header32bppBGRA**</span><span class="sxs-lookup"><span data-stu-id="09fa9-142">**EnableV5Header32bppBGRA**</span></span> | <span data-ttu-id="09fa9-143">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="09fa9-143">**VT\_BOOL**</span></span> | <span data-ttu-id="09fa9-144">**VARIANTE \_ vrai/variante \_ faux**</span><span class="sxs-lookup"><span data-stu-id="09fa9-144">**VARIANT\_TRUE/VARIANT\_FALSE**</span></span> | <span data-ttu-id="09fa9-145">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="09fa9-145">**VARIANT\_FALSE**</span></span> |



 

### <a name="enablev5header32bppbgra"></a><span data-ttu-id="09fa9-146">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="09fa9-146">EnableV5Header32bppBGRA</span></span>

<span data-ttu-id="09fa9-147">Spécifie s’il faut autoriser l’encodage des données au \_ format de pixel GUID WICPixelFormat32bppBGRA.</span><span class="sxs-lookup"><span data-stu-id="09fa9-147">Specifies whether to allow encoding data in the GUID\_WICPixelFormat32bppBGRA pixel format.</span></span> <span data-ttu-id="09fa9-148">Si cette option a la valeur **Variant \_ true**, le BMP est écrit avec un en-tête BITMAPV5HEADER.</span><span class="sxs-lookup"><span data-stu-id="09fa9-148">If this option is set to **VARIANT\_TRUE**, the BMP will be written out with a BITMAPV5HEADER header.</span></span>

<span data-ttu-id="09fa9-149">La valeur par défaut **est \_ false**.</span><span class="sxs-lookup"><span data-stu-id="09fa9-149">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="09fa9-150">Si une option d’encodeur est présente dans la liste d’options IPropertyBag2 que le codec ne prend pas en charge, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="09fa9-150">If an encoder option is present in the IPropertyBag2 option list that the codec does not support, it is ignored.</span></span>

<span data-ttu-id="09fa9-151">Remarque pour les fichiers Windows BMP 16 bits et 32 bits, le codec BMP ignore tout canal alpha, car de nombreux fichiers image hérités contiennent des données non valides dans ce canal supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="09fa9-151">Note for 16-bit and 32-bit Windows BMP files, the BMP codec ignores any alpha channel, as many legacy image files contain invalid data in this extra channel.</span></span> <span data-ttu-id="09fa9-152">À compter de Windows 8, les fichiers Windows BMP 32 bits écrits à l’aide de **BITMAPV5HEADER** avec un contenu de canal alpha valide sont lus en tant que WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="09fa9-152">Starting with Windows 8, 32-bit Windows BMP files written using the **BITMAPV5HEADER** with valid alpha channel content are read as WICPixelFormat32bppBGRA</span></span>

## <a name="decoding"></a><span data-ttu-id="09fa9-153">Décodage</span><span class="sxs-lookup"><span data-stu-id="09fa9-153">Decoding</span></span>

<span data-ttu-id="09fa9-154">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="09fa9-154">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="09fa9-155">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="09fa9-155">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="09fa9-156">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="09fa9-156">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
