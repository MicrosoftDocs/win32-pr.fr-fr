---
description: Implémentation de IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implémentation de IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034583"
---
# <a name="implementing-iwicbitmapdecoder"></a><span data-ttu-id="29351-103">Implémentation de IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="29351-103">Implementing IWICBitmapDecoder</span></span>

## <a name="iwicbitmapdecoder"></a><span data-ttu-id="29351-104">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="29351-104">IWICBitmapDecoder</span></span>

<span data-ttu-id="29351-105">Quand une application demande un décodeur, le premier point d’interaction avec le codec se fait par le biais de l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="29351-105">When an application requests a decoder, the first point of interaction with the codec is through the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface.</span></span> <span data-ttu-id="29351-106">Il s’agit de l’interface au niveau du conteneur qui fournit l’accès aux propriétés de niveau supérieur du conteneur et, plus important encore, aux frames qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="29351-106">This is the container-level interface that provides access to the top-level properties of the container and, most importantly, the frames it contains.</span></span> <span data-ttu-id="29351-107">Il s’agit de l’interface principale sur votre classe de décodeur au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="29351-107">This is the primary interface on your container-level decoder class.</span></span>

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="29351-108">Certains formats d’image ont des miniatures globales, des contextes de couleur ou des métadonnées, tandis que de nombreux formats d’image les fournissent uniquement pour chaque image.</span><span class="sxs-lookup"><span data-stu-id="29351-108">Some image formats have global thumbnails, color contexts, or metadata, while many image formats provide these only on a per-frame basis.</span></span> <span data-ttu-id="29351-109">Les méthodes d’accès à ces éléments sont facultatives sur [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), mais elles sont requises sur [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="29351-109">The methods for accessing these items are optional on [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), but are required on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span> <span data-ttu-id="29351-110">De même, certains codecs n’utilisent pas les formats de pixel indexés et n’ont donc pas besoin d’implémenter les méthodes [CopyPalette](-wic-imp-iwicbitmapframedecode.md) sur l’une ou l’autre des interfaces.</span><span class="sxs-lookup"><span data-stu-id="29351-110">Likewise, some codecs do not use indexed pixel formats and so do not need to implement the [CopyPalette](-wic-imp-iwicbitmapframedecode.md) methods on either interface.</span></span> <span data-ttu-id="29351-111">Pour plus d’informations sur les méthodes **IWICBitmapDecoder** facultatives, consultez [implémentation de IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), où elles sont le plus souvent implémentées.</span><span class="sxs-lookup"><span data-stu-id="29351-111">For more information on the optional **IWICBitmapDecoder** methods, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), where they are most commonly implemented.</span></span>

### <a name="querycapability"></a><span data-ttu-id="29351-112">QueryCapability</span><span class="sxs-lookup"><span data-stu-id="29351-112">QueryCapability</span></span>

<span data-ttu-id="29351-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) est la méthode utilisée pour l’arbitrage du codec.</span><span class="sxs-lookup"><span data-stu-id="29351-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is the method used for codec arbitration.</span></span> <span data-ttu-id="29351-114">(Pour plus d’informations, consultez [découverte et arbitrage](-wic-howwicworks.md) dans la rubrique fonctionnement [du composant de création d’images Windows](-wic-howwicworks.md) ).</span><span class="sxs-lookup"><span data-stu-id="29351-114">(See [Discovery and Arbitration](-wic-howwicworks.md) in the [How The Windows Imaging Component Works](-wic-howwicworks.md) topic).</span></span> <span data-ttu-id="29351-115">Si deux codecs sont capables de décoder le même format d’image, ou si une collision de modèle se produit dans laquelle deux codecs utilisent le même modèle d’identification, cette méthode vous permet de sélectionner le codec qui peut gérer au mieux une image spécifique.</span><span class="sxs-lookup"><span data-stu-id="29351-115">If two codecs are capable of decoding the same image format, or if a pattern collision occurs in which two codecs use the same identifying pattern, this method allows you to select the codec that can best handle any specific image.</span></span>

