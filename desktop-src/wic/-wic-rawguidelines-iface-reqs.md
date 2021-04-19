---
description: Spécifications de la méthode d’interface
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Spécifications de la méthode d’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530675"
---
# <a name="interface-method-requirements"></a><span data-ttu-id="7a225-103">Spécifications de la méthode d’interface</span><span class="sxs-lookup"><span data-stu-id="7a225-103">Interface Method Requirements</span></span>

<span data-ttu-id="7a225-104">Aucune méthode sur chaque interface ne doit avoir une implémentation.</span><span class="sxs-lookup"><span data-stu-id="7a225-104">Not every method on every interface must have an implementation.</span></span> <span data-ttu-id="7a225-105">Par exemple, certains codecs ont des métadonnées globales, des miniatures ou des contextes de couleur, tandis que d’autres codec les fournissent uniquement pour chaque image.</span><span class="sxs-lookup"><span data-stu-id="7a225-105">For example, some codecs have global metadata, thumbnails, or color contexts, whereas other codecs provide these only on a per-frame basis.</span></span> <span data-ttu-id="7a225-106">Si les auteurs de codec ne les fournissent qu’en fonction [**de la**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)trame, ils ont uniquement besoin d’implémenter / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) ou ColorContexts, ou d’implémenter les méthodes [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) ou [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) sur [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) et [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) plutôt que sur [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="7a225-106">If codec authors provide these only on a per-frame basis, they need only implement the [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) or ColorContexts, or implement the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) or [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) rather than on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span> <span data-ttu-id="7a225-107">De même, certains codecs n’utilisent pas de formats indexés et n’ont donc pas besoin d’implémenter les méthodes [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) et [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="7a225-107">Likewise, some codecs do not use indexed formats and so are not required to implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) and [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) methods.</span></span> <span data-ttu-id="7a225-108">Ces méthodes sont donc facultatives et restent à la discrétion du créateur du codec.</span><span class="sxs-lookup"><span data-stu-id="7a225-108">These methods are therefore optional and are left to the discretion of the codec creator.</span></span> <span data-ttu-id="7a225-109">La plupart des autres méthodes sont requises.</span><span class="sxs-lookup"><span data-stu-id="7a225-109">Most other methods are required.</span></span>

<span data-ttu-id="7a225-110">Pour Windows 7, [**obtenir**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) et [**obtenir**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)des / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) sont requis et doivent être implémentés sur les classes de niveau conteneur ou sur les classes de niveau Frame.</span><span class="sxs-lookup"><span data-stu-id="7a225-110">For Windows 7 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)/[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) and [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) are required and must be implemented on either the contain-level classes or on the frame-level classes.</span></span> <span data-ttu-id="7a225-111">Si votre format de fichier image ne prend pas en charge les aperçus ou les miniatures dans l’un de ces emplacements, vous devez modifier votre format de fichier image pour fournir une telle prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7a225-111">If your image file format doesn't support previews or thumbnails in either of these locations, then you should revise your image file format to provide such support.</span></span>

<span data-ttu-id="7a225-112">Lorsqu’une méthode n’est pas implémentée, il est important de retourner une erreur appropriée afin que l’appelant puisse déterminer que la fonctionnalité demandée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7a225-112">When a method is not implemented, it is important to return an appropriate error so the caller can determine that the requested feature is not supported.</span></span> <span data-ttu-id="7a225-113">Par exemple, si les auteurs de codec ne prennent pas en charge les miniatures au niveau du conteneur, ils doivent retourner [WINCODEC \_ Err \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) lorsqu’une application appelle [**miniature**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)et, si elles n’ont pas de palette, elles doivent retourner [WINCODEC \_ Err \_ PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7a225-113">For example, if codec authors do not support container-level thumbnails, they should return [WINCODEC\_ERR\_CODECNOTHUMBNAIL](-wic-codec-error-codes.md) when an application calls [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), and if they don't have a palette, they should return [WINCODEC\_ERR\_PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span></span> <span data-ttu-id="7a225-114">S’il n’existe aucun code d' [ \_ erreur WINCODEC](-wic-codec-error-codes.md) approprié, le codec doit retourner E \_ NOTIMPL pour les méthodes non implémentées.</span><span class="sxs-lookup"><span data-stu-id="7a225-114">If no suitable [WINCODEC\_ERR](-wic-codec-error-codes.md) code exists, then the codec should return E\_NOTIMPL for unimplemented methods.</span></span>

<span data-ttu-id="7a225-115">Les tableaux suivants répertorient les méthodes obligatoires et facultatives pour chaque interface WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="7a225-115">The following tables list the required and optional methods for each Windows Imaging Component (WIC) interfaces.</span></span>

