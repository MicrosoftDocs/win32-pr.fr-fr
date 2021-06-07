---
description: Fournit des informations sur le codec DDS natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Vue d’ensemble du format DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444950"
---
# <a name="dds-format-overview"></a><span data-ttu-id="075e5-103">Vue d’ensemble du format DDS</span><span class="sxs-lookup"><span data-stu-id="075e5-103">DDS Format Overview</span></span>

<span data-ttu-id="075e5-104">Cette rubrique fournit des informations sur le codec DDS natif disponible via le composant WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="075e5-104">This topic provides information about the native DDS codec available through the Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="075e5-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="075e5-105">Codec Identity</span></span>

<span data-ttu-id="075e5-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="075e5-106">The following table provides codec identification information.</span></span>



| <span data-ttu-id="075e5-107">Composant</span><span class="sxs-lookup"><span data-stu-id="075e5-107">Component</span></span>              | <span data-ttu-id="075e5-108">Description</span><span class="sxs-lookup"><span data-stu-id="075e5-108">Description</span></span>        |
|------------------------|--------------------|
| <span data-ttu-id="075e5-109">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="075e5-109">Formal Name(s)</span></span>         | <span data-ttu-id="075e5-110">Surface DirectDraw</span><span class="sxs-lookup"><span data-stu-id="075e5-110">DirectDraw Surface</span></span> |
| <span data-ttu-id="075e5-111">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="075e5-111">File Name Extension(s)</span></span> | <span data-ttu-id="075e5-112">DDS</span><span class="sxs-lookup"><span data-stu-id="075e5-112">dds</span></span>                |
| <span data-ttu-id="075e5-113">type MIME</span><span class="sxs-lookup"><span data-stu-id="075e5-113">MIME type</span></span>              | <span data-ttu-id="075e5-114">image/VND-ms. DDS</span><span class="sxs-lookup"><span data-stu-id="075e5-114">image/vnd-ms.dds</span></span>   |



 

<span data-ttu-id="075e5-115">Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec DDS natifs.</span><span class="sxs-lookup"><span data-stu-id="075e5-115">The following table lists the GUIDs used to identify the native DDS codec components.</span></span>



| <span data-ttu-id="075e5-116">Composant</span><span class="sxs-lookup"><span data-stu-id="075e5-116">Component</span></span>        | <span data-ttu-id="075e5-117">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="075e5-117">Friendly Name</span></span>            | <span data-ttu-id="075e5-118">GUID</span><span class="sxs-lookup"><span data-stu-id="075e5-118">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="075e5-119">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="075e5-119">Container Format</span></span> | <span data-ttu-id="075e5-120">GUID \_ ContainerFormatDds</span><span class="sxs-lookup"><span data-stu-id="075e5-120">GUID\_ContainerFormatDds</span></span> | <span data-ttu-id="075e5-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span><span class="sxs-lookup"><span data-stu-id="075e5-121">9967cb95-2e85-4ac8-8ca283d7ccd425c9</span></span> |
| <span data-ttu-id="075e5-122">Décodeur</span><span class="sxs-lookup"><span data-stu-id="075e5-122">Decoder</span></span>          | <span data-ttu-id="075e5-123">CLSID \_ WICDdsDecoder</span><span class="sxs-lookup"><span data-stu-id="075e5-123">CLSID\_WICDdsDecoder</span></span>     | <span data-ttu-id="075e5-124">9053699f-a341-429d-9e90ee437cf80c73</span><span class="sxs-lookup"><span data-stu-id="075e5-124">9053699f-a341-429d-9e90ee437cf80c73</span></span> |
| <span data-ttu-id="075e5-125">Encodeur</span><span class="sxs-lookup"><span data-stu-id="075e5-125">Encoder</span></span>          | <span data-ttu-id="075e5-126">CLSID \_ WICDdsEncoder</span><span class="sxs-lookup"><span data-stu-id="075e5-126">CLSID\_WICDdsEncoder</span></span>     | <span data-ttu-id="075e5-127">a61dde94-66ce-4ac1-881b71680588895e</span><span class="sxs-lookup"><span data-stu-id="075e5-127">a61dde94-66ce-4ac1-881b71680588895e</span></span> |



 