<span data-ttu-id="29351-116">Lors de l’appel de cette méthode, le composant WIC (Windows Imaging Component) vous transmet le flux réel contenant l’image.</span><span class="sxs-lookup"><span data-stu-id="29351-116">When invoking this method, Windows Imaging Component (WIC) passes you the actual stream containing the image.</span></span> <span data-ttu-id="29351-117">Vous devez vérifier si vous pouvez décoder chaque frame dans l’image et énumérer les blocs de métadonnées, pour déclarer avec précision les fonctionnalités de ce décodeur par rapport au flux de fichier spécifique qui lui est passé.</span><span class="sxs-lookup"><span data-stu-id="29351-117">You must verify whether you can decode each frame within the image and enumerate through the metadata blocks, to accurately declare what capabilities this decoder has with respect to the specific file stream passed to it.</span></span> <span data-ttu-id="29351-118">Cela est important pour tous les décodeurs, mais particulièrement important pour les formats d’image basés sur des conteneurs TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="29351-118">This is important for all decoders, but particularly important for image formats based on Tagged Image File Format (TIFF) containers.</span></span> <span data-ttu-id="29351-119">Le processus de découverte fonctionne en faisant correspondre les modèles associés aux décodeurs dans le registre aux modèles dans le fichier image réel.</span><span class="sxs-lookup"><span data-stu-id="29351-119">The discovery process works by matching patterns associated with decoders in the registry to patterns in the actual image file.</span></span> <span data-ttu-id="29351-120">La déclaration de votre modèle d’identification dans le registre garantit que votre décodeur sera toujours détecté pour les images dans votre format d’image.</span><span class="sxs-lookup"><span data-stu-id="29351-120">Declaring your identifying pattern in the registry guarantees that your decoder will always be detected for images in your image format.</span></span> <span data-ttu-id="29351-121">Toutefois, votre décodeur peut toujours être détecté pour les images dans d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="29351-121">However, your decoder could still be detected for images in other formats.</span></span> <span data-ttu-id="29351-122">Par exemple, tous les conteneurs TIFF incluent le modèle TIFF, qui est un modèle d’identification valide pour le format d’image TIFF.</span><span class="sxs-lookup"><span data-stu-id="29351-122">For example, all TIFF containers include the TIFF pattern, which is a valid identifying pattern for the TIFF image format.</span></span> <span data-ttu-id="29351-123">Cela signifie que, pendant la découverte, au moins deux modèles d’identification se trouvent dans les fichiers image pour tout format d’image basé sur un conteneur de style TIFF.</span><span class="sxs-lookup"><span data-stu-id="29351-123">This means that, during discovery, at least two identifying patterns will be found in image files for any image format that’s based on a TIFF-style container.</span></span> <span data-ttu-id="29351-124">L’un est le modèle TIFF et l’autre est le modèle de format d’image réel.</span><span class="sxs-lookup"><span data-stu-id="29351-124">One will be the TIFF pattern and the other will be the actual image format pattern.</span></span> <span data-ttu-id="29351-125">Bien qu’il soit moins probable, il peut y avoir des collisions de modèles entre d’autres formats d’image non liés.</span><span class="sxs-lookup"><span data-stu-id="29351-125">While less likely, there could be pattern collisions between other unrelated image formats as well.</span></span> <span data-ttu-id="29351-126">C’est pourquoi la découverte et l’arbitrage sont un processus en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="29351-126">This is why discovery and arbitration is a two-stage process.</span></span> <span data-ttu-id="29351-127">Vérifiez toujours que le flux d’image transmis à [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) est en fait une instance valide de votre propre format d’image.</span><span class="sxs-lookup"><span data-stu-id="29351-127">Always verify that the image stream passed to [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is actually a valid instance of your own image format.</span></span> <span data-ttu-id="29351-128">En outre, si votre codec décode un format d’image pour lequel vous n’êtes pas propriétaire de la spécification, votre implémentation de **QueryCapability** doit vérifier la présence de toute fonctionnalité qui peut être valide sous la spécification de format d’image que votre CODEC n’implémente pas.</span><span class="sxs-lookup"><span data-stu-id="29351-128">Also, if your codec decodes an image format for which you don’t own the specification, your **QueryCapability** implementation should check for the presence of any feature that may be valid under the image format specification that your codec doesn’t implement.</span></span> <span data-ttu-id="29351-129">Cela permet de s’assurer que les utilisateurs ne subissent pas de décodage inutile ou obtiennent des résultats inattendus avec votre codec.</span><span class="sxs-lookup"><span data-stu-id="29351-129">This will ensure that users do not experience unnecessary decoding failures or get unexpected results with your codec.</span></span>

<span data-ttu-id="29351-130">Avant d’effectuer une opération sur l’image, vous devez enregistrer la position actuelle du flux afin de pouvoir la restaurer à sa position d’origine avant de retourner à partir de la méthode.</span><span class="sxs-lookup"><span data-stu-id="29351-130">Before performing any operation on the image, you must save the current position of the stream, so you can restore it to its original position before returning from the method.</span></span> <span data-ttu-id="29351-131">L’énumération [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) qui spécifie les fonctionnalités est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="29351-131">The [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) enumeration that specifies the capabilities is defined as follows:</span></span>

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

<span data-ttu-id="29351-132">Vous devez déclarer **WICBitmapDecoderCapabilitySameEncoder** uniquement si votre encodeur était celui qui encodé l’image.</span><span class="sxs-lookup"><span data-stu-id="29351-132">You should declare **WICBitmapDecoderCapabilitySameEncoder** only if your encoder was the one that encoded the image.</span></span> <span data-ttu-id="29351-133">Après avoir vérifié si vous pouvez décoder chaque frame dans le conteneur, déclarez **WICBitmapDecoderCapabilityCanDecodeSomeImages** si vous pouvez décoder certains des frames, mais pas tous, **WICBitmapDecoderCapabilityCanDecodeAllImages** si vous pouvez décoder tous les frames, ou si vous ne pouvez pas les décoder.</span><span class="sxs-lookup"><span data-stu-id="29351-133">After verifying whether you can decode each frame in the container, declare either **WICBitmapDecoderCapabilityCanDecodeSomeImages** if you can decode some but not all of the frames, **WICBitmapDecoderCapabilityCanDecodeAllImages** if you can decode all of the frames, or neither if you cannot decode any of them.</span></span> <span data-ttu-id="29351-134">(Ces deux énumérations s’excluent mutuellement ; si vous retournez **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** sera ignoré.) Déclarez **WICBitmapDecoderCapabilityCanEnumerateMetadata** après avoir vérifié que vous pouvez énumérer les blocs de métadonnées dans le conteneur d’images.</span><span class="sxs-lookup"><span data-stu-id="29351-134">(These two enums are mutually exclusive; if you return **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** will be ignored.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** after verifying that you can enumerate through the metadata blocks in the image container.</span></span> <span data-ttu-id="29351-135">Vous n’avez pas besoin de rechercher une miniature dans chaque cadre.</span><span class="sxs-lookup"><span data-stu-id="29351-135">You don’t have to check for a thumbnail in every frame.</span></span> <span data-ttu-id="29351-136">S’il existe une miniature globale et que vous pouvez la décoder, vous pouvez déclarer **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span><span class="sxs-lookup"><span data-stu-id="29351-136">If there is a global thumbnail and you can decode it, you can declare **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span></span> <span data-ttu-id="29351-137">S’il n’y a aucune miniature globale, essayez de décoder la miniature pour le frame 0.</span><span class="sxs-lookup"><span data-stu-id="29351-137">If there is no global thumbnail, then attempt to decode the thumbnail for Frame 0.</span></span> <span data-ttu-id="29351-138">S’il n’y a aucune miniature à l’un de ces emplacements, ne déclarez pas cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="29351-138">If there is no thumbnail in either of these places, do not declare this capability.</span></span>

<span data-ttu-id="29351-139">Après avoir déterminé les fonctionnalités du décodeur par rapport au flux d’image passé à cette méthode, effectuez une opération ou avec le [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) vous avez vérifié que ce décodeur peut effectuer sur cette image et retourner le résultat.</span><span class="sxs-lookup"><span data-stu-id="29351-139">After determining the capabilities of the decoder with respect to the image stream passed to this method, perform an OR operation with the [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) you have verified that this decoder can perform on this image, and return the result.</span></span> <span data-ttu-id="29351-140">N’oubliez pas de restaurer le flux à sa position d’origine avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="29351-140">Remember to restore the stream to its original position before returning.</span></span>

### <a name="initialize"></a><span data-ttu-id="29351-141">Initialiser</span><span class="sxs-lookup"><span data-stu-id="29351-141">Initialize</span></span>

<span data-ttu-id="29351-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) est appelé par une application après qu’un décodeur a été sélectionné pour décoder une image spécifique.</span><span class="sxs-lookup"><span data-stu-id="29351-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) is invoked by an application after a decoder has been selected to decode a specific image.</span></span> <span data-ttu-id="29351-143">Le flux d’image est passé au décodeur et un appelant peut éventuellement spécifier l’option de cache [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) pour gérer les métadonnées dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="29351-143">The image stream is passed to the decoder, and a caller may optionally specify the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) cache option for dealing with the metadata in the file.</span></span>

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

