---
description: Le composant WIC (Windows Imaging Component) fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Vue d’ensemble du composant Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203234"
---
# <a name="windows-imaging-component-overview"></a><span data-ttu-id="accf7-103">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="accf7-103">Windows Imaging Component Overview</span></span>

<span data-ttu-id="accf7-104">Le composant WIC (Windows Imaging Component) fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image.</span><span class="sxs-lookup"><span data-stu-id="accf7-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="accf7-105">WIC permet aux éditeurs de logiciels indépendants et aux fabricants de matériel indépendants (IHV) de développer leurs propres codecs d’image et d’obtenir la même prise en charge de plate-forme que les formats d’images standard (par exemple, TIFF, JPEG, PNG, GIF, BMP et HDPhoto).</span><span class="sxs-lookup"><span data-stu-id="accf7-105">WIC makes it possible for independent software vendors (ISVs) and independent hardware vendors (IHVs) to develop their own image codecs and get the same platform support as standard image formats (for example, TIFF, JPEG, PNG, GIF, BMP, and HDPhoto).</span></span> <span data-ttu-id="accf7-106">Un ensemble unique et cohérent d’interfaces est utilisé pour le traitement de tous les images, quel que soit le format d’image, de sorte que toute application utilisant le WIC obtient la prise en charge automatique des nouveaux formats d’image dès l’installation du codec.</span><span class="sxs-lookup"><span data-stu-id="accf7-106">A single, consistent set of interfaces is used for all image processing, regardless of image format, so any application using the WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="accf7-107">L’infrastructure de métadonnées extensible permet aux applications de lire et d’écrire leurs propres métadonnées propriétaires directement dans des fichiers image, de sorte que les métadonnées ne sont jamais perdues ou séparées de l’image.</span><span class="sxs-lookup"><span data-stu-id="accf7-107">The extensible metadata framework makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata never gets lost or separated from the image.</span></span>

