---
description: cette rubrique présente les sources bitmap, un composant core Windows Imaging component (WIC) qui représente les pixels bitmap d’une image.
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: Vue d’ensemble des sources bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910bfc253798058639b98a1d1beaacec9bd4d1bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231035"
---
# <a name="bitmap-sources-overview"></a>Vue d’ensemble des sources bitmap

cette rubrique présente les sources bitmap, un composant core Windows Imaging component (WIC) qui représente les pixels bitmap d’une image.

Cette rubrique contient les sections suivantes.

-   [Sources bitmap](#bitmap-sources-overview)
-   [Frames bitmap](#bitmap-frames)
-   [Images bitmap](#bitmap-sources-overview)
-   [Transformer des sources bitmap](#transform-bitmap-sources)
-   [Format de pixel et convertisseurs de contexte de couleur](#pixel-format-and-color-context-converters)
-   [Dessin de sources bitmap](#drawing-bitmap-sources)
-   [Rubriques connexes](#related-topics)

## <a name="bitmap-sources"></a>Sources bitmap

Le composant [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) est le bloc de construction de base de WIC et représente un seul jeu de pixels. Une source bitmap peut être un frame individuel d’une image à plusieurs frames, ou peut être le résultat d’une transformation effectuée sur une source bitmap. L’interface **IWICBitmapSource** est la base de la plupart des interfaces WIC principales, telles que le frame de décodeur [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) et la transformation de sources bitmap telles que [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).

Le tableau suivant décrit les différents composants sources bitmap fournis par WIC.



| Sources bitmap                                                    | Description                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | Représente une image de décodeur.                                    |
| [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | Fournit une représentation en écriture et en mémoire pour les sources bitmap. |
| [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | Découpe une source bitmap en un rectangle souhaité.                        |
| [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | Retourne et/ou fait pivoter une source bitmap à l’orientation souhaitée.       |
| [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | Met à l’échelle une source bitmap à une taille souhaitée.                            |
| [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | Transforme le contexte de couleur d’une source bitmap.                     |
| [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | Convertit le format de pixel d’une source bitmap.                        |



 

## <a name="bitmap-frames"></a>Frames bitmap

Le [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) le plus courant est le [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Cette interface est utilisée pour accéder aux données bitmap réelles d’un format d’image. De nombreux formats d’image prennent uniquement en charge un seul Frame bitmap, tandis que d’autres formats tels que GIF et TIFF prennent en charge plusieurs images par image.

Pour obtenir un exemple sur l’obtention d’images bitmap à partir d’une image, consultez la rubrique [Comment récupérer les frames d’une image](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) .

## <a name="bitmaps"></a>Images bitmap

Un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) ajoute les concepts d’accessibilité et de mémoire statique aux sources bitmap. Les bitmaps WIC permettent aux utilisateurs d’accéder directement aux pixels d’une source bitmap. Cet accès direct est fourni par la méthode [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) et prend en charge toute combinaison d’accès en lecture et/ou en écriture aux pixels bitmap. La méthode **Lock** verrouille le rectangle bitmap spécifié et fournit un objet [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) pour accéder aux pixels.

Pour obtenir un exemple d’utilisation des objets [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) et [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) , consultez la rubrique [Comment modifier les pixels d’une source bitmap](-wic-bitmapsources-howto-modifypixels.md) .

## <a name="transform-bitmap-sources"></a>Transformer des sources bitmap

WIC fournit plusieurs interfaces [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) qui transforment les données de pixels. Plus précisément, WIC fournit des transformations de source bitmap pour la mise à l’échelle, le découpage, la rotation et le retournement des données de pixels. Ces transformations de source bitmap sont [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)et [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator). Chacune de ces sources d’image bitmap a une méthode pour initialiser et créer une nouvelle source de bitmap transformée. Par exemple, **IWICBitmapClipper** comprend la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) . Cette méthode initialise la source de l’image bitmap Clipper avec les données de pixels découpées de la source de l’image bitmap en entrée à l' [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)donné.

Les rubriques de procédures suivantes illustrent différentes utilisations des sources bitmap de transformation.

-   [Mise à l’échelle d’une source bitmap](-wic-bitmapsources-howto-scale.md)
-   [Comment découper une source bitmap](-wic-bitmapsources-howto-clip.md)
-   [Comment retourner et faire pivoter une source bitmap](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a>Format de pixel et convertisseurs de contexte de couleur

WIC fournit également des sources bitmap qui convertissent le format de pixel et le contexte de couleur d’une source bitmap. WIC fournit les [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) et [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) pour ces opérations.

[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) convertit une source bitmap donnée d’un format de pixel à un autre.

Pour obtenir un exemple d’utilisation de [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter), consultez la rubrique [Comment dessiner une source bitmap à l’aide de Direct2D](-wic-bitmapsources-howto-drawusingd2d.md) .

## <a name="drawing-bitmap-sources"></a>Dessin de sources bitmap

WIC est une technologie de codec d’image continue qui est utilisée pour gérer les métadonnées et les données d’image et ne fournit pas par nature un moyen de restituer des images. toutefois, les sources bitmap peuvent être dessinées à l’aide de plusieurs technologies Windows graphics, telles que Direct2D, Windows Graphics Device Interface (GDI) et Windows GDI+. Chacune de ces technologies a un niveau d’interopérabilité différent avec WIC. Direct2D fournit une interopérabilité directe via l’interface [ID2D1Bitmap](../direct2d/render-targets-overview.md) et la méthode [ID2D1RenderTarget :: CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) , tandis que GDI et GDI+ requièrent que les utilisateurs copient les pixels de la source bitmap dans des [bitmaps](../gdi/bitmaps.md).

L’exemple suivant montre comment dessiner des sources bitmap à l’aide de Direct2D.

-   [Comment dessiner une source bitmap à l’aide de Direct2D](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble de l’encodage](-wic-creating-encoder.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