<span data-ttu-id="29351-144">Certaines applications utilisent les métadonnées plus que d’autres.</span><span class="sxs-lookup"><span data-stu-id="29351-144">Some applications use metadata more than others.</span></span> <span data-ttu-id="29351-145">La plupart des applications n’ont pas besoin d’accéder à toutes les métadonnées d’un fichier image et demandent des métadonnées spécifiques en fonction de leurs besoins.</span><span class="sxs-lookup"><span data-stu-id="29351-145">Most applications don’t need to access all the metadata in an image file, and will request specific metadata as they need it.</span></span> <span data-ttu-id="29351-146">D’autres applications préfèrent mettre en cache toutes les métadonnées en amont, de garder le flux de fichier ouvert et d’exécuter des e/s de disque chaque fois qu’ils ont besoin d’accéder aux métadonnées.</span><span class="sxs-lookup"><span data-stu-id="29351-146">Other applications would rather cache all the metadata up front than keep the file stream open and perform disk I/O every time they need to access metadata.</span></span> <span data-ttu-id="29351-147">Si l’appelant ne spécifie pas une option de cache des métadonnées, le comportement de mise en cache par défaut doit être cache à la demande.</span><span class="sxs-lookup"><span data-stu-id="29351-147">If the caller doesn’t specify a metadata cache option, the default caching behavior should be cache on demand.</span></span> <span data-ttu-id="29351-148">Cela signifie qu’aucune métadonnée ne doit être chargée en mémoire tant que l’application n’a pas effectué une demande spécifique pour ces métadonnées.</span><span class="sxs-lookup"><span data-stu-id="29351-148">This means no metadata should be loaded into memory until the application makes a specific request for that metadata.</span></span> <span data-ttu-id="29351-149">Si l’application spécifie **WICDecodeMetadataCacheOnLoad**, les métadonnées doivent être chargées en mémoire immédiatement et mises en cache.</span><span class="sxs-lookup"><span data-stu-id="29351-149">If the application specifies **WICDecodeMetadataCacheOnLoad**, the metadata should be loaded in memory immediately and cached.</span></span> <span data-ttu-id="29351-150">Lorsque les métadonnées sont mises en cache lors du chargement, le flux de fichier peut être libéré une fois que les métadonnées ont été mises en cache.</span><span class="sxs-lookup"><span data-stu-id="29351-150">When metadata is cached on load, the file stream may be released after the metadata has been cached.</span></span>

