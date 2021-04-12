---
description: Implémentation de IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implémentation de IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319850"
---
# <a name="implementing-iwicbitmapsourcetransform"></a><span data-ttu-id="1ee0e-103">Implémentation de IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="1ee0e-103">Implementing IWICBitmapSourceTransform</span></span>

## <a name="iwicbitmapsourcetransform"></a><span data-ttu-id="1ee0e-104">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="1ee0e-104">IWICBitmapSourceTransform</span></span>

<span data-ttu-id="1ee0e-105">Bien que facultatif, nous recommandons vivement que chaque décodeur implémente cette interface sur votre classe de décodage au niveau de la trame, car elle peut offrir des avantages majeurs en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-105">Though optional, we highly recommend that every decoder implement this interface on your frame-level decoding class, because it can provide major performance benefits.</span></span> <span data-ttu-id="1ee0e-106">Quand une application demande une région spécifique d’intérêt, de taille, d’orientation ou de format de pixel, au lieu de simplement décoder l’image entière à la résolution complète, puis d’appliquer les transformations demandées, le composant WIC [:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour cette interface sur l’objet [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="1ee0e-106">When an application requests a specific region of interest, size, orientation, or pixel format, instead of just decoding the whole image at full resolution and then applying the requested transforms, Windows Imaging Component (WIC) calls [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for this interface on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span> <span data-ttu-id="1ee0e-107">Si le décodeur de trame le prend en charge, WIC appelle la ou les méthodes appropriées pour déterminer si le décodeur de trame peut effectuer la transformation demandée ou déterminer la taille ou le format de pixel le plus proche que le décodeur peut fournir à celui qui a été demandé.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-107">If the frame decoder supports it, WIC calls the appropriate method or methods to determine whether the frame decoder can perform the requested transform or determine the closest size or pixel format the decoder can provide to the one requested.</span></span> <span data-ttu-id="1ee0e-108">Si le décodeur peut effectuer la transformation ou les transformations demandées, WIC appelle [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) avec les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-108">If the decoder can perform the requested transform or transforms, WIC invokes [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the appropriate parameters.</span></span> <span data-ttu-id="1ee0e-109">Si le décodeur peut effectuer des transformations, mais pas toutes les transformations demandées, WIC demande au décodeur d’effectuer les transformations nécessaires et utilise les objets de transformation WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)et [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) pour effectuer les transformations restantes qui n’ont pas pu être effectuées par le décodeur de trame **sur le résultat de l'**</span><span class="sxs-lookup"><span data-stu-id="1ee0e-109">If the decoder can perform some, but not all of the requested transforms, WIC asks the decoder to perform those that it can, and uses the WIC transform objects ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) to perform the remaining transforms that could not be performed by the frame decoder on the result of the **CopyPixels** call.</span></span> <span data-ttu-id="1ee0e-110">Si le décodeur ne prend pas en charge [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), WIC doit utiliser les objets Transform pour effectuer toutes les transformations.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-110">If the decoder doesn’t support [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), then WIC must use the transform objects to perform all of the transforms.</span></span> <span data-ttu-id="1ee0e-111">Il est généralement plus efficace pour le décodeur d’effectuer des transformations pendant le processus de décodage que de décoder l’image entière, puis d’effectuer les transformations.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-111">It’s usually much more efficient for the decoder to perform transforms during the decoding process than it is to decode the entire image and then perform the transforms.</span></span> <span data-ttu-id="1ee0e-112">Cela est particulièrement vrai pour les opérations telles que la mise à l’échelle vers une taille plus petite ou des conversions de format de pixel.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-112">This is especially true for operations such as scaling to a much smaller size or pixel format conversions.</span></span>


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [<span data-ttu-id="1ee0e-113">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="1ee0e-113">DoesSupportTransform</span></span>](#doessupporttransform)
-   [<span data-ttu-id="1ee0e-114">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="1ee0e-114">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="1ee0e-115">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="1ee0e-115">GetClosestSize</span></span>](#getclosestsize)
-   [<span data-ttu-id="1ee0e-116">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="1ee0e-116">GetClosestPixelFormat</span></span>](#getclosestpixelformat)

### <a name="doessupporttransform"></a><span data-ttu-id="1ee0e-117">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="1ee0e-117">DoesSupportTransform</span></span>

<span data-ttu-id="1ee0e-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) demande si le décodeur prend en charge l’opération de rotation ou de retournement demandée.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) asks whether the decoder supports the requested rotation or flipping operation.</span></span> <span data-ttu-id="1ee0e-119">Les [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) qui peuvent être demandés sont :</span><span class="sxs-lookup"><span data-stu-id="1ee0e-119">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) that may be requested are:</span></span>


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a><span data-ttu-id="1ee0e-120">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="1ee0e-120">CopyPixels</span></span>

<span data-ttu-id="1ee0e-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) effectue le travail réel de décodage des bits d’image, tel que la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sur l’interface [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , mais la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) sur [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) est beaucoup plus puissante et peut améliorer considérablement les performances de traitement des images.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) performs the actual work of decoding the image bits, such as the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, but the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method on [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) is much more powerful, and can improve image processing performance significantly.</span></span>

<span data-ttu-id="1ee0e-122">Lorsque plusieurs opérations de transformation sont demandées, le résultat est dépendant de l’ordre dans lequel les opérations sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-122">When multiple transform operations are requested, the result is dependent on the order in which the operations are performed.</span></span> <span data-ttu-id="1ee0e-123">Pour garantir la prévisibilité et la cohérence entre les codecs, il est important que tous les codecs effectuent ces opérations dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-123">To ensure predictability and consistency across codecs, it’s important that all codecs perform these operations in the same order.</span></span> <span data-ttu-id="1ee0e-124">Il s’agit de l’ordre canonique pour effectuer ces opérations.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-124">This is the canonical order for performing these operations.</span></span>

1.  <span data-ttu-id="1ee0e-125">Scale</span><span class="sxs-lookup"><span data-stu-id="1ee0e-125">Scale</span></span>
2.  <span data-ttu-id="1ee0e-126">Rogner</span><span class="sxs-lookup"><span data-stu-id="1ee0e-126">Crop</span></span>
3.  <span data-ttu-id="1ee0e-127">Faire pivoter</span><span class="sxs-lookup"><span data-stu-id="1ee0e-127">Rotate</span></span>

<span data-ttu-id="1ee0e-128">La conversion du format de Pixel peut être effectuée à tout moment, car elle n’a aucun effet sur les autres transformations.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-128">Pixel format conversion can be performed at any time, because it has no effect on the other transforms.</span></span>

<span data-ttu-id="1ee0e-129">Le premier paramètre, *prcSrc*, est utilisé pour spécifier la région d’intérêt pour le découpage de l’image.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-129">The first parameter, *prcSrc*, is used to specify the region of interest for clipping the image.</span></span> <span data-ttu-id="1ee0e-130">Étant donné que la mise à l’échelle est effectuée avant le découpage par Convention, si l’image doit être mise à l’échelle et découpée, la zone d’intérêt doit être déterminée une fois l’image mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-130">Because scaling is performed before clipping by convention, if the image is to be scaled as well as clipped, the region of interest should be determined after the image has been scaled.</span></span>

<span data-ttu-id="1ee0e-131">Le deuxième et le troisième paramètres indiquent la taille à laquelle la mise à l’échelle de l’image est mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-131">The second and third parameters indicate the size to which to scale the image.</span></span>

<span data-ttu-id="1ee0e-132">Le paramètre *pguidDstFormat* indique le format de pixel demandé pour l’image décodée.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-132">The *pguidDstFormat* parameter indicates the requested pixel format for the decoded image.</span></span> <span data-ttu-id="1ee0e-133">Dans la mesure où WIC a déjà appelé [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), il doit s’agir d’un format de pixel que le décodeur a indiqué qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-133">Because WIC has already called [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), this should be a pixel format that the decoder has indicated that it supports.</span></span>

<span data-ttu-id="1ee0e-134">Le paramètre *dstTransform* indique l’angle de rotation demandé et s’il faut retourner l’image verticalement, horizontalement ou les deux à la fois.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-134">The *dstTransform* parameter indicates the requested rotation angle, and whether to flip the image vertically, horizontally, or both.</span></span> <span data-ttu-id="1ee0e-135">Là encore, étant donné que WIC aura déjà appelé [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), la transformation demandée doit être celle que le décodeur a déjà indiqué qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-135">Again, because WIC will have already called [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), the requested transform should be one that the decoder has already indicated that it supports.</span></span> <span data-ttu-id="1ee0e-136">N’oubliez pas que la rotation doit toujours être effectuée après la mise à l’échelle et le découpage.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-136">Remember that rotation should always be performed after scaling and clipping.</span></span>

### <a name="getclosestsize"></a><span data-ttu-id="1ee0e-137">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="1ee0e-137">GetClosestSize</span></span>

<span data-ttu-id="1ee0e-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) accepte deux paramètres in/out.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) takes two in/out parameters.</span></span> <span data-ttu-id="1ee0e-139">L’appelant utilise les paramètres *puiWidth* et *puiHeight* pour spécifier la taille à laquelle l’appelant préfère le décodage de l’image.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-139">The caller uses the *puiWidth* and *puiHeight* parameters to specify the size at which that the caller prefers the image to be decoded.</span></span> <span data-ttu-id="1ee0e-140">Toutefois, un décodeur peut décoder une image uniquement en une taille qui est un multiple de sa taille DCT, et les différents formats d’image peuvent avoir des tailles DCT différentes.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-140">However, a decoder can decode an image only to a size that’s a multiple of its DCT size, and different image formats can have different DCT sizes.</span></span> <span data-ttu-id="1ee0e-141">Le décodeur doit déterminer, en fonction de sa propre taille DCT, le plus proche possible de la taille demandée, et définir les *puiWidth* et *puiHeight* sur ces dimensions au retour.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-141">The decoder should determine, based on its own DCT size, the closest it can come to the requested size, and set the *puiWidth* and *puiHeight* to those dimensions on return.</span></span> <span data-ttu-id="1ee0e-142">Si une taille supérieure est demandée, mais que le codec ne prend pas en charge la mise à l’échelle, le fichier d’origine doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-142">If a larger size is requested, but the codec doesn’t support upscaling, the original should be returned.</span></span>

### <a name="getclosestpixelformat"></a><span data-ttu-id="1ee0e-143">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="1ee0e-143">GetClosestPixelFormat</span></span>

<span data-ttu-id="1ee0e-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) est utilisé pour déterminer le format de pixel le plus proche du format de pixel demandé que le décodeur peut fournir sans perte de données.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) is used to determine the closest pixel format to the requested pixel format that the decoder can provide without loss of data.</span></span> <span data-ttu-id="1ee0e-145">Il est toujours préférable de passer à un format de pixel plus large que plus étroit, même s’il augmente la taille de l’image, car il peut toujours être reconverti en un format plus restrictif, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-145">It’s always preferable to convert to a wider pixel format than a narrower one, even though it will increase the size of the image, because it can always be reconverted to a more restrictive format if necessary.</span></span> <span data-ttu-id="1ee0e-146">Toutefois, une fois les données perdues, elles ne peuvent pas être récupérées.</span><span class="sxs-lookup"><span data-stu-id="1ee0e-146">However, after the data is lost, it can’t be recovered.</span></span>

## <a name="continued-reading"></a><span data-ttu-id="1ee0e-147">Lecture continue</span><span class="sxs-lookup"><span data-stu-id="1ee0e-147">Continued Reading</span></span>

<span data-ttu-id="1ee0e-148">Pour en savoir plus sur la création d’un codec avec WIC activé, consultez [implémentation de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span><span class="sxs-lookup"><span data-stu-id="1ee0e-148">To learn more about how to create a WIC-enabled codec, see [Implementing IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ee0e-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ee0e-149">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1ee0e-150">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="1ee0e-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1ee0e-151">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="1ee0e-151">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[<span data-ttu-id="1ee0e-152">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="1ee0e-152">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="1ee0e-153">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1ee0e-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1ee0e-154">Implémentation de IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="1ee0e-154">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="1ee0e-155">Implémentation de IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="1ee0e-155">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="1ee0e-156">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1ee0e-156">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="1ee0e-157">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="1ee0e-157">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
