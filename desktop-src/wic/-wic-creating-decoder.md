---
description: La rubrique présente le décodeur bitmap, un principal composant codec WIC (Windows Imaging Component) utilisé pour décoder les fichiers image d’un flux.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Décodage, vue d’ensemble
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320925"
---
# <a name="decoding-overview"></a><span data-ttu-id="fb7b3-103">Décodage, vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="fb7b3-103">Decoding Overview</span></span>

<span data-ttu-id="fb7b3-104">La rubrique présente le décodeur bitmap, un principal composant codec WIC (Windows Imaging Component) utilisé pour décoder les fichiers image d’un flux.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-104">The topic introduces the bitmap decoder, a core Windows Imaging Component (WIC) codec component used to decode image files from a stream.</span></span>

<span data-ttu-id="fb7b3-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fb7b3-106">Introduction</span><span class="sxs-lookup"><span data-stu-id="fb7b3-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="fb7b3-107">Décodeurs bitmap natifs</span><span class="sxs-lookup"><span data-stu-id="fb7b3-107">Native Bitmap Decoders</span></span>](#native-bitmap-decoders)
-   [<span data-ttu-id="fb7b3-108">Création d’un décodeur bitmap</span><span class="sxs-lookup"><span data-stu-id="fb7b3-108">Creating a Bitmap Decoder</span></span>](#creating-a-bitmap-decoder)
-   [<span data-ttu-id="fb7b3-109">Extensibilité du décodeur</span><span class="sxs-lookup"><span data-stu-id="fb7b3-109">Decoder Extensibility</span></span>](#decoder-extensibility)
-   [<span data-ttu-id="fb7b3-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb7b3-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="fb7b3-111">Introduction</span><span class="sxs-lookup"><span data-stu-id="fb7b3-111">Introduction</span></span>

<span data-ttu-id="fb7b3-112">Les décodeurs bitmap peuvent être affichés comme conteneur externe d’une image numérique et permettent d’accéder à des propriétés globales et à des frames d’image.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-112">Bitmap decoders can be viewed as the outer container of a digital image and provides access to global properties and image frames.</span></span> <span data-ttu-id="fb7b3-113">Certains formats d’image prennent en charge les miniatures globales, les aperçus, les contextes de couleur ou les métadonnées, tandis que d’autres fournissent ces propriétés uniquement au niveau du frame.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-113">Some image formats support global thumbnails, previews, color contexts, or metadata, while others provide these properties only at the frame level.</span></span> <span data-ttu-id="fb7b3-114">Notez, toutefois, que la plupart des formats d’image standard ne prennent pas en charge ces propriétés globales.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-114">Note, however, many of the standard image formats do not support these global properties.</span></span> <span data-ttu-id="fb7b3-115">Ainsi, la plupart des implémentations de codec natives fournies par WIC ne prennent pas en charge la plupart de ces propriétés globales.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-115">As such, many of the native codec implementations provided by WIC do not support the majority of these global properties.</span></span> <span data-ttu-id="fb7b3-116">Pour plus d’informations sur la prise en charge des propriétés globales, consultez le tableau dans la section décodeurs bitmap natifs de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-116">See the table in the Native Bitmap Decoders section of this topic for information about global property support.</span></span>

<span data-ttu-id="fb7b3-117">Dans WIC, les décodeurs bitmap sont représentés par l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et fournissent l’accès à ces propriétés globales de la bitmap et, plus important encore, aux frames qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-117">In WIC, bitmap decoders are represented by the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface and provides access to these global properties of the bitmap and, more importantly, the frames it contains.</span></span> <span data-ttu-id="fb7b3-118">L’interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) représente un frame de bitmap individuel et est décrite en détail dans la [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="fb7b3-118">The [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface represents an individual bitmap frame and is discussed in detail in the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="native-bitmap-decoders"></a><span data-ttu-id="fb7b3-119">Décodeurs bitmap natifs</span><span class="sxs-lookup"><span data-stu-id="fb7b3-119">Native Bitmap Decoders</span></span>

<span data-ttu-id="fb7b3-120">WIC fournit plusieurs implémentations natives de l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) pour les formats d’image Web standard et le format de photo HD à plage dynamique élevée.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-120">WIC provides several native implementations of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface for the standard web image formats and the high dynamic range HD Photo format.</span></span> <span data-ttu-id="fb7b3-121">Le tableau suivant répertorie les décodeurs natifs disponibles, le nom de l’identificateur de classe et la prise en charge des propriétés globales.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-121">The following table lists the available native decoders, class identifier name, and support for global properties.</span></span> <span data-ttu-id="fb7b3-122">Bien qu’une fonctionnalité ne prenne pas en charge une propriété telle que les miniatures au niveau global, le format d’image peut prendre en charge de telles propriétés au niveau du frame individuel.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-122">Though a feature may not support a property such as thumbnails at the global level, the image format may support such properties at the individual frame level.</span></span>



| <span data-ttu-id="fb7b3-123">Format d'image</span><span class="sxs-lookup"><span data-stu-id="fb7b3-123">Image Format</span></span> | <span data-ttu-id="fb7b3-124">Nom du CLSID</span><span class="sxs-lookup"><span data-stu-id="fb7b3-124">CLSID Name</span></span>            | <span data-ttu-id="fb7b3-125">Miniatures</span><span class="sxs-lookup"><span data-stu-id="fb7b3-125">Thumbnails</span></span> | <span data-ttu-id="fb7b3-126">Versions préliminaires</span><span class="sxs-lookup"><span data-stu-id="fb7b3-126">Previews</span></span> | <span data-ttu-id="fb7b3-127">Contextes de couleur</span><span class="sxs-lookup"><span data-stu-id="fb7b3-127">Color Contexts</span></span> | <span data-ttu-id="fb7b3-128">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="fb7b3-128">Metadata</span></span> |
|--------------|-----------------------|------------|----------|----------------|----------|
| <span data-ttu-id="fb7b3-129">BMP</span><span class="sxs-lookup"><span data-stu-id="fb7b3-129">BMP</span></span>          | <span data-ttu-id="fb7b3-130">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="fb7b3-130">CLSID\_WICBmpDecoder</span></span>  | <span data-ttu-id="fb7b3-131">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-131">No</span></span>         | <span data-ttu-id="fb7b3-132">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-132">No</span></span>       | <span data-ttu-id="fb7b3-133">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-133">No</span></span>             | <span data-ttu-id="fb7b3-134">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-134">No</span></span>       |
| <span data-ttu-id="fb7b3-135">GIF</span><span class="sxs-lookup"><span data-stu-id="fb7b3-135">GIF</span></span>          | <span data-ttu-id="fb7b3-136">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="fb7b3-136">CLSID\_WICGifDecoder</span></span>  | <span data-ttu-id="fb7b3-137">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-137">No</span></span>         | <span data-ttu-id="fb7b3-138">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-138">No</span></span>       | <span data-ttu-id="fb7b3-139">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-139">No</span></span>             | <span data-ttu-id="fb7b3-140">Oui</span><span class="sxs-lookup"><span data-stu-id="fb7b3-140">Yes</span></span>      |
| <span data-ttu-id="fb7b3-141">ICO</span><span class="sxs-lookup"><span data-stu-id="fb7b3-141">ICO</span></span>          | <span data-ttu-id="fb7b3-142">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="fb7b3-142">CLSID\_WICIcoDecoder</span></span>  | <span data-ttu-id="fb7b3-143">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-143">No</span></span>         | <span data-ttu-id="fb7b3-144">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-144">No</span></span>       | <span data-ttu-id="fb7b3-145">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-145">No</span></span>             | <span data-ttu-id="fb7b3-146">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-146">No</span></span>       |
| <span data-ttu-id="fb7b3-147">JPEG</span><span class="sxs-lookup"><span data-stu-id="fb7b3-147">JPEG</span></span>         | <span data-ttu-id="fb7b3-148">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="fb7b3-148">CLSID\_WICJpegDecoder</span></span> | <span data-ttu-id="fb7b3-149">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-149">No</span></span>         | <span data-ttu-id="fb7b3-150">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-150">No</span></span>       | <span data-ttu-id="fb7b3-151">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-151">No</span></span>             | <span data-ttu-id="fb7b3-152">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-152">No</span></span>       |
| <span data-ttu-id="fb7b3-153">PNG</span><span class="sxs-lookup"><span data-stu-id="fb7b3-153">PNG</span></span>          | <span data-ttu-id="fb7b3-154">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="fb7b3-154">CLSID\_WICPngDecoder</span></span>  | <span data-ttu-id="fb7b3-155">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-155">No</span></span>         | <span data-ttu-id="fb7b3-156">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-156">No</span></span>       | <span data-ttu-id="fb7b3-157">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-157">No</span></span>             | <span data-ttu-id="fb7b3-158">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-158">No</span></span>       |
| <span data-ttu-id="fb7b3-159">TIFF</span><span class="sxs-lookup"><span data-stu-id="fb7b3-159">TIFF</span></span>         | <span data-ttu-id="fb7b3-160">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="fb7b3-160">CLSID\_WICTiffDecoder</span></span> | <span data-ttu-id="fb7b3-161">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-161">No</span></span>         | <span data-ttu-id="fb7b3-162">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-162">No</span></span>       | <span data-ttu-id="fb7b3-163">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-163">No</span></span>             | <span data-ttu-id="fb7b3-164">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-164">No</span></span>       |
| <span data-ttu-id="fb7b3-165">Photo HD</span><span class="sxs-lookup"><span data-stu-id="fb7b3-165">HD Photo</span></span>     | <span data-ttu-id="fb7b3-166">CLSID \_ WICWmpDecoder</span><span class="sxs-lookup"><span data-stu-id="fb7b3-166">CLSID\_WICWmpDecoder</span></span>  | <span data-ttu-id="fb7b3-167">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-167">No</span></span>         | <span data-ttu-id="fb7b3-168">Oui</span><span class="sxs-lookup"><span data-stu-id="fb7b3-168">Yes</span></span>      | <span data-ttu-id="fb7b3-169">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-169">No</span></span>             | <span data-ttu-id="fb7b3-170">Non</span><span class="sxs-lookup"><span data-stu-id="fb7b3-170">No</span></span>       |



 

## <a name="creating-a-bitmap-decoder"></a><span data-ttu-id="fb7b3-171">Création d’un décodeur bitmap</span><span class="sxs-lookup"><span data-stu-id="fb7b3-171">Creating a Bitmap Decoder</span></span>

<span data-ttu-id="fb7b3-172">Pour décoder une image à l’aide de WIC, vous devez d’abord créer une instance de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) pour le format d’image ciblé.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-172">To decode an image using WIC, you first need to create an instance of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) for the targeted image format.</span></span> <span data-ttu-id="fb7b3-173">L’instance de décodeur vous permet d’accéder aux propriétés globales et aux métadonnées, si elles sont prises en charge, ainsi qu’aux trames d’image.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-173">The decoder instance enables you to access the global properties and metadata, if supported, as well as the image frames.</span></span> <span data-ttu-id="fb7b3-174">La fabrique d’images WIC, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), fournit plusieurs méthodes pour créer des décodeurs bitmap.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-174">The WIC imaging factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), provides several methods for creating bitmap decoders.</span></span> <span data-ttu-id="fb7b3-175">Les méthodes de fabrique suivantes sont fournies pour créer des décodeurs bitmap.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-175">The following factory methods are provided to create bitmap decoders.</span></span>