### <a name="getcontainerformat"></a><span data-ttu-id="29351-151">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="29351-151">GetContainerFormat</span></span>

<span data-ttu-id="29351-152">Pour implémenter [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), il suffit de retourner le GUID du format d’image de l’image pour laquelle le décodeur est instancié.</span><span class="sxs-lookup"><span data-stu-id="29351-152">To implement [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), just return the GUID of the image format of the image for which the decoder is instantiated.</span></span> <span data-ttu-id="29351-153">Cette méthode est également implémentée sur [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) et [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="29351-153">This method is also implemented on [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span>

### <a name="getdecoderinfo"></a><span data-ttu-id="29351-154">GetDecoderInfo</span><span class="sxs-lookup"><span data-stu-id="29351-154">GetDecoderInfo</span></span>

<span data-ttu-id="29351-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) retourne un objet [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="29351-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) returns an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) object.</span></span> <span data-ttu-id="29351-156">Pour obtenir l’objet **IWICBitmapDecoderInfo** , il vous suffit de transmettre le GUID de votre décodeur à la méthode [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) sur [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), puis de demander l’interface **IWICBitmapDecoderInfo** sur ce dernier, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="29351-156">To get the **IWICBitmapDecoderInfo** object, just pass the GUID of your decoder to the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method on [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), and then request the **IWICBitmapDecoderInfo** interface on it, as shown in the following example.</span></span>


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a><span data-ttu-id="29351-157">GetFrameCount</span><span class="sxs-lookup"><span data-stu-id="29351-157">GetFrameCount</span></span>

