---
description: Implémentation de IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implémentation de IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b49e3636f5d81202b1060d868ecb40bb99d095dd9f26b6afd0d40c5f5fd0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205763"
---
# <a name="implementing-iwicbitmapframedecode"></a>Implémentation de IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) est l’interface au niveau de la trame qui fournit l’accès aux bits d’image réels. Vous implémentez cette interface sur votre classe de décodage au niveau de la trame. Comme elle est dérivée de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), votre implémentation de **IWICBitmapFrameDecode** inclura une implémentation des méthodes **IWICBitmapSource** . Les méthodes supplémentaires sur **IWICBitmapFrameDecode** permettent d’accéder à la miniature au niveau de la trame, à tous les contextes de couleur de l’image et au lecteur de requêtes de métadonnées pour le frame.

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

-   [GetThumbnail](#getthumbnail)
-   [GetColorContexts](#getcolorcontexts)
-   [GetMetadataQueryReader](#getmetadataqueryreader)
-   [Obtient, GetPixelFormat et GetResolution](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**Miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) retourne la miniature du frame actuel. Pour des raisons de performances, les miniatures sont généralement encodées au format JPEG. Tout comme avec l’aperçu sur le décodeur, il n’est pas nécessaire ou recommandé de fournir votre propre décodeur JPEG pour les miniatures. au lieu de cela, vous devez déléguer au décodeur JPEG fourni par Windows composant d’imagerie (WIC).

Pour plus d’informations sur les miniatures, consultez la méthode [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) sur l' [implémentation de IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).

### <a name="getcolorcontexts"></a>GetColorContexts

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) retourne les contextes de couleur valides (également appelés profils de couleurs) associés à l’image dans ce frame. Dans la plupart des cas, il ne s’agit que d’un seul, mais il peut y avoir des cas où il y a deux ou, rarement, plus. L’appelant passera un ou plusieurs objets [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , en définissant le paramètre *ompte* pour indiquer le nombre de fois qu’ils sont transmis. Cette méthode remplit les objets **IWICColorContext** avec les données de contexte de couleur réelles pour les profils de couleur associés à l’image. Définissez le paramètre *pcActualCount* sur le nombre réel de contextes de couleur associés à l’image, même si cette valeur est supérieure au nombre que vous pouvez retourner. (Dans le cas où d’autres contextes de couleur sont disponibles que le nombre d’objets **IWICColorContext** transmis par l’appelant, cela indique à l’appelant qu’un ou plusieurs autres contextes sont disponibles.)

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) retourne un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) qu’une application peut utiliser pour récupérer des métadonnées à partir du frame d’image. Cette interface est implémentée par un gestionnaire de métadonnées et permet à une application d’interroger des propriétés de métadonnées spécifiques appartenant à un format de métadonnées particulier. Pour plus d’informations, consultez [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).

Pour instancier un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), appelez [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) sur [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>Obtient, GetPixelFormat et GetResolution

[](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)Les requêtes, [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)et [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) sont explicites et retournent les propriétés demandées de l’image.

### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) est la méthode qu’une application appelle lorsqu’elle souhaite créer une bitmap en mémoire qui peut être rendue sur l’écran ou l’imprimante. Il s’agit de la méthode qui effectue le décodage réel des bits de l’image. Les paramètres sont un rectangle, qui représente la région d’intérêt de l’image source à copier en mémoire ; STRIDE, qui spécifie le nombre d’octets dans une ligne d’analyse ; taille de la mémoire tampon allouée par l’application ; et un pointeur vers la mémoire tampon dans laquelle les bits d’image demandés doivent être copiés. (Pour empêcher les dépassements de mémoire tampon potentiels d’introduire des failles de sécurité, veillez à copier uniquement le nombre de données d’image dans la mémoire tampon en spécifiant le paramètre *cbBufferSize* .)

### <a name="copypalette"></a>CopyPalette

Seuls les codecs ayant des formats de pixel indexés doivent implémenter la méthode [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) . Si une image utilise un format indexé, utilisez cette méthode pour retourner la palette des couleurs utilisées dans l’image. Si votre CODEC n’a pas de format indexé, retournez WINCODEC \_ Err \_ PALETTEUNAVAILABLE.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation de IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Implémentation de IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



