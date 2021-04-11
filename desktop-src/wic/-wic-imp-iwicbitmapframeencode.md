---
description: Implémentation de IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implémentation de IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204222"
---
# <a name="implementing-iwicbitmapframeencode"></a><span data-ttu-id="36a97-103">Implémentation de IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="36a97-103">Implementing IWICBitmapFrameEncode</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="36a97-104">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="36a97-104">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="36a97-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) est l’équivalent de l’encodeur à l’interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="36a97-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the encoder’s counterpart to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span> <span data-ttu-id="36a97-106">Vous pouvez implémenter cette interface sur votre classe de codage au niveau de la trame, qui est la classe qui effectue l’encodage réel des bits d’image pour chaque frame.</span><span class="sxs-lookup"><span data-stu-id="36a97-106">You can implement this interface on your frame-level encoding class, which is the class that does the actual encoding of the image bits for each frame.</span></span>


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [<span data-ttu-id="36a97-107">Initialiser</span><span class="sxs-lookup"><span data-stu-id="36a97-107">Initialize</span></span>](#initialize)
-   [<span data-ttu-id="36a97-108">Définit et SetResolution</span><span class="sxs-lookup"><span data-stu-id="36a97-108">SetSize and SetResolution</span></span>](#setsize-and-setresolution)
-   [<span data-ttu-id="36a97-109">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="36a97-109">SetPixelFormat</span></span>](#setpixelformat)
-   [<span data-ttu-id="36a97-110">SetColorContexts</span><span class="sxs-lookup"><span data-stu-id="36a97-110">SetColorContexts</span></span>](#setcolorcontexts)
-   [<span data-ttu-id="36a97-111">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="36a97-111">GetMetadataQueryWriter</span></span>](#getmetadataquerywriter)
-   [<span data-ttu-id="36a97-112">SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="36a97-112">SetThumbnail</span></span>](#setthumbnail)
-   [<span data-ttu-id="36a97-113">WritePixels</span><span class="sxs-lookup"><span data-stu-id="36a97-113">WritePixels</span></span>](#writepixels)
-   [<span data-ttu-id="36a97-114">WriteSource</span><span class="sxs-lookup"><span data-stu-id="36a97-114">WriteSource</span></span>](#writesource)
-   [<span data-ttu-id="36a97-115">Commiter</span><span class="sxs-lookup"><span data-stu-id="36a97-115">Commit</span></span>](#commit)
-   [<span data-ttu-id="36a97-116">SetPalette</span><span class="sxs-lookup"><span data-stu-id="36a97-116">SetPalette</span></span>](#setpalette)

### <a name="initialize"></a><span data-ttu-id="36a97-117">Initialiser</span><span class="sxs-lookup"><span data-stu-id="36a97-117">Initialize</span></span>

<span data-ttu-id="36a97-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) est la première méthode appelée sur un objet [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) une fois qu’elle a été instanciée.</span><span class="sxs-lookup"><span data-stu-id="36a97-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) is the first method invoked on an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object after it has been instantiated.</span></span> <span data-ttu-id="36a97-119">Cette méthode a un paramètre, qui peut être défini sur **null**.</span><span class="sxs-lookup"><span data-stu-id="36a97-119">This method has one parameter, which may be set to **NULL**.</span></span> <span data-ttu-id="36a97-120">Ce paramètre représente les options de l’encodeur. il s’agit de la même instance [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que vous avez créée dans la méthode [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) sur le décodeur au niveau du conteneur, puis repassée à l’appelant dans le paramètre pIEncoderOptions de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="36a97-120">This parameter represents the encoder options, and is the same [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) instance that you created in the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method on the container-level decoder, and passed back to the caller in the pIEncoderOptions parameter of that method.</span></span> <span data-ttu-id="36a97-121">À ce moment-là, vous avez rempli le struct IPropertyBag2 avec des propriétés qui représentent les options d’encodage prises en charge par votre encodeur au niveau de la trame.</span><span class="sxs-lookup"><span data-stu-id="36a97-121">At that time, you populated the IPropertyBag2 struct with properties that represent the encoding options supported by your frame-level encoder.</span></span> <span data-ttu-id="36a97-122">L’appelant a maintenant fourni des valeurs pour ces propriétés afin d’indiquer certains paramètres d’option d’encodage et renvoie le même objet pour initialiser l’objet **IWICBitmapFrameEncode** .</span><span class="sxs-lookup"><span data-stu-id="36a97-122">The caller has now provided values for those properties to indicate certain encoding option parameters, and is passing the same object back to you to initialize the **IWICBitmapFrameEncode** object.</span></span> <span data-ttu-id="36a97-123">Vous devez appliquer les options spécifiées lors de l’encodage des bits de l’image.</span><span class="sxs-lookup"><span data-stu-id="36a97-123">You should apply the specified options when encoding the image bits.</span></span>

### <a name="setsize-and-setresolution"></a><span data-ttu-id="36a97-124">Définit et SetResolution</span><span class="sxs-lookup"><span data-stu-id="36a97-124">SetSize and SetResolution</span></span>

<span data-ttu-id="36a97-125">Les paramètres de la [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) et de la [**configuration**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) sont explicites.</span><span class="sxs-lookup"><span data-stu-id="36a97-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) and [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) are self-explanatory.</span></span> <span data-ttu-id="36a97-126">L’appelant utilise ces méthodes pour spécifier la taille et la résolution de l’image encodée.</span><span class="sxs-lookup"><span data-stu-id="36a97-126">The caller uses these methods to specify the size and resolution for the encoded image.</span></span>

### <a name="setpixelformat"></a><span data-ttu-id="36a97-127">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="36a97-127">SetPixelFormat</span></span>

<span data-ttu-id="36a97-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) est utilisé pour demander un format de pixel dans lequel encoder l’image.</span><span class="sxs-lookup"><span data-stu-id="36a97-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) is used to request a pixel format in which to encode the image.</span></span> <span data-ttu-id="36a97-129">Si le format de pixel demandé n’est pas pris en charge, vous devez retourner le GUID du format de pixel le plus proche qui est pris en charge dans *pPixelFormat*, qui est un paramètre in/out.</span><span class="sxs-lookup"><span data-stu-id="36a97-129">If the requested pixel format is not supported, you should return the GUID of the closest pixel format that is supported in *pPixelFormat*, which is an in/out parameter.</span></span>

### <a name="setcolorcontexts"></a><span data-ttu-id="36a97-130">SetColorContexts</span><span class="sxs-lookup"><span data-stu-id="36a97-130">SetColorContexts</span></span>

<span data-ttu-id="36a97-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) est utilisé pour spécifier un ou plusieurs contextes de couleur valides (également appelés profils de couleurs) pour cette image.</span><span class="sxs-lookup"><span data-stu-id="36a97-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) is used to specify one or more valid color contexts (also known as color profiles) for this image.</span></span> <span data-ttu-id="36a97-132">Il est important de spécifier les contextes de couleur. par conséquent, une application qui décode l’image ultérieurement peut convertir le profil de couleurs source en profil de destination de l’appareil utilisé pour afficher ou imprimer l’image.</span><span class="sxs-lookup"><span data-stu-id="36a97-132">It’s important to specify the color contexts, so an application that decodes the image at a later time can convert from the source color profile to the destination profile of the device being used to display or print the image.</span></span> <span data-ttu-id="36a97-133">Sans profil de couleurs, il n’est pas possible d’obtenir des couleurs cohérentes sur différents appareils.</span><span class="sxs-lookup"><span data-stu-id="36a97-133">Without a color profile, it is not possible to get consistent colors across different devices.</span></span> <span data-ttu-id="36a97-134">Cela peut être frustrant pour les utilisateurs finaux lorsque leurs photos semblent différentes sur des moniteurs différents et qu’ils ne peuvent pas obtenir les impressions correspondant à ce qu’elles voient à l’écran.</span><span class="sxs-lookup"><span data-stu-id="36a97-134">This can be frustrating for end users when their photos look different on different monitors, and they can’t get the prints to match what they see on screen.</span></span>

### <a name="getmetadataquerywriter"></a><span data-ttu-id="36a97-135">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="36a97-135">GetMetadataQueryWriter</span></span>

<span data-ttu-id="36a97-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) retourne un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) qu’une application peut utiliser pour insérer ou modifier des propriétés de métadonnées spécifiques dans un bloc de métadonnées sur le frame d’image.</span><span class="sxs-lookup"><span data-stu-id="36a97-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) returns an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) that an application can use to insert or edit specific metadata properties in a metadata block on the image frame.</span></span>

<span data-ttu-id="36a97-137">Vous pouvez instancier un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) à partir du [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="36a97-137">You can instantiate an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) from the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in several ways.</span></span> <span data-ttu-id="36a97-138">Vous pouvez le créer à partir de votre [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), de la même façon que [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) a été créé à partir d’un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) dans la méthode [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) sur l’interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="36a97-138">You can either create it from your [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), the same way [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) was created from an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span>


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



<span data-ttu-id="36a97-139">Vous pouvez également le créer à partir d’un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)existant, tel que celui obtenu à l’aide de la méthode précédente.</span><span class="sxs-lookup"><span data-stu-id="36a97-139">You can also create it from an existing [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), such as the one obtained using the previous method.</span></span>


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



<span data-ttu-id="36a97-140">Le paramètre *pGuidVendor* vous permet de spécifier un fournisseur particulier à utiliser par le générateur de requêtes lors de l’instanciation d’un enregistreur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="36a97-140">The *pguidVendor* parameter allows you to specify a particular vendor for the query writer to use when instantiating a metadata writer.</span></span> <span data-ttu-id="36a97-141">Par exemple, si vous fournissez vos propres enregistreurs de métadonnées, vous souhaiterez peut-être spécifier votre propre GUID de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="36a97-141">For example, if you provide your own metadata writers, you may want to specify your own vendor GUID.</span></span> <span data-ttu-id="36a97-142">Si vous n’avez pas de préférence, vous pouvez passer la **valeur null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="36a97-142">You can pass **NULL** to this parameter if you don’t have a preference.</span></span>

### <a name="setthumbnail"></a><span data-ttu-id="36a97-143">SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="36a97-143">SetThumbnail</span></span>

<span data-ttu-id="36a97-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) est utilisé pour fournir une miniature.</span><span class="sxs-lookup"><span data-stu-id="36a97-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is used to provide a thumbnail.</span></span> <span data-ttu-id="36a97-145">Toutes les images doivent fournir une miniature à l’échelle mondiale, sur chaque image, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="36a97-145">All images should provide a thumbnail either globally, on each frame, or both.</span></span> <span data-ttu-id="36a97-146">Les méthodes **miniature** et **SetThumbnail** sont facultatives au niveau du conteneur, mais si un codec retourne WINCODEC \_ Err \_ CODECNOTHUMBNAIL de la méthode [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) , Windows Imaging Component (WIC) appellera la méthode [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) pour le frame 0.</span><span class="sxs-lookup"><span data-stu-id="36a97-146">The **GetThumbnail** and **SetThumbnail** methods are optional at the container-level but, if a codec returns WINCODEC\_ERR\_CODECNOTHUMBNAIL from the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method, Windows Imaging Component (WIC) will invoke the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method for Frame 0.</span></span> <span data-ttu-id="36a97-147">Si aucune miniature n’est trouvée à l’un ou l’autre emplacement, WIC doit décoder l’image complète et l’adapter à la taille de la miniature, ce qui peut entraîner une baisse importante des performances pour les images de grande taille.</span><span class="sxs-lookup"><span data-stu-id="36a97-147">If no thumbnail is found in either place, WIC must decode the full image and scale it to thumbnail size, which could incur a large performance penalty for larger images.</span></span>

<span data-ttu-id="36a97-148">La miniature doit avoir une taille et une résolution qui accélèrent le décodage et l’affichage.</span><span class="sxs-lookup"><span data-stu-id="36a97-148">The thumbnail should be of a size and resolution that makes it quick to decode and display.</span></span> <span data-ttu-id="36a97-149">Pour cette raison, les miniatures sont généralement des images JPEG.</span><span class="sxs-lookup"><span data-stu-id="36a97-149">For this reason, thumbnails are most commonly JPEG images.</span></span> <span data-ttu-id="36a97-150">Notez que, si vous utilisez JPEG pour vos miniatures, vous n’êtes pas obligé d’écrire un encodeur JPEG pour les encoder ou un décodeur JPEG pour les décoder.</span><span class="sxs-lookup"><span data-stu-id="36a97-150">Note that, if you use JPEG for your thumbnails, you don’t have to write a JPEG encoder to encode them, or a JPEG decoder to decode them.</span></span> <span data-ttu-id="36a97-151">Vous devez toujours déléguer au codec JPEG fourni avec la plateforme WIC pour l’encodage et le décodage des miniatures.</span><span class="sxs-lookup"><span data-stu-id="36a97-151">You should always delegate to the JPEG codec that ships with the WIC platform for encoding and decoding thumbnails.</span></span>

### <a name="writepixels"></a><span data-ttu-id="36a97-152">WritePixels</span><span class="sxs-lookup"><span data-stu-id="36a97-152">WritePixels</span></span>

<span data-ttu-id="36a97-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) est la méthode utilisée pour transmettre des lignes d’analyse à partir d’une bitmap en mémoire pour l’encodage.</span><span class="sxs-lookup"><span data-stu-id="36a97-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) is the method used to pass in scan lines from a bitmap in memory for encoding.</span></span> <span data-ttu-id="36a97-154">La méthode est appelée à plusieurs reprises jusqu’à ce que toutes les lignes de numérisation aient été passées.</span><span class="sxs-lookup"><span data-stu-id="36a97-154">The method will be called repeatedly until all of the scan lines have been passed in.</span></span> <span data-ttu-id="36a97-155">Le paramètre *lineCount* indique le nombre de lignes de numérisation à écrire dans cet appel.</span><span class="sxs-lookup"><span data-stu-id="36a97-155">The *lineCount* parameter indicates how many scan lines are to be written in this call.</span></span> <span data-ttu-id="36a97-156">Le paramètre *cbStride* indique le nombre d’octets par ligne d’analyse.</span><span class="sxs-lookup"><span data-stu-id="36a97-156">The *cbStride* parameter indicates the number of bytes per scan line.</span></span> <span data-ttu-id="36a97-157">*cbBufferSize* indique la taille de la mémoire tampon passée dans le paramètre pbPixels, qui contient les bits d’image réels à encoder.</span><span class="sxs-lookup"><span data-stu-id="36a97-157">*cbBufferSize* indicates the size of the buffer passed in the pbPixels parameter, which contains the actual image bits to be encoded.</span></span> <span data-ttu-id="36a97-158">Si la hauteur combinée des lignes d’analyse des appels cumulatifs est supérieure à la hauteur spécifiée dans la méthode de la méthode de [**configuration**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , retournez WINCODEC \_ Err \_ TOOMANYSCANLINES.</span><span class="sxs-lookup"><span data-stu-id="36a97-158">If the combined height of the scan lines from cumulative calls is greater than the height specified in [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="36a97-159">Lorsque le [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) est **WICBitmapEncoderCacheInMemory**, les lignes de numérisation doivent être mises en cache dans la mémoire jusqu’à ce que toutes les lignes de numérisation aient été transmises.</span><span class="sxs-lookup"><span data-stu-id="36a97-159">When the [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) is **WICBitmapEncoderCacheInMemory**, the scan lines should be cached in memory until all scan lines have been passed in.</span></span> <span data-ttu-id="36a97-160">Si l’option de mise en cache de l’encodeur est **WICBitmapEncoderCacheTempFile**, les lignes d’analyse doivent être mises en cache dans un fichier temporaire, créé lors de l’initialisation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="36a97-160">If the encoder cache option is **WICBitmapEncoderCacheTempFile**, the scan lines should be cached in a temporary file, created when initializing the object.</span></span> <span data-ttu-id="36a97-161">Dans l’un ou l’autre de ces cas, l’image ne doit pas être encodée tant que l’appelant n’appelle pas [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span><span class="sxs-lookup"><span data-stu-id="36a97-161">In either of these cases, the image should not be encoded until the caller calls [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span></span> <span data-ttu-id="36a97-162">Dans le cas où l’option de cache est **WICBitmapEncoderNoCache**, l’encodeur doit encoder les lignes d’analyse à mesure qu’elles sont reçues, si possible.</span><span class="sxs-lookup"><span data-stu-id="36a97-162">In the case where the cache option is **WICBitmapEncoderNoCache**, the encoder should encode the scan lines as they’re received, if possible.</span></span> <span data-ttu-id="36a97-163">(Dans certains formats, cela n’est pas possible et les lignes d’analyse doivent être mises en cache jusqu’à ce que la validation soit appelée.)</span><span class="sxs-lookup"><span data-stu-id="36a97-163">(In some formats, this is not possible, and the scan lines must be cached until Commit is called.)</span></span>

<span data-ttu-id="36a97-164">La plupart des codecs bruts n’implémenteront pas [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), car ils ne prennent pas en charge la modification des bits d’image dans le fichier brut.</span><span class="sxs-lookup"><span data-stu-id="36a97-164">Most raw codecs will not implement [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), because they don’t support altering the image bits in the raw file.</span></span> <span data-ttu-id="36a97-165">Toutefois, les codecs bruts doivent toujours implémenter **WritePixels**, car lorsque les métadonnées sont ajoutées, il peut augmenter la taille du fichier, ce qui nécessite la réécriture du fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="36a97-165">Raw codecs should still implement **WritePixels**, however, because when metadata is added, it may increase the size of the file, requiring the file to be rewritten on the disk.</span></span> <span data-ttu-id="36a97-166">Dans ce cas, il est nécessaire de pouvoir copier les bits d’image existants, ce que fait la méthode **WritePixels** .</span><span class="sxs-lookup"><span data-stu-id="36a97-166">In that case, it’s necessary to be able to copy the existing image bits, which is what the **WritePixels** method does.</span></span>

### <a name="writesource"></a><span data-ttu-id="36a97-167">WriteSource</span><span class="sxs-lookup"><span data-stu-id="36a97-167">WriteSource</span></span>

<span data-ttu-id="36a97-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) est utilisé pour encoder un objet [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="36a97-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) is used to encode an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span> <span data-ttu-id="36a97-169">Le premier paramètre est un pointeur vers un objet **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="36a97-169">The first parameter is a pointer to an **IWICBitmapSource** object.</span></span> <span data-ttu-id="36a97-170">Le deuxième paramètre est un WICRect qui spécifie la région d’intérêt à encoder.</span><span class="sxs-lookup"><span data-stu-id="36a97-170">The second parameter is a WICRect that specifies the region of interest to encode.</span></span> <span data-ttu-id="36a97-171">Cette méthode peut être appelée plusieurs fois successivement, à condition que la largeur de chaque rectangle soit la même que celle de l’image finale à encoder.</span><span class="sxs-lookup"><span data-stu-id="36a97-171">This method may be called multiple times in succession, as long as the width of each rectangle is the same width of the final image to be encoded.</span></span> <span data-ttu-id="36a97-172">Si la largeur du rectangle passé dans le paramètre PRC est différente de la largeur spécifiée dans la méthode deinstall, retournez WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS.</span><span class="sxs-lookup"><span data-stu-id="36a97-172">If the width of the rectangle passed in the prc parameter is different than the width specified in the SetSize method, return WINCODEC\_ERR\_SOURCERECTDOESNOTMATCHDIMENSIONS.</span></span> <span data-ttu-id="36a97-173">Si la hauteur combinée des lignes d’analyse des appels cumulatifs est supérieure à la hauteur spécifiée dans la méthode de la méthode de configuration, retournez WINCODEC \_ Err \_ TOOMANYSCANLINES.</span><span class="sxs-lookup"><span data-stu-id="36a97-173">If the combined height of the scan lines from cumulative calls is greater than the height specified in SetSize method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="36a97-174">Les options de cache fonctionnent de la même manière avec cette méthode qu’avec la méthode [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) décrite précédemment.</span><span class="sxs-lookup"><span data-stu-id="36a97-174">The cache options work the same way with this method as with the [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) method described previously.</span></span>

### <a name="commit"></a><span data-ttu-id="36a97-175">Commit</span><span class="sxs-lookup"><span data-stu-id="36a97-175">Commit</span></span>

<span data-ttu-id="36a97-176">La [**validation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) est la méthode qui sérialise les bits d’image encodés dans le flux de fichier et itère au sein de tous les enregistreurs de métadonnées pour le frame qui les demande de sérialiser leurs métadonnées dans le flux.</span><span class="sxs-lookup"><span data-stu-id="36a97-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) is the method that serializes the encoded image bits to the file stream, and iterates through all the metadata writers for the frame requesting them to serialize their metadata to the stream.</span></span> <span data-ttu-id="36a97-177">Dans le cas où l’option de cache d’encodeur est WICBitmapEncoderCacheInMemory ou WICBitmapEncoderCacheTempFile, cette méthode est également responsable de l’encodage de l’image, et lorsque l’option de cache est WICBitmapEncoderCacheTempFile, la méthode de **validation** doit également supprimer le fichier temporaire utilisé pour mettre en cache les données d’image avant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="36a97-177">In the case where the encoder cache option is WICBitmapEncoderCacheInMemory or WICBitmapEncoderCacheTempFile, this method is also responsible for encoding the image, and when the cache option is WICBitmapEncoderCacheTempFile, the **Commit** method should also delete the temporary file used to cache the image data before encoding.</span></span>

<span data-ttu-id="36a97-178">Cette méthode est toujours appelée une fois que toutes les lignes de numérisation ou les rectangles qui composent l’image ont été transmis à l’aide de la méthode [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) ou [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="36a97-178">This method is always invoked after all the scan lines or rectangles that make up the image have been passed in using either the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) or [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span> <span data-ttu-id="36a97-179">La taille du rectangle final qui est composé par les appels accumulés à WritePixels ou WriteSource doit être de la même taille que celle spécifiée dans la méthode de configuration.</span><span class="sxs-lookup"><span data-stu-id="36a97-179">The size of the final rectangle that is composed through the accumulated calls to WritePixels or WriteSource must be the same size as was specified in the SetSize method.</span></span> <span data-ttu-id="36a97-180">Si la taille ne correspond pas à la taille attendue, cette méthode doit retourner WINCODECERROR \_ UNEXPECTEDSIZE.</span><span class="sxs-lookup"><span data-stu-id="36a97-180">If the size does not match the expected size, this method should return WINCODECERROR\_UNEXPECTEDSIZE.</span></span>

<span data-ttu-id="36a97-181">Pour itérer au sein des enregistreurs de métadonnées et indiquer à chaque enregistreur de métadonnées de sérialiser les métadonnées, accédez au flux, appelez GetWriterByIndex pour itérer au sein des enregistreurs de chaque bloc, puis appelez IWICPersistStream. Save sur chaque enregistreur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="36a97-181">To iterate through the metadata writers and tell each metadata writer to serialize its metadata go the stream, invoke GetWriterByIndex to iterate through the writers for each block, and invoke IWICPersistStream.Save on each metadata writer.</span></span>


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a><span data-ttu-id="36a97-182">SetPalette</span><span class="sxs-lookup"><span data-stu-id="36a97-182">SetPalette</span></span>

<span data-ttu-id="36a97-183">Seuls les codecs ayant des formats indexés doivent implémenter la méthode [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="36a97-183">Only codecs that have indexed formats need to implement the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) method.</span></span> <span data-ttu-id="36a97-184">Si une image utilise un format indexé, utilisez cette méthode pour spécifier la palette des couleurs utilisées dans l’image.</span><span class="sxs-lookup"><span data-stu-id="36a97-184">If an image uses an indexed format, use this method to specify the palette of colors used in the image.</span></span> <span data-ttu-id="36a97-185">Si votre CODEC n’a pas de format indexé, retournez WINCODEC \_ Err \_ PALETTEUNAVAILABLE à partir de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="36a97-185">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE from this method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36a97-186">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36a97-186">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="36a97-187">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="36a97-187">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="36a97-188">Implémentation de IWICBitmapCodecProgressNotification (encodeur)</span><span class="sxs-lookup"><span data-stu-id="36a97-188">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[<span data-ttu-id="36a97-189">Implémentation de IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="36a97-189">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="36a97-190">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="36a97-190">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="36a97-191">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="36a97-191">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