## <a name="pixel-format-support"></a><span data-ttu-id="075e5-128">Prise en charge du format pixel</span><span class="sxs-lookup"><span data-stu-id="075e5-128">Pixel Format Support</span></span>

<span data-ttu-id="075e5-129">Notez que le format DDS prend en charge toute valeur de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valide.</span><span class="sxs-lookup"><span data-stu-id="075e5-129">Note that the DDS format supports any valid [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value.</span></span> <span data-ttu-id="075e5-130">Toutefois, le codec WIC DDS prend uniquement en charge le décodage et l’encodage des fichiers contenant les formats suivants :</span><span class="sxs-lookup"><span data-stu-id="075e5-130">However, the WIC DDS codec only supports decoding and encoding files containing the following formats:</span></span>

-   <span data-ttu-id="075e5-131">DXGI \_ format \_ BC1 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="075e5-131">DXGI\_FORMAT\_BC1\_UNORM</span></span>
-   <span data-ttu-id="075e5-132">DXGI \_ format \_ BC2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="075e5-132">DXGI\_FORMAT\_BC2\_UNORM</span></span>
-   <span data-ttu-id="075e5-133">DXGI \_ format \_ BC3 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="075e5-133">DXGI\_FORMAT\_BC3\_UNORM</span></span>

## <a name="encoding"></a><span data-ttu-id="075e5-134">Encodage</span><span class="sxs-lookup"><span data-stu-id="075e5-134">Encoding</span></span>

<span data-ttu-id="075e5-135">Les API de codage WIC sont conçues pour être indépendantes du codec et, par conséquent, l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="075e5-135">The WIC encoding APIs are designed to be codec-independent and therefore image encoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="075e5-136">Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="075e5-136">For more information about image encoding using the WIC API, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="075e5-137">Le format de fichier DDS a des exigences uniques qui résultent de sa prise en charge des concepts tels que les des mipmaps et les tableaux de texture.</span><span class="sxs-lookup"><span data-stu-id="075e5-137">The DDS file format has unique requirements that arise from its support for concepts such as mipmaps and texture arrays.</span></span> <span data-ttu-id="075e5-138">Pour exercer un contrôle complet sur l’encodage d’image DDS, vous devez utiliser l’interface [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) pour définir des paramètres d’encodage spécifiques à DDS.</span><span class="sxs-lookup"><span data-stu-id="075e5-138">To fully exercise control over DDS image encoding, you should use the [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) interface to set DDS-specific encoding parameters.</span></span>

## <a name="decoding"></a><span data-ttu-id="075e5-139">Décodage</span><span class="sxs-lookup"><span data-stu-id="075e5-139">Decoding</span></span>

<span data-ttu-id="075e5-140">Les API de décodage WIC sont conçues pour être indépendantes du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="075e5-140">The WIC decoding APIs are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="075e5-141">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="075e5-141">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="075e5-142">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="075e5-142">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="block-compressed-data-access"></a><span data-ttu-id="075e5-143">Bloquer l’accès aux données compressées</span><span class="sxs-lookup"><span data-stu-id="075e5-143">Block compressed data access</span></span>

<span data-ttu-id="075e5-144">En plus de prendre en charge les interfaces de codec WIC standard, le décodeur DDS fournit un accès direct aux données compressées en bloc natives à l’aide des interfaces spécifiques à DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) et [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span><span class="sxs-lookup"><span data-stu-id="075e5-144">In addition to supporting the standard WIC codec interfaces, the DDS decoder provides direct access to the native block compressed data using the DDS-specific interfaces, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) and [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode).</span></span> <span data-ttu-id="075e5-145">Pour utiliser ces interfaces, appelez QueryInterface sur [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectivement.</span><span class="sxs-lookup"><span data-stu-id="075e5-145">To use these interfaces, call QueryInterface off of [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectively.</span></span>

 

 
