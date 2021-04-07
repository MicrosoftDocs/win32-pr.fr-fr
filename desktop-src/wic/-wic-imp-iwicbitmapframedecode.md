---
description: Implémentation de IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implémentation de IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758302"
---
# <a name="implementing-iwicbitmapframedecode"></a><span data-ttu-id="91541-103">Implémentation de IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="91541-103">Implementing IWICBitmapFrameDecode</span></span>

## <a name="iwicbitmapframedecode"></a><span data-ttu-id="91541-104">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="91541-104">IWICBitmapFrameDecode</span></span>

<span data-ttu-id="91541-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) est l’interface au niveau de la trame qui fournit l’accès aux bits d’image réels.</span><span class="sxs-lookup"><span data-stu-id="91541-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) is the frame-level interface that provides access to the actual image bits.</span></span> <span data-ttu-id="91541-106">Vous implémentez cette interface sur votre classe de décodage au niveau de la trame.</span><span class="sxs-lookup"><span data-stu-id="91541-106">You implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="91541-107">Comme elle est dérivée de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), votre implémentation de **IWICBitmapFrameDecode** inclura une implémentation des méthodes **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="91541-107">Because it’s derived from [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), your implementation of **IWICBitmapFrameDecode** will include an implementation of the **IWICBitmapSource** methods.</span></span> <span data-ttu-id="91541-108">Les méthodes supplémentaires sur **IWICBitmapFrameDecode** permettent d’accéder à la miniature au niveau de la trame, à tous les contextes de couleur de l’image et au lecteur de requêtes de métadonnées pour le frame.</span><span class="sxs-lookup"><span data-stu-id="91541-108">The additional methods on **IWICBitmapFrameDecode** provide access to the frame-level thumbnail, any color contexts for the image, and the metadata query reader for the frame.</span></span>

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [<span data-ttu-id="91541-109">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="91541-109">GetThumbnail</span></span>](#getthumbnail)
-   [<span data-ttu-id="91541-110">GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="91541-110">GetColorContexts</span></span>](#getcolorcontexts)
-   [<span data-ttu-id="91541-111">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="91541-111">GetMetadataQueryReader</span></span>](#getmetadataqueryreader)
-   [<span data-ttu-id="91541-112">Obtient, GetPixelFormat et GetResolution</span><span class="sxs-lookup"><span data-stu-id="91541-112">GetSize, GetPixelFormat, and GetResolution</span></span>](#getsize-getpixelformat-and-getresolution)
-   [<span data-ttu-id="91541-113">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="91541-113">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="91541-114">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="91541-114">CopyPalette</span></span>](#copypalette)

### <a name="getthumbnail"></a><span data-ttu-id="91541-115">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="91541-115">GetThumbnail</span></span>

<span data-ttu-id="91541-116">[**Miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) retourne la miniature du frame actuel.</span><span class="sxs-lookup"><span data-stu-id="91541-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) returns the thumbnail for the current frame.</span></span> <span data-ttu-id="91541-117">Pour des raisons de performances, les miniatures sont généralement encodées au format JPEG.</span><span class="sxs-lookup"><span data-stu-id="91541-117">For performance reasons, thumbnails are most commonly encoded in a JPEG format.</span></span> <span data-ttu-id="91541-118">Tout comme avec l’aperçu sur le décodeur, il n’est pas nécessaire ou recommandé de fournir votre propre décodeur JPEG pour les miniatures.</span><span class="sxs-lookup"><span data-stu-id="91541-118">Just as with the Preview on the decoder, it is not necessary or recommended to provide your own JPEG decoder for thumbnails.</span></span> <span data-ttu-id="91541-119">Au lieu de cela, vous devez déléguer au décodeur JPEG fourni par Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="91541-119">Instead, you should delegate to the JPEG decoder provided by Windows Imaging Component (WIC).</span></span>

<span data-ttu-id="91541-120">Pour plus d’informations sur les miniatures, consultez la méthode [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) sur l' [implémentation de IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span><span class="sxs-lookup"><span data-stu-id="91541-120">For more information on thumbnails, see the [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) method on [Implementing IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span></span>

### <a name="getcolorcontexts"></a><span data-ttu-id="91541-121">GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="91541-121">GetColorContexts</span></span>

<span data-ttu-id="91541-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) retourne les contextes de couleur valides (également appelés profils de couleurs) associés à l’image dans ce frame.</span><span class="sxs-lookup"><span data-stu-id="91541-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) returns the valid color contexts (also known as color profiles) associated with the image in this frame.</span></span> <span data-ttu-id="91541-123">Dans la plupart des cas, il ne s’agit que d’un seul, mais il peut y avoir des cas où il y a deux ou, rarement, plus.</span><span class="sxs-lookup"><span data-stu-id="91541-123">In most cases, this will only be one, but there could be cases where there are two or, rarely, more.</span></span> <span data-ttu-id="91541-124">L’appelant passera un ou plusieurs objets [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , en définissant le paramètre *ompte* pour indiquer le nombre de fois qu’ils sont transmis.</span><span class="sxs-lookup"><span data-stu-id="91541-124">The caller will pass in one or more [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects, setting the *cCount* parameter to indicate how many they are passing in.</span></span> <span data-ttu-id="91541-125">Cette méthode remplit les objets **IWICColorContext** avec les données de contexte de couleur réelles pour les profils de couleur associés à l’image.</span><span class="sxs-lookup"><span data-stu-id="91541-125">This method populates the **IWICColorContext** objects with the actual color context data for the color profiles associated with the image.</span></span> <span data-ttu-id="91541-126">Définissez le paramètre *pcActualCount* sur le nombre réel de contextes de couleur associés à l’image, même si cette valeur est supérieure au nombre que vous pouvez retourner.</span><span class="sxs-lookup"><span data-stu-id="91541-126">Set the *pcActualCount* parameter to the actual number of color contexts associated with the image, even if this is greater than the number you can return.</span></span> <span data-ttu-id="91541-127">(Dans le cas où d’autres contextes de couleur sont disponibles que le nombre d’objets **IWICColorContext** transmis par l’appelant, cela indique à l’appelant qu’un ou plusieurs autres contextes sont disponibles.)</span><span class="sxs-lookup"><span data-stu-id="91541-127">(In the case where more color contexts are available than the number of **IWICColorContext** objects passed in by the caller, this tells the caller there are one or more others available.)</span></span>

### <a name="getmetadataqueryreader"></a><span data-ttu-id="91541-128">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="91541-128">GetMetadataQueryReader</span></span>

<span data-ttu-id="91541-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) retourne un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) qu’une application peut utiliser pour récupérer des métadonnées à partir du frame d’image.</span><span class="sxs-lookup"><span data-stu-id="91541-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) returns an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) that an application can use to retrieve metadata from the image frame.</span></span> <span data-ttu-id="91541-130">Cette interface est implémentée par un gestionnaire de métadonnées et permet à une application d’interroger des propriétés de métadonnées spécifiques appartenant à un format de métadonnées particulier.</span><span class="sxs-lookup"><span data-stu-id="91541-130">This interface is implemented by a metadata handler, and allows an application to query for specific metadata properties belonging to a particular metadata format.</span></span> <span data-ttu-id="91541-131">Pour plus d’informations, consultez [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span><span class="sxs-lookup"><span data-stu-id="91541-131">For more information, see [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span></span>

<span data-ttu-id="91541-132">Pour instancier un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), appelez [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) sur [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span><span class="sxs-lookup"><span data-stu-id="91541-132">To instantiate an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), call [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) on the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span></span>


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a><span data-ttu-id="91541-133">Obtient, GetPixelFormat et GetResolution</span><span class="sxs-lookup"><span data-stu-id="91541-133">GetSize, GetPixelFormat, and GetResolution</span></span>

<span data-ttu-id="91541-134">[](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)Les requêtes, [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)et [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) sont explicites et retournent les propriétés demandées de l’image.</span><span class="sxs-lookup"><span data-stu-id="91541-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat), and [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) are self-explanatory, and return the requested properties of the image.</span></span>

### <a name="copypixels"></a><span data-ttu-id="91541-135">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="91541-135">CopyPixels</span></span>

<span data-ttu-id="91541-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) est la méthode qu’une application appelle lorsqu’elle souhaite créer une bitmap en mémoire qui peut être rendue sur l’écran ou l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="91541-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) is the method an application calls when it wants to create a bitmap in memory that can be rendered to the display or printer.</span></span> <span data-ttu-id="91541-137">Il s’agit de la méthode qui effectue le décodage réel des bits de l’image.</span><span class="sxs-lookup"><span data-stu-id="91541-137">This is the method that does the actual decoding of the image bits.</span></span> <span data-ttu-id="91541-138">Les paramètres sont un rectangle, qui représente la région d’intérêt de l’image source à copier en mémoire ; STRIDE, qui spécifie le nombre d’octets dans une ligne d’analyse ; taille de la mémoire tampon allouée par l’application ; et un pointeur vers la mémoire tampon dans laquelle les bits d’image demandés doivent être copiés.</span><span class="sxs-lookup"><span data-stu-id="91541-138">The parameters are a rectangle, which represents the region of interest in the source image to copy into memory; the stride, which specifies the number of bytes in one scan line; the size of the buffer in memory that has been allocated by the application; and a pointer to the buffer into which the requested image bits should be copied.</span></span> <span data-ttu-id="91541-139">(Pour empêcher les dépassements de mémoire tampon potentiels d’introduire des failles de sécurité, veillez à copier uniquement le nombre de données d’image dans la mémoire tampon en spécifiant le paramètre *cbBufferSize* .)</span><span class="sxs-lookup"><span data-stu-id="91541-139">(To prevent potential buffer overruns from introducing security vulnerabilities, be sure to copy only as much image data into the buffer as the *cbBufferSize* parameter specifies.)</span></span>

### <a name="copypalette"></a><span data-ttu-id="91541-140">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="91541-140">CopyPalette</span></span>

<span data-ttu-id="91541-141">Seuls les codecs ayant des formats de pixel indexés doivent implémenter la méthode [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="91541-141">Only codecs that have indexed pixel formats must implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span> <span data-ttu-id="91541-142">Si une image utilise un format indexé, utilisez cette méthode pour retourner la palette des couleurs utilisées dans l’image.</span><span class="sxs-lookup"><span data-stu-id="91541-142">If an image uses an indexed format, use this method to return the palette of colors used in the image.</span></span> <span data-ttu-id="91541-143">Si votre CODEC n’a pas de format indexé, retournez WINCODEC \_ Err \_ PALETTEUNAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="91541-143">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91541-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91541-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="91541-145">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="91541-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91541-146">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="91541-146">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="91541-147">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="91541-147">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="91541-148">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="91541-148">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="91541-149">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="91541-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="91541-150">Implémentation de IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="91541-150">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="91541-151">Implémentation de IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="91541-151">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="91541-152">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="91541-152">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="91541-153">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="91541-153">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