<span data-ttu-id="29351-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) retourne simplement le nombre de frames dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="29351-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) just returns the number of frames in the container.</span></span> <span data-ttu-id="29351-159">Certains formats de conteneur prennent en charge plusieurs frames, tandis que d’autres ne prennent en charge qu’une seule trame par conteneur.</span><span class="sxs-lookup"><span data-stu-id="29351-159">Some container formats support multiple frames, and others support only one frame per container.</span></span>

### <a name="getframe"></a><span data-ttu-id="29351-160">GetFrame</span><span class="sxs-lookup"><span data-stu-id="29351-160">GetFrame</span></span>

<span data-ttu-id="29351-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) est une méthode importante sur l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) , car le frame contient les bits d’image réels, et l’objet décodeur de trame retourné par cette méthode est l’objet qui effectue le décodage réel de l’image demandée.</span><span class="sxs-lookup"><span data-stu-id="29351-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) is an important method on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface because the frame contains the actual image bits, and the frame decoder object returned from this method is the object that does the actual decoding of the requested image.</span></span> <span data-ttu-id="29351-162">Il s’agit de l’autre objet que vous devez implémenter lors de l’écriture d’un décodeur.</span><span class="sxs-lookup"><span data-stu-id="29351-162">That is the other object you need to implement when writing a decoder.</span></span> <span data-ttu-id="29351-163">Pour plus d’informations sur les décodeurs de frame, consultez [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span><span class="sxs-lookup"><span data-stu-id="29351-163">For more information on frame decoders, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span></span>

### <a name="getpreview"></a><span data-ttu-id="29351-164">GetPreview</span><span class="sxs-lookup"><span data-stu-id="29351-164">GetPreview</span></span>

<span data-ttu-id="29351-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) retourne un aperçu de l’image.</span><span class="sxs-lookup"><span data-stu-id="29351-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) returns a preview of the image.</span></span> <span data-ttu-id="29351-166">Pour obtenir une présentation détaillée des préversions, consultez la méthode [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) sur l’interface [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) .</span><span class="sxs-lookup"><span data-stu-id="29351-166">For a detailed discussion of previews, see the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) method on the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) interface.</span></span>

<span data-ttu-id="29351-167">Si votre format d’image contient une préversion JPEG incorporée, il est fortement recommandé, au lieu d’écrire un décodeur JPEG pour le décoder, de déléguer le décodeur JPEG fourni avec la plateforme WIC pour le décodage des aperçus et des miniatures.</span><span class="sxs-lookup"><span data-stu-id="29351-167">If your image format contains an embedded JPEG preview, it is strongly recommend that, instead of writing a JPEG decoder to decode it, you delegate to the JPEG decoder that ships with the WIC platform for decoding previews and thumbnails.</span></span> <span data-ttu-id="29351-168">Pour ce faire, recherchez le début des données de l’image d’aperçu dans le flux et appelez la méthode [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) sur [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="29351-168">To do this, seek to the beginning of the preview image data in the stream and invoke the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method on the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a><span data-ttu-id="29351-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29351-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="29351-170">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="29351-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29351-171">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="29351-171">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="29351-172">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="29351-172">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="29351-173">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="29351-173">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29351-174">Interfaces de décodeur</span><span class="sxs-lookup"><span data-stu-id="29351-174">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="29351-175">Implémentation de IWICBitmapCodecProgressNotification (décodeur)</span><span class="sxs-lookup"><span data-stu-id="29351-175">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="29351-176">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="29351-176">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="29351-177">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="29351-177">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



