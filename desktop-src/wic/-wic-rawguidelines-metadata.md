---
description: Prise en charge des métadonnées
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Prise en charge des métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529352"
---
# <a name="metadata-support"></a><span data-ttu-id="9079c-103">Prise en charge des métadonnées</span><span class="sxs-lookup"><span data-stu-id="9079c-103">Metadata Support</span></span>

<span data-ttu-id="9079c-104">Les formats BRUTs doivent également prendre en charge les scénarios courants de lecture et d’écriture des métadonnées pour les images dans Windows.</span><span class="sxs-lookup"><span data-stu-id="9079c-104">RAW formats should also support the common metadata read and write scenarios for images in Windows.</span></span> <span data-ttu-id="9079c-105">Microsoft a développé un ensemble de fournisseurs de métadonnées natifs pour les métadonnées EXIF (Exchangeable Image File), IPTC (International Press Telecommunications Council) et XMP (Extensible Metadata Platform) qui sont actuellement appelés uniquement pour les conteneurs TIFF et JPEG.</span><span class="sxs-lookup"><span data-stu-id="9079c-105">Microsoft has developed a set of native metadata providers for exchangeable image file (EXIF), International Press Telecommunications Council (IPTC), and Extensible Metadata Platform (XMP) metadata that are currently invoked only for TIFF and JPEG containers.</span></span> <span data-ttu-id="9079c-106">Si l’image brute est stockée dans l’un de ces formats de conteneur, il est recommandé d’utiliser les fournisseurs de métadonnées intégrés Windows.</span><span class="sxs-lookup"><span data-stu-id="9079c-106">If the RAW image is stored in one of these container formats, it is recommended to use the Windows built-in metadata providers.</span></span> <span data-ttu-id="9079c-107">Toutefois, l’auteur du codec est chargé de la configurer correctement.</span><span class="sxs-lookup"><span data-stu-id="9079c-107">However, the codec author is responsible for configuring this properly.</span></span> <span data-ttu-id="9079c-108">Pour les fichiers BRUTs qui ne sont pas basés sur un conteneur TIFF, il peut être nécessaire d’implémenter des enregistreurs EXIF, IPTC ou XMP, car les lecteurs et les Writers intégrés s’attendent à ce que les données soient conformes aux spécifications de disposition sur disque EXIF, IPTC et XMP.</span><span class="sxs-lookup"><span data-stu-id="9079c-108">For RAW files that are not based on a TIFF container, it might be necessary to implement EXIF, IPTC, or XMP writers because the built-in readers and writers expect the data to conform to EXIF, IPTC, and XMP on-disk layout specifications.</span></span> <span data-ttu-id="9079c-109">Les auteurs de codec peuvent également implémenter leurs propres fournisseurs pour toutes les métadonnées personnalisées.</span><span class="sxs-lookup"><span data-stu-id="9079c-109">Codec authors can also implement their own providers for any custom metadata.</span></span>

<span data-ttu-id="9079c-110">En raison de l’architecture du composant WIC (Windows Imaging Component), les enregistreurs de métadonnées peuvent être appelés uniquement par le biais d’une instance d’un encodeur d’image.</span><span class="sxs-lookup"><span data-stu-id="9079c-110">Because of the architecture of Windows Imaging Component (WIC), metadata writers can be invoked only through an instance of an image encoder.</span></span> <span data-ttu-id="9079c-111">Par conséquent, les propriétaires de format brut doivent créer au moins un encodeur [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) , même si l’encodage réel des pixels dans un format brut n’est pas implémenté.</span><span class="sxs-lookup"><span data-stu-id="9079c-111">Therefore, RAW format owners should create at least a "stub" [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) encoder, even if the actual encoding of pixels into a RAW format is not implemented.</span></span> <span data-ttu-id="9079c-112">L’auteur du codec doit appeler les gestionnaires de métadonnées appropriés :</span><span class="sxs-lookup"><span data-stu-id="9079c-112">The codec author must invoke the proper metadata handlers:</span></span>

-   <span data-ttu-id="9079c-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) sur le décodeur et le décodeur de trame, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9079c-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on both the decoder and frame decoder as appropriate.</span></span>
-   <span data-ttu-id="9079c-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sur l’encodeur et l’encodeur de trame, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9079c-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on both the encoder and frame encoder as appropriate.</span></span>

<span data-ttu-id="9079c-115">Pour prendre en charge tous les scénarios anticipés dans les applications d’imagerie de Windows Vista, il est recommandé que les fournisseurs de codec prennent en charge les éléments suivants au minimum :</span><span class="sxs-lookup"><span data-stu-id="9079c-115">To support all of the anticipated scenarios in imaging applications in Windows Vista, it is recommended that codec vendors support the following at a minimum:</span></span>

-   <span data-ttu-id="9079c-116">Lecture EXIF</span><span class="sxs-lookup"><span data-stu-id="9079c-116">EXIF read</span></span>
-   <span data-ttu-id="9079c-117">Écriture EXIF partielle (pour autoriser les mises à jour pour capturer la date et l’heure)</span><span class="sxs-lookup"><span data-stu-id="9079c-117">Partial EXIF write (to permit updates to capture date and time)</span></span>
-   <span data-ttu-id="9079c-118">Lecture et écriture XMP (y compris éventuellement le noyau IPTC pour XMP)</span><span class="sxs-lookup"><span data-stu-id="9079c-118">XMP read and write (including optionally IPTC Core for XMP)</span></span>
-   <span data-ttu-id="9079c-119">IPTC IIMv4 lecture et écriture</span><span class="sxs-lookup"><span data-stu-id="9079c-119">IPTC IIMv4 read and write</span></span>

<span data-ttu-id="9079c-120">La majeure partie de l’accès aux métadonnées (lecture et écriture) dans Windows Vista se produit via l’interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) ou [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="9079c-120">Most of the metadata access (both read and write) in Windows Vista occurs through the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) or [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interface.</span></span> <span data-ttu-id="9079c-121">Par conséquent, pour participer aux expériences de métadonnées Windows Vista, les auteurs de codec brut doivent implémenter les méthodes [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) et [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="9079c-121">Therefore, to participate in the Windows Vista metadata experiences, RAW codec authors must implement the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9079c-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9079c-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9079c-123">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9079c-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9079c-124">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="9079c-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="9079c-125">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="9079c-125">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="9079c-126">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="9079c-126">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