-   [<span data-ttu-id="fb7b3-176">**CreateDecoder**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-176">**CreateDecoder**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [<span data-ttu-id="fb7b3-177">**CreateDecoderFromFileHandle**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-177">**CreateDecoderFromFileHandle**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [<span data-ttu-id="fb7b3-178">**CreateDecoderFromFilename**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-178">**CreateDecoderFromFilename**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [<span data-ttu-id="fb7b3-179">**CreateDecoderFromStream**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-179">**CreateDecoderFromStream**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

<span data-ttu-id="fb7b3-180">Le code suivant montre comment créer un décodeur bitmap à l’aide d’un nom de fichier image et récupérer la première image de l’image.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-180">The following code demonstrates the how to create a bitmap decoder using an image filename and retrieve the first frame of the image.</span></span>


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a><span data-ttu-id="fb7b3-181">Extensibilité du décodeur</span><span class="sxs-lookup"><span data-stu-id="fb7b3-181">Decoder Extensibility</span></span>

<span data-ttu-id="fb7b3-182">L’une des principales fonctionnalités de WIC est un Framework d’extensibilité qui permet aux développeurs de codec de développer leurs propres codecs d’image et d’avoir la même prise en charge de plate-forme que les implémentations natives de codecs d’image.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-182">One of the core features of WIC is an extensibility framework that enables codec developers to develop their own image codecs and get the same platform support as the native implementations of image codecs.</span></span> <span data-ttu-id="fb7b3-183">Un ensemble unique et cohérent d’interfaces est utilisé pour le traitement de tous les images, quel que soit le format d’image.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-183">A single, consistent set of interfaces is used for all image processing, regardless of image format.</span></span> <span data-ttu-id="fb7b3-184">Toute application utilisant WIC obtient la prise en charge automatique des nouveaux formats d’image dès que le codec est installé.</span><span class="sxs-lookup"><span data-stu-id="fb7b3-184">Any application using WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="fb7b3-185">Pour plus d’informations sur le développement de codecs, consultez les rubriques relatives au [développement de composants](-wic-component-development.md).</span><span class="sxs-lookup"><span data-stu-id="fb7b3-185">For more information on codec development, see the topics in [Component Development](-wic-component-development.md).</span></span> <span data-ttu-id="fb7b3-186">Pour plus d’informations sur le développement d’un décodeur, consultez [implémentation d’un décodeur de WIC-Enabled](-wic-implementingwicdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="fb7b3-186">For more information on decoder development, see [Implementing a WIC-Enabled Decoder](-wic-implementingwicdecoder.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb7b3-187">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb7b3-187">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fb7b3-188">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="fb7b3-188">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fb7b3-189">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="fb7b3-189">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="fb7b3-190">Vue d’ensemble de l’encodage</span><span class="sxs-lookup"><span data-stu-id="fb7b3-190">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> <dt>

[<span data-ttu-id="fb7b3-191">Développement de composants</span><span class="sxs-lookup"><span data-stu-id="fb7b3-191">Component Development</span></span>](-wic-component-development.md)
</dt> </dl>

 

 



