---
description: Cette section de rubriques fournit aux développeurs des conseils sur la façon d’implémenter des codecs de format de fichier image qui fonctionnent dans l’infrastructure WIC (Windows Imaging Component).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Comment écrire un codec WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865550"
---
# <a name="how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="1a3f1-103">Comment écrire un codec WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1a3f1-103">How to Write a WIC-Enabled Codec</span></span>

<span data-ttu-id="1a3f1-104">Cette section de rubriques fournit aux développeurs des conseils sur la façon d’implémenter des codecs de format de fichier image qui fonctionnent dans l’infrastructure WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="1a3f1-104">This section of topics provide developers with guidance on how to implement image file format codecs that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="1a3f1-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="1a3f1-105">Introduction</span></span>](-wic-howtowriteacodec-intro.md)  
[<span data-ttu-id="1a3f1-106">Fonctionnement du composant WIC (Windows Imaging Component)</span><span class="sxs-lookup"><span data-stu-id="1a3f1-106">How The Windows Imaging Component (WIC) Works</span></span>](-wic-howwicworks.md)  
<dl>

[<span data-ttu-id="1a3f1-107">Découverte et arbitrage</span><span class="sxs-lookup"><span data-stu-id="1a3f1-107">Discovery and Arbitration</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="1a3f1-108">Décodage</span><span class="sxs-lookup"><span data-stu-id="1a3f1-108">Decoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="1a3f1-109">Encodage</span><span class="sxs-lookup"><span data-stu-id="1a3f1-109">Encoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="1a3f1-110">Durée de vie d’un codec</span><span class="sxs-lookup"><span data-stu-id="1a3f1-110">The Lifetime of a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="1a3f1-111">Guide pratique pour activer un codec dans WIC</span><span class="sxs-lookup"><span data-stu-id="1a3f1-111">How to WIC-enable a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="1a3f1-112">Prise en charge du cloisonnement multithread dans WIC</span><span class="sxs-lookup"><span data-stu-id="1a3f1-112">Multi-Threaded Apartment Support in WIC</span></span>](-wic-howwicworks.md)  
<span data-ttu-id="1a3f1-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implémentation d’un décodeur WIC-Enabled</a></span><span class="sxs-lookup"><span data-stu-id="1a3f1-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementing a WIC-Enabled Decoder</a></span></span><dl>

[<span data-ttu-id="1a3f1-114">Interfaces de décodeur</span><span class="sxs-lookup"><span data-stu-id="1a3f1-114">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)<dl>

[<span data-ttu-id="1a3f1-115">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="1a3f1-115">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)  
[<span data-ttu-id="1a3f1-116">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="1a3f1-116">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[<span data-ttu-id="1a3f1-117">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="1a3f1-117">IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)  
[<span data-ttu-id="1a3f1-118">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="1a3f1-118">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)  
[<span data-ttu-id="1a3f1-119">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="1a3f1-119">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)  
[<span data-ttu-id="1a3f1-120">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="1a3f1-120">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)  
[<span data-ttu-id="1a3f1-121">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="1a3f1-121">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)  
<span data-ttu-id="1a3f1-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implémentation d’un encodeur WIC-Enabled</a>  
</span><span class="sxs-lookup"><span data-stu-id="1a3f1-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementing a WIC-Enabled Encoder</a>  
</span></span><dl>

[<span data-ttu-id="1a3f1-123">Interfaces d’encodeur</span><span class="sxs-lookup"><span data-stu-id="1a3f1-123">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)  
<dl>

[<span data-ttu-id="1a3f1-124">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="1a3f1-124">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)  
[<span data-ttu-id="1a3f1-125">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="1a3f1-125">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[<span data-ttu-id="1a3f1-126">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="1a3f1-126">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)  
[<span data-ttu-id="1a3f1-127">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="1a3f1-127">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)  
<span data-ttu-id="1a3f1-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Installation et inscription du codec</a>  
</span><span class="sxs-lookup"><span data-stu-id="1a3f1-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec Installation and Registration</a>  
</span></span><dl>

[<span data-ttu-id="1a3f1-129">Inscription d’un codec</span><span class="sxs-lookup"><span data-stu-id="1a3f1-129">Registering a Codec</span></span>](-wic-codecinstallandreg.md)  
<dl>

[<span data-ttu-id="1a3f1-130">Entrées générales du Registre</span><span class="sxs-lookup"><span data-stu-id="1a3f1-130">General Register Entries</span></span>](-wic-generalregentries.md)  
[<span data-ttu-id="1a3f1-131">Entrées de Registre spécifiques à l’encodeur</span><span class="sxs-lookup"><span data-stu-id="1a3f1-131">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)  
<dl>

[<span data-ttu-id="1a3f1-132">Inscription d’un format de conteneur avec des enregistreurs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="1a3f1-132">Registering a Container Format with Metadata Writers</span></span>](-wic-encoderregentries.md)  
<span data-ttu-id="1a3f1-133"></dl> </dd> <a href="-wic-decoderregentries.md">Entrées de Registre spécifiques à l’encodeur</a>  
</span><span class="sxs-lookup"><span data-stu-id="1a3f1-133"></dl> </dd> <a href="-wic-decoderregentries.md">Encoder-Specific Registry Entries</a>  
</span></span><dl>

[<span data-ttu-id="1a3f1-134">Inscription d’un nouveau format de conteneur avec des lecteurs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="1a3f1-134">Registering a New Container Format with Metadata Readers</span></span>](-wic-decoderregentries.md)  
<span data-ttu-id="1a3f1-135"></dl> </dd> <a href="-wic-integrationregentries.md">Intégration à la Galerie et à l’Explorateur Windows Vista</a>  
</span><span class="sxs-lookup"><span data-stu-id="1a3f1-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integration with Windows Vista PhotoGallery and Explorer</a>  
</span></span><dl>

[<span data-ttu-id="1a3f1-136">Magasin de propriétés Windows</span><span class="sxs-lookup"><span data-stu-id="1a3f1-136">Windows Property Store</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="1a3f1-137">Galerie de photos Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a3f1-137">Windows Vista Photo Gallery</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="1a3f1-138">Cache de miniatures Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a3f1-138">Windows Vista Thumbnail Cache</span></span>](-wic-integrationregentries.md)  
<span data-ttu-id="1a3f1-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Mise à jour du cache de miniatures lors de l’installation d’un codec</a> [mettant votre WIC-Enabled codec à la disposition des utilisateurs](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">conclusion</a>  
</span><span class="sxs-lookup"><span data-stu-id="1a3f1-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Updating the Thumbnail Cache when Installing a Codec</a> [Making Your WIC-Enabled Codec Available to Users](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">Conclusion</a>  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="1a3f1-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a3f1-140">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1a3f1-141">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1a3f1-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1a3f1-142">Introduction (écriture d’un CODEC WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="1a3f1-142">Introduction (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[<span data-ttu-id="1a3f1-143">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="1a3f1-143">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



