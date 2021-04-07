---
description: Implémentation de IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implémentation de IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758301"
---
# <a name="implementing-iwicbitmapsource"></a><span data-ttu-id="bf873-103">Implémentation de IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="bf873-103">Implementing IWICBitmapSource</span></span>

## <a name="iwicbitmapsource"></a><span data-ttu-id="bf873-104">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="bf873-104">IWICBitmapSource</span></span>

<span data-ttu-id="bf873-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) est important pour l’utilisation d’images du point de vue d’une application.</span><span class="sxs-lookup"><span data-stu-id="bf873-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) is important for working with images from an application perspective.</span></span> <span data-ttu-id="bf873-106">Il représente l’abstraction de niveau le plus élevé pour une source d’image, et toutes les interfaces WIC (Windows Imaging Component) qui représentent une image, y compris [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)et toutes les interfaces de transformation ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)et [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) sont dérivées de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="bf873-106">It represents the highest level abstraction for an image source, and all Windows Imaging Component (WIC) interfaces that represent an image, including [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), and all the transform interfaces ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) are derived from it.</span></span> <span data-ttu-id="bf873-107">À un moment donné, un objet **IWICBitmapSource** peut ou non être sauvegardé par une image bitmap réelle en mémoire.</span><span class="sxs-lookup"><span data-stu-id="bf873-107">At any specific time, an **IWICBitmapSource** object may or may not be backed by an actual bitmap in memory.</span></span> <span data-ttu-id="bf873-108">Cela permet un traitement très efficace par une application, car une image peut être traitée comme une abstraction.</span><span class="sxs-lookup"><span data-stu-id="bf873-108">This enables very efficient processing by an application, because an image can be dealt with as an abstraction.</span></span> <span data-ttu-id="bf873-109">Les opérations de transformation peuvent être chaînées dans un pipeline de transformation sans consommer de ressources mémoire tant que l’application n’est pas prête à afficher ou à imprimer l’image, à ce moment-là, elle appelle la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sur la transformation finale pour obtenir une bitmap en mémoire de l’image avec les transformations sélectionnées appliquées.</span><span class="sxs-lookup"><span data-stu-id="bf873-109">Transform operations can be chained in a transform pipeline without consuming memory resources until the application is ready to render or print the image, at which time it invokes the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the final transform to get a bitmap in memory of the image with the selected transforms applied.</span></span>

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
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

<span data-ttu-id="bf873-110">Du point de vue du codec, les méthodes [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) sont implémentées sur l’objet décodeur de trame.</span><span class="sxs-lookup"><span data-stu-id="bf873-110">From a codec perspective, the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) methods are implemented on the frame decoder object.</span></span> <span data-ttu-id="bf873-111">Ces méthodes sont décrites dans implémentation de IWICBitmapSource, ainsi que les autres méthodes sur [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), dérivées de **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="bf873-111">These methods are described in Implementing IWICBitmapSource, along with the other methods on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), which is derived from **IWICBitmapSource**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf873-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf873-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bf873-113">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="bf873-113">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bf873-114">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="bf873-114">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="bf873-115">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="bf873-115">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="bf873-116">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="bf873-116">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="bf873-117">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="bf873-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bf873-118">Implémentation de IWICBitmapCodecProgressNotification (décodeur)</span><span class="sxs-lookup"><span data-stu-id="bf873-118">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="bf873-119">Implémentation de IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="bf873-119">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="bf873-120">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="bf873-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="bf873-121">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="bf873-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