[<span data-ttu-id="7a225-116">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="7a225-116">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



<span data-ttu-id="7a225-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a225-117">Required</span></span>

[<span data-ttu-id="7a225-118">**QueryCapability**</span><span class="sxs-lookup"><span data-stu-id="7a225-118">**QueryCapability**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[<span data-ttu-id="7a225-119">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="7a225-119">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[<span data-ttu-id="7a225-120">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="7a225-120">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[<span data-ttu-id="7a225-121">**GetDecoderInfo**</span><span class="sxs-lookup"><span data-stu-id="7a225-121">**GetDecoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[<span data-ttu-id="7a225-122">**GetFrameCount**</span><span class="sxs-lookup"><span data-stu-id="7a225-122">**GetFrameCount**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[<span data-ttu-id="7a225-123">**GetFrame**</span><span class="sxs-lookup"><span data-stu-id="7a225-123">**GetFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

<span data-ttu-id="7a225-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7a225-124">Optional</span></span>

<span data-ttu-id="7a225-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span><span class="sxs-lookup"><span data-stu-id="7a225-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span></span>

<span data-ttu-id="7a225-126">[**Miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="7a225-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span></span>

[<span data-ttu-id="7a225-127">**GetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="7a225-127">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[<span data-ttu-id="7a225-128">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="7a225-128">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[<span data-ttu-id="7a225-129">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="7a225-129">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="7a225-130">¹ requis si votre format de fichier image prend en charge les aperçus au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="7a225-130">¹Required if your image file format supports container-level previews.</span></span> <span data-ttu-id="7a225-131">Si ce n’est pas le cas, il est vivement recommandé de modifier le format de votre fichier image pour le prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="7a225-131">If this is not the case you are strongly encouraged to revise your image file format to support this.</span></span> <span data-ttu-id="7a225-132">Si elle est implémentée ici, un [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) correspondant est requis sur la classe encode au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="7a225-132">If implemented here, then a corresponding [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) is required on the container-level encode class.</span></span>

<span data-ttu-id="7a225-133">² requis ici, ou sur la classe de décodage au niveau de la trame, selon l’emplacement de stockage des miniatures dans le format de fichier image.</span><span class="sxs-lookup"><span data-stu-id="7a225-133">²Required either here, or on the frame-level decode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="7a225-134">Si elle est implémentée ici, un [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) correspondant est requis sur la classe encode au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="7a225-134">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) is required on the container-level encode class.</span></span>

[<span data-ttu-id="7a225-135">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="7a225-135">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



<span data-ttu-id="7a225-136">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a225-136">Required</span></span>

[<span data-ttu-id="7a225-137">**GetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="7a225-137">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[<span data-ttu-id="7a225-138">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="7a225-138">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[<span data-ttu-id="7a225-139">**GetSize,**</span><span class="sxs-lookup"><span data-stu-id="7a225-139">**GetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[<span data-ttu-id="7a225-140">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="7a225-140">**GetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[<span data-ttu-id="7a225-141">**GetResolution**</span><span class="sxs-lookup"><span data-stu-id="7a225-141">**GetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[<span data-ttu-id="7a225-142">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="7a225-142">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

<span data-ttu-id="7a225-143">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7a225-143">Optional</span></span>

<span data-ttu-id="7a225-144">[**Miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="7a225-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span></span>

[<span data-ttu-id="7a225-145">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="7a225-145">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="7a225-146">¹ requis ici, ou sur la classe de décodage au niveau du conteneur, selon l’endroit où vous stockez les miniatures dans le format de fichier image.</span><span class="sxs-lookup"><span data-stu-id="7a225-146">¹Required either here, or on the container-level decode class, depending on where you image file format stores thumbnails.</span></span> <span data-ttu-id="7a225-147">Si elle est implémentée ici, un [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) correspondant est requis sur la classe de codeur au niveau de la trame.</span><span class="sxs-lookup"><span data-stu-id="7a225-147">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is required on the frame-level encoder class.</span></span>

[<span data-ttu-id="7a225-148">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="7a225-148">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="7a225-149">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a225-149">Required</span></span>

[<span data-ttu-id="7a225-150">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="7a225-150">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[<span data-ttu-id="7a225-151">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="7a225-151">**GetCount**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[<span data-ttu-id="7a225-152">**GetReaderByIndex**</span><span class="sxs-lookup"><span data-stu-id="7a225-152">**GetReaderByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[<span data-ttu-id="7a225-153">**GetEnumerator**</span><span class="sxs-lookup"><span data-stu-id="7a225-153">**GetEnumerator**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[<span data-ttu-id="7a225-154">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="7a225-154">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



<span data-ttu-id="7a225-155">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a225-155">Required</span></span>

[<span data-ttu-id="7a225-156">**DoesSupportTransform**</span><span class="sxs-lookup"><span data-stu-id="7a225-156">**DoesSupportTransform**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[<span data-ttu-id="7a225-157">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="7a225-157">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

<span data-ttu-id="7a225-158">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7a225-158">Optional</span></span>

[<span data-ttu-id="7a225-159">**GetClosestSize**</span><span class="sxs-lookup"><span data-stu-id="7a225-159">**GetClosestSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[<span data-ttu-id="7a225-160">**GetClosestPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="7a225-160">**GetClosestPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[<span data-ttu-id="7a225-161">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="7a225-161">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

<span data-ttu-id="7a225-162">Consultez [prise en charge de IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), plus loin dans ce document.</span><span class="sxs-lookup"><span data-stu-id="7a225-162">See [Support for IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), later in this document.</span></span>

[<span data-ttu-id="7a225-163">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="7a225-163">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



<span data-ttu-id="7a225-164">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a225-164">Required</span></span>

[<span data-ttu-id="7a225-165">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="7a225-165">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="7a225-166">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="7a225-166">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[<span data-ttu-id="7a225-167">**GetEncoderInfo**</span><span class="sxs-lookup"><span data-stu-id="7a225-167">**GetEncoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[<span data-ttu-id="7a225-168">**CreateNewFrame**</span><span class="sxs-lookup"><span data-stu-id="7a225-168">**CreateNewFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[<span data-ttu-id="7a225-169">**Commit**</span><span class="sxs-lookup"><span data-stu-id="7a225-169">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="7a225-170">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7a225-170">Optional</span></span>

<span data-ttu-id="7a225-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span><span class="sxs-lookup"><span data-stu-id="7a225-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span></span>

<span data-ttu-id="7a225-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="7a225-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span></span>

[<span data-ttu-id="7a225-173">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="7a225-173">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[<span data-ttu-id="7a225-174">**GetMetadataQueryWriter**</span><span class="sxs-lookup"><span data-stu-id="7a225-174">**GetMetadataQueryWriter**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[<span data-ttu-id="7a225-175">**SetPalette**</span><span class="sxs-lookup"><span data-stu-id="7a225-175">**SetPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

<span data-ttu-id="7a225-176">¹ requis si votre format de fichier image prend en charge les aperçus au niveau de la trame.</span><span class="sxs-lookup"><span data-stu-id="7a225-176">¹Required if your image file format supports frame-level previews.</span></span>

<span data-ttu-id="7a225-177">² requis ici, ou sur la classe de codage au niveau de la trame, selon l’emplacement de stockage des miniatures dans le format de fichier image.</span><span class="sxs-lookup"><span data-stu-id="7a225-177">²Required either here, or on the frame-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="7a225-178">Si elle est implémentée ici, un [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) correspondant est requis sur la classe de décodage au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="7a225-178">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) is required on the container-level decode class.</span></span>

[<span data-ttu-id="7a225-179">**IWICBitmapFrameEncode**</span><span class="sxs-lookup"><span data-stu-id="7a225-179">**IWICBitmapFrameEncode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



<span data-ttu-id="7a225-180">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a225-180">Required</span></span>

[<span data-ttu-id="7a225-181">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="7a225-181">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="7a225-182">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="7a225-182">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="7a225-183">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="7a225-183">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="7a225-184">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="7a225-184">**SetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[<span data-ttu-id="7a225-185">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="7a225-185">**SetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[<span data-ttu-id="7a225-186">**SetResolution**</span><span class="sxs-lookup"><span data-stu-id="7a225-186">**SetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[<span data-ttu-id="7a225-187">**WritePixels**</span><span class="sxs-lookup"><span data-stu-id="7a225-187">**WritePixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[<span data-ttu-id="7a225-188">**WriteSource**</span><span class="sxs-lookup"><span data-stu-id="7a225-188">**WriteSource**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[<span data-ttu-id="7a225-189">**Commit**</span><span class="sxs-lookup"><span data-stu-id="7a225-189">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="7a225-190">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7a225-190">Optional</span></span>

<span data-ttu-id="7a225-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="7a225-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span></span>

[<span data-ttu-id="7a225-192">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="7a225-192">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

<span data-ttu-id="7a225-193">¹ requis ici ou sur la classe encode au niveau du conteneur, selon l’endroit où votre fichier image stocke les miniatures.</span><span class="sxs-lookup"><span data-stu-id="7a225-193">¹Required either here, or on the container-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="7a225-194">Si elle est implémentée ici, un [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) correspondant est requis sur la classe de décodage au niveau de la trame.</span><span class="sxs-lookup"><span data-stu-id="7a225-194">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) is required on the frame-level decode class.</span></span>

[<span data-ttu-id="7a225-195">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="7a225-195">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="7a225-196">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a225-196">Required</span></span>

[<span data-ttu-id="7a225-197">**InitializeFromBlockReader**</span><span class="sxs-lookup"><span data-stu-id="7a225-197">**InitializeFromBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[<span data-ttu-id="7a225-198">**AddWriter**</span><span class="sxs-lookup"><span data-stu-id="7a225-198">**AddWriter**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[<span data-ttu-id="7a225-199">**GetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="7a225-199">**GetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[<span data-ttu-id="7a225-200">**SetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="7a225-200">**SetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[<span data-ttu-id="7a225-201">**RemoveWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="7a225-201">**RemoveWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a><span data-ttu-id="7a225-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a225-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7a225-203">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="7a225-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7a225-204">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="7a225-204">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="7a225-205">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="7a225-205">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="7a225-206">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="7a225-206">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
