---
description: Cette rubrique fournit des informations sur le codec GIF natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Vue d’ensemble du format GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203802"
---
# <a name="gif-format-overview"></a><span data-ttu-id="bf1e4-103">Vue d’ensemble du format GIF</span><span class="sxs-lookup"><span data-stu-id="bf1e4-103">GIF Format Overview</span></span>

<span data-ttu-id="bf1e4-104">Cette rubrique fournit des informations sur le codec GIF natif disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="bf1e4-104">This topic provides information about the native GIF codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="bf1e4-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="bf1e4-105">Codec Identity</span></span>

<span data-ttu-id="bf1e4-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-106">The following table provides codec identification information.</span></span>



|                        |                                       |
|------------------------|---------------------------------------|
| <span data-ttu-id="bf1e4-107">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="bf1e4-107">Formal Name(s)</span></span>         | <span data-ttu-id="bf1e4-108">GIF (Graphics Interchange format 89a)</span><span class="sxs-lookup"><span data-stu-id="bf1e4-108">Graphics Interchange Format 89a (GIF)</span></span> |
| <span data-ttu-id="bf1e4-109">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="bf1e4-109">File Name Extension(s)</span></span> | <span data-ttu-id="bf1e4-110">GIF</span><span class="sxs-lookup"><span data-stu-id="bf1e4-110">gif</span></span>                                   |
| <span data-ttu-id="bf1e4-111">type MIME</span><span class="sxs-lookup"><span data-stu-id="bf1e4-111">MIME type</span></span>              | <span data-ttu-id="bf1e4-112">image/gif</span><span class="sxs-lookup"><span data-stu-id="bf1e4-112">image/gif</span></span>                             |
| <span data-ttu-id="bf1e4-113">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="bf1e4-113">Specification Support</span></span>  | <span data-ttu-id="bf1e4-114">Spécification GIF 89a/89m</span><span class="sxs-lookup"><span data-stu-id="bf1e4-114">GIF Specification 89a/89m</span></span>             |



 

<span data-ttu-id="bf1e4-115">Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec GIF natifs.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-115">The following table lists the GUIDs used to identify the native GIF codec components.</span></span>



| <span data-ttu-id="bf1e4-116">Composant</span><span class="sxs-lookup"><span data-stu-id="bf1e4-116">Component</span></span>        | <span data-ttu-id="bf1e4-117">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="bf1e4-117">Friendly Name</span></span>            | <span data-ttu-id="bf1e4-118">GUID</span><span class="sxs-lookup"><span data-stu-id="bf1e4-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="bf1e4-119">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="bf1e4-119">Container Format</span></span> | <span data-ttu-id="bf1e4-120">GUID \_ ContainerFormatGif</span><span class="sxs-lookup"><span data-stu-id="bf1e4-120">GUID\_ContainerFormatGif</span></span> | <span data-ttu-id="bf1e4-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span><span class="sxs-lookup"><span data-stu-id="bf1e4-121">1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5</span></span> |
| <span data-ttu-id="bf1e4-122">Décodeur</span><span class="sxs-lookup"><span data-stu-id="bf1e4-122">Decoder</span></span>          | <span data-ttu-id="bf1e4-123">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="bf1e4-123">CLSID\_WICGifDecoder</span></span>     | <span data-ttu-id="bf1e4-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span><span class="sxs-lookup"><span data-stu-id="bf1e4-124">381dda3c-9ce9-4834-a23e1f98f8fc52be</span></span> |
| <span data-ttu-id="bf1e4-125">Encodeur</span><span class="sxs-lookup"><span data-stu-id="bf1e4-125">Encoder</span></span>          | <span data-ttu-id="bf1e4-126">CLSID \_ WICGifEncoder</span><span class="sxs-lookup"><span data-stu-id="bf1e4-126">CLSID\_WICGifEncoder</span></span>     | <span data-ttu-id="bf1e4-127">114f5598-0b22-40a0-86a1c83ea495adbd</span><span class="sxs-lookup"><span data-stu-id="bf1e4-127">114f5598-0b22-40a0-86a1c83ea495adbd</span></span> |



 

## <a name="encoding"></a><span data-ttu-id="bf1e4-128">Encodage</span><span class="sxs-lookup"><span data-stu-id="bf1e4-128">Encoding</span></span>

<span data-ttu-id="bf1e4-129">L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-129">The WIC encoding API are designed to be codec-independent and image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="bf1e4-130">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="bf1e4-130">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

### <a name="encoder-options"></a><span data-ttu-id="bf1e4-131">Options de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="bf1e4-131">Encoder Options</span></span>

<span data-ttu-id="bf1e4-132">Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-132">WIC-enabled codecs differ at the encoding option level.</span></span> <span data-ttu-id="bf1e4-133">Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-133">Encoder options reflect the capabilities of an image encoder and each native codec supports a set of these encoder options.</span></span> <span data-ttu-id="bf1e4-134">Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-134">Encoder options can be basic WIC supported options available to all WIC enabled codes (though not necessarily supported) or codec-specific options designed by the image format codec.</span></span> <span data-ttu-id="bf1e4-135">Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bf1e4-135">To manage these encoding options during the encoding process, WIC uses the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface .</span></span> <span data-ttu-id="bf1e4-136">Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="bf1e4-136">For more information about using the **IPropertyBag2** interface for WIC encoding , see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="bf1e4-137">L’encodeur GIF ne prend pas en charge les options WIC de base et ne fournit pas d’options d’encodeur personnalisées.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-137">The GIF encoder does not support any basic WIC options and does not provide custom encoder options.</span></span> <span data-ttu-id="bf1e4-138">Si une option d’encodeur figure dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-138">If an encoder option is in the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) option list, it is ignored.</span></span>

## <a name="decoding"></a><span data-ttu-id="bf1e4-139">Décodage</span><span class="sxs-lookup"><span data-stu-id="bf1e4-139">Decoding</span></span>

<span data-ttu-id="bf1e4-140">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="bf1e4-140">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="bf1e4-141">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="bf1e4-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="bf1e4-142">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="bf1e4-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 