<span data-ttu-id="accf7-108">Cette rubrique comprend les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="accf7-108">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="accf7-109">Fonctionnalités du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="accf7-109">Windows Imaging Component Features</span></span>](#windows-imaging-component-features)
-   [<span data-ttu-id="accf7-110">Codecs natifs</span><span class="sxs-lookup"><span data-stu-id="accf7-110">Native Codecs</span></span>](#native-codecs)
-   [<span data-ttu-id="accf7-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="accf7-111">Related topics</span></span>](#related-topics)

## <a name="windows-imaging-component-features"></a><span data-ttu-id="accf7-112">Fonctionnalités du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="accf7-112">Windows Imaging Component Features</span></span>

<span data-ttu-id="accf7-113">Les principales fonctionnalités de WIC sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="accf7-113">The primary features of WIC are:</span></span>

-   <span data-ttu-id="accf7-114">Permet aux développeurs d’applications d’effectuer des opérations de traitement d’image sur n’importe quel format d’image via un ensemble unique et cohérent d’interfaces courantes, sans avoir besoin d’une connaissance préalable des formats d’image spécifiques.</span><span class="sxs-lookup"><span data-stu-id="accf7-114">Enables application developers to perform image processing operations on any image format through a single, consistent set of common interfaces, without requiring prior knowledge of specific image formats.</span></span>
-   <span data-ttu-id="accf7-115">Fournit une architecture « plug-and-Play » extensible pour les codecs d’image, les formats de pixel et les métadonnées, avec la découverte automatique de nouveaux formats au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="accf7-115">Provides an extensible "plug and play" architecture for image codecs, pixel formats, and metadata, with automatic run-time discovery of new formats.</span></span>
-   <span data-ttu-id="accf7-116">Prend en charge la lecture et l’écriture de métadonnées arbitraires dans les fichiers image, avec la possibilité de conserver les métadonnées non reconnues pendant la modification.</span><span class="sxs-lookup"><span data-stu-id="accf7-116">Supports reading and writing of arbitrary metadata in image files, with the ability to preserve unrecognized metadata during editing.</span></span>
-   <span data-ttu-id="accf7-117">Préserve les données d’image de profondeur de bits élevées, jusqu’à 32 bits par canal, dans le pipeline de traitement d’image.</span><span class="sxs-lookup"><span data-stu-id="accf7-117">Preserves high bit depth image data, up to 32 bits per channel, throughout the image processing pipeline.</span></span>
-   <span data-ttu-id="accf7-118">Offre une prise en charge intégrée des formats d’image, des formats de pixel et des schémas de métadonnées les plus populaires.</span><span class="sxs-lookup"><span data-stu-id="accf7-118">Provides built-in support for most popular image formats, pixel formats, and metadata schemas.</span></span>

## <a name="native-codecs"></a><span data-ttu-id="accf7-119">Codecs natifs</span><span class="sxs-lookup"><span data-stu-id="accf7-119">Native Codecs</span></span>

<span data-ttu-id="accf7-120">WIC comprend plusieurs codecs intégrés.</span><span class="sxs-lookup"><span data-stu-id="accf7-120">WIC includes several built-in codecs.</span></span> <span data-ttu-id="accf7-121">Les codecs standard suivants sont fournis avec la plateforme.</span><span class="sxs-lookup"><span data-stu-id="accf7-121">The following standard codecs are provided with the platform.</span></span> 

| <span data-ttu-id="accf7-122">Codec</span><span class="sxs-lookup"><span data-stu-id="accf7-122">Codec</span></span>                                                                                             | <span data-ttu-id="accf7-123">Types MIME</span><span class="sxs-lookup"><span data-stu-id="accf7-123">Mime Types</span></span>                       | <span data-ttu-id="accf7-124">Décodeurs</span><span class="sxs-lookup"><span data-stu-id="accf7-124">Decoders</span></span> | <span data-ttu-id="accf7-125">Encodeurs</span><span class="sxs-lookup"><span data-stu-id="accf7-125">Encoders</span></span> |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| <span data-ttu-id="accf7-126">BMP (format bitmap Windows), BMP Specification v5.</span><span class="sxs-lookup"><span data-stu-id="accf7-126">BMP (Windows Bitmap Format), BMP Specification v5.</span></span>                                                | <span data-ttu-id="accf7-127">image/bmp</span><span class="sxs-lookup"><span data-stu-id="accf7-127">image/bmp</span></span>                        | <span data-ttu-id="accf7-128">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-128">Yes</span></span>      | <span data-ttu-id="accf7-129">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-129">Yes</span></span>      |
| <span data-ttu-id="accf7-130">GIF (Graphics Interchange format 89a), spécification GIF 89a/89m</span><span class="sxs-lookup"><span data-stu-id="accf7-130">GIF (Graphics Interchange Format 89a), GIF Specification 89a/89m</span></span>                                  | <span data-ttu-id="accf7-131">image/gif</span><span class="sxs-lookup"><span data-stu-id="accf7-131">image/gif</span></span>                        | <span data-ttu-id="accf7-132">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-132">Yes</span></span>      | <span data-ttu-id="accf7-133">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-133">Yes</span></span>      |
| <span data-ttu-id="accf7-134">ICO (format d’icône)</span><span class="sxs-lookup"><span data-stu-id="accf7-134">ICO (Icon Format)</span></span>                                                                                 | <span data-ttu-id="accf7-135">image/ico</span><span class="sxs-lookup"><span data-stu-id="accf7-135">image/ico</span></span>                        | <span data-ttu-id="accf7-136">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-136">Yes</span></span>      | <span data-ttu-id="accf7-137">Non</span><span class="sxs-lookup"><span data-stu-id="accf7-137">No</span></span>       |
| <span data-ttu-id="accf7-138">JPEG (Joint Photographic Experts Group), spécification d’JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="accf7-138">JPEG (Joint Photographic Experts Group), JFIF Specification 1.02</span></span>                                  | <span data-ttu-id="accf7-139">image/JPEG, image/JPE, image/jpg</span><span class="sxs-lookup"><span data-stu-id="accf7-139">image/jpeg, image/jpe, image/jpg</span></span> | <span data-ttu-id="accf7-140">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-140">Yes</span></span>      | <span data-ttu-id="accf7-141">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-141">Yes</span></span>      |
| <span data-ttu-id="accf7-142">PNG (Portable Network Graphics), spécification PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="accf7-142">PNG (Portable Network Graphics), PNG Specification 1.2</span></span>                                            | <span data-ttu-id="accf7-143">image/png</span><span class="sxs-lookup"><span data-stu-id="accf7-143">image/png</span></span>                        | <span data-ttu-id="accf7-144">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-144">Yes</span></span>      | <span data-ttu-id="accf7-145">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-145">Yes</span></span>      |
| <span data-ttu-id="accf7-146">TIFF (Tagged Image File Format), spécification TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="accf7-146">TIFF (Tagged Image File Format), TIFF Specification 6.0</span></span>                                           | <span data-ttu-id="accf7-147">image/TIFF, image/TIF</span><span class="sxs-lookup"><span data-stu-id="accf7-147">image/tiff, image/tif</span></span>            | <span data-ttu-id="accf7-148">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-148">Yes</span></span>      | <span data-ttu-id="accf7-149">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-149">Yes</span></span>      |
| <span data-ttu-id="accf7-150">Windows Media photo, [spécification de photo HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span><span class="sxs-lookup"><span data-stu-id="accf7-150">Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span></span> | <span data-ttu-id="accf7-151">image/vnd. ms-phot</span><span class="sxs-lookup"><span data-stu-id="accf7-151">image/vnd.ms-phot</span></span>                | <span data-ttu-id="accf7-152">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-152">Yes</span></span>      | <span data-ttu-id="accf7-153">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-153">Yes</span></span>      |
| <span data-ttu-id="accf7-154">DDS (surface DirectDraw)</span><span class="sxs-lookup"><span data-stu-id="accf7-154">DDS (DirectDraw Surface)</span></span>                                                                          | <span data-ttu-id="accf7-155">image/vnd. ms-DDS</span><span class="sxs-lookup"><span data-stu-id="accf7-155">image/vnd.ms-dds</span></span>                 | <span data-ttu-id="accf7-156">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-156">Yes</span></span>      | <span data-ttu-id="accf7-157">Oui</span><span class="sxs-lookup"><span data-stu-id="accf7-157">Yes</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="accf7-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="accf7-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="accf7-159">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="accf7-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="accf7-160">Vue d’ensemble des métadonnées WIC</span><span class="sxs-lookup"><span data-stu-id="accf7-160">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

<span data-ttu-id="accf7-161">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="accf7-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="accf7-162">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="accf7-162">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

<span data-ttu-id="accf7-163">[Exemple de CODEC AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="accf7-163">[AITCodec Sample CODEC](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span></span>
</dt> </dl>

 

 
