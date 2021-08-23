---
description: la rubrique présente le décodeur bitmap, un principal composant codec WIC (Windows Imaging component) utilisé pour décoder les fichiers image d’un flux.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Décodage, vue d’ensemble
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14300c9857702ceff5f07fcc127a4ef4182f9e77ad46f0598edc12abf91f240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711401"
---
# <a name="decoding-overview"></a>Décodage, vue d’ensemble

la rubrique présente le décodeur bitmap, un principal composant codec WIC (Windows Imaging component) utilisé pour décoder les fichiers image d’un flux.

Cette rubrique contient les sections suivantes.

-   [Introduction](#introduction)
-   [Décodeurs bitmap natifs](#native-bitmap-decoders)
-   [Création d’un décodeur bitmap](#creating-a-bitmap-decoder)
-   [Extensibilité du décodeur](#decoder-extensibility)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Les décodeurs bitmap peuvent être affichés comme conteneur externe d’une image numérique et permettent d’accéder à des propriétés globales et à des frames d’image. Certains formats d’image prennent en charge les miniatures globales, les aperçus, les contextes de couleur ou les métadonnées, tandis que d’autres fournissent ces propriétés uniquement au niveau du frame. Notez, toutefois, que la plupart des formats d’image standard ne prennent pas en charge ces propriétés globales. Ainsi, la plupart des implémentations de codec natives fournies par WIC ne prennent pas en charge la plupart de ces propriétés globales. Pour plus d’informations sur la prise en charge des propriétés globales, consultez le tableau dans la section décodeurs bitmap natifs de cette rubrique.

Dans WIC, les décodeurs bitmap sont représentés par l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et fournissent l’accès à ces propriétés globales de la bitmap et, plus important encore, aux frames qu’elle contient. L’interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) représente un frame de bitmap individuel et est décrite en détail dans la [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

## <a name="native-bitmap-decoders"></a>Décodeurs bitmap natifs

WIC fournit plusieurs implémentations natives de l’interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) pour les formats d’image Web standard et le format de photo HD à plage dynamique élevée. Le tableau suivant répertorie les décodeurs natifs disponibles, le nom de l’identificateur de classe et la prise en charge des propriétés globales. Bien qu’une fonctionnalité ne prenne pas en charge une propriété telle que les miniatures au niveau global, le format d’image peut prendre en charge de telles propriétés au niveau du frame individuel.



| Format d'image | Nom du CLSID            | Miniatures | Versions préliminaires | Contextes de couleur | Métadonnées |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | CLSID \_ WICBmpDecoder  | Non         | Non       | Non             | Non       |
| GIF          | CLSID \_ WICGifDecoder  | Non         | Non       | Non             | Oui      |
| ICO          | CLSID \_ WICIcoDecoder  | Non         | Non       | Non             | Non       |
| JPEG         | CLSID \_ WICJpegDecoder | Non         | Non       | Non             | Non       |
| PNG          | CLSID \_ WICPngDecoder  | Non         | Non       | Non             | Non       |
| TIFF         | CLSID \_ WICTiffDecoder | Non         | Non       | Non             | Non       |
| Photo HD     | CLSID \_ WICWmpDecoder  | Non         | Oui      | Non             | Non       |



 

## <a name="creating-a-bitmap-decoder"></a>Création d’un décodeur bitmap

Pour décoder une image à l’aide de WIC, vous devez d’abord créer une instance de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) pour le format d’image ciblé. L’instance de décodeur vous permet d’accéder aux propriétés globales et aux métadonnées, si elles sont prises en charge, ainsi qu’aux trames d’image. La fabrique d’images WIC, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), fournit plusieurs méthodes pour créer des décodeurs bitmap. Les méthodes de fabrique suivantes sont fournies pour créer des décodeurs bitmap.

-   [**CreateDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

Le code suivant montre comment créer un décodeur bitmap à l’aide d’un nom de fichier image et récupérer la première image de l’image.


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



## <a name="decoder-extensibility"></a>Extensibilité du décodeur

L’une des principales fonctionnalités de WIC est un Framework d’extensibilité qui permet aux développeurs de codec de développer leurs propres codecs d’image et d’avoir la même prise en charge de plate-forme que les implémentations natives de codecs d’image. Un ensemble unique et cohérent d’interfaces est utilisé pour le traitement de tous les images, quel que soit le format d’image. Toute application utilisant WIC obtient la prise en charge automatique des nouveaux formats d’image dès que le codec est installé. Pour plus d’informations sur le développement de codecs, consultez les rubriques relatives au [développement de composants](-wic-component-development.md). Pour plus d’informations sur le développement d’un décodeur, consultez [implémentation d’un décodeur de WIC-Enabled](-wic-implementingwicdecoder.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble de l’encodage](-wic-creating-encoder.md)
</dt> <dt>

[Développement de composants](-wic-component-development.md)
</dt> </dl>

 

 



