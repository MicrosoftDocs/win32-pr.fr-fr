---
description: Spécifications de la méthode d’interface
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Spécifications de la méthode d’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8525f7b04fe82247ecd64a38f5f1acc298be5d3ace56303072268fed6a4a3cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086922"
---
# <a name="interface-method-requirements"></a>Spécifications de la méthode d’interface

Aucune méthode sur chaque interface ne doit avoir une implémentation. Par exemple, certains codecs ont des métadonnées globales, des miniatures ou des contextes de couleur, tandis que d’autres codec les fournissent uniquement pour chaque image. Si les auteurs de codec ne les fournissent qu’en fonction [**de la**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)trame, ils ont uniquement besoin d’implémenter / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) ou ColorContexts, ou d’implémenter les méthodes [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) ou [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) sur [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) et [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) plutôt que sur [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). De même, certains codecs n’utilisent pas de formats indexés et n’ont donc pas besoin d’implémenter les méthodes [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) et [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) . Ces méthodes sont donc facultatives et restent à la discrétion du créateur du codec. La plupart des autres méthodes sont requises.

pour Windows 7, [**obtenir**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) et [**obtenir**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)des / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) sont requis et doivent être implémentés sur les classes de niveau supérieur ou sur les classes de niveau frame. Si votre format de fichier image ne prend pas en charge les aperçus ou les miniatures dans l’un de ces emplacements, vous devez modifier votre format de fichier image pour fournir une telle prise en charge.

Lorsqu’une méthode n’est pas implémentée, il est important de retourner une erreur appropriée afin que l’appelant puisse déterminer que la fonctionnalité demandée n’est pas prise en charge. Par exemple, si les auteurs de codec ne prennent pas en charge les miniatures au niveau du conteneur, ils doivent retourner [WINCODEC \_ Err \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) lorsqu’une application appelle [**miniature**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)et, si elles n’ont pas de palette, elles doivent retourner [WINCODEC \_ Err \_ PALETTEUNAVAILABLE](-wic-codec-error-codes.md). S’il n’existe aucun code d' [ \_ erreur WINCODEC](-wic-codec-error-codes.md) approprié, le codec doit retourner E \_ NOTIMPL pour les méthodes non implémentées.

les tableaux suivants répertorient les méthodes obligatoires et facultatives pour chaque interface de composant d’imagerie Windows (WIC).

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



Obligatoire

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[**Initialiser**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

Facultatif

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹

[**Miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹ requis si votre format de fichier image prend en charge les aperçus au niveau du conteneur. Si ce n’est pas le cas, il est vivement recommandé de modifier le format de votre fichier image pour le prendre en charge. Si elle est implémentée ici, un [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) correspondant est requis sur la classe encode au niveau du conteneur.

² requis ici, ou sur la classe de décodage au niveau de la trame, selon l’emplacement de stockage des miniatures dans le format de fichier image. Si elle est implémentée ici, un [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) correspondant est requis sur la classe encode au niveau du conteneur.

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



Obligatoire

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

Facultatif

[**Miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹ requis ici, ou sur la classe de décodage au niveau du conteneur, selon l’endroit où vous stockez les miniatures dans le format de fichier image. Si elle est implémentée ici, un [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) correspondant est requis sur la classe de codeur au niveau de la trame.

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Obligatoire

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



Obligatoire

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

Facultatif

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

Consultez [prise en charge de IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), plus loin dans ce document.

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



Obligatoire

[**Initialiser**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[**Commiter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Facultatif

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

¹ requis si votre format de fichier image prend en charge les aperçus au niveau de la trame.

² requis ici, ou sur la classe de codage au niveau de la trame, selon l’emplacement de stockage des miniatures dans le format de fichier image. Si elle est implémentée ici, un [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) correspondant est requis sur la classe de décodage au niveau du conteneur.

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



Obligatoire

[**Initialiser**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[**Commiter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Facultatif

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹

[**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

¹ requis ici ou sur la classe encode au niveau du conteneur, selon l’endroit où votre fichier image stocke les miniatures. Si elle est implémentée ici, un [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) correspondant est requis sur la classe de décodage au niveau de la trame.

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Obligatoire

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
