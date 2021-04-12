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
# <a name="implementing-iwicbitmapsourcetransform"></a>Implémentation de IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Bien que facultatif, nous recommandons vivement que chaque décodeur implémente cette interface sur votre classe de décodage au niveau de la trame, car elle peut offrir des avantages majeurs en matière de performances. Quand une application demande une région spécifique d’intérêt, de taille, d’orientation ou de format de pixel, au lieu de simplement décoder l’image entière à la résolution complète, puis d’appliquer les transformations demandées, le composant WIC [:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour cette interface sur l’objet [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Si le décodeur de trame le prend en charge, WIC appelle la ou les méthodes appropriées pour déterminer si le décodeur de trame peut effectuer la transformation demandée ou déterminer la taille ou le format de pixel le plus proche que le décodeur peut fournir à celui qui a été demandé. Si le décodeur peut effectuer la transformation ou les transformations demandées, WIC appelle [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) avec les paramètres appropriés. Si le décodeur peut effectuer des transformations, mais pas toutes les transformations demandées, WIC demande au décodeur d’effectuer les transformations nécessaires et utilise les objets de transformation WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)et [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) pour effectuer les transformations restantes qui n’ont pas pu être effectuées par le décodeur de trame **sur le résultat de l'** Si le décodeur ne prend pas en charge [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), WIC doit utiliser les objets Transform pour effectuer toutes les transformations. Il est généralement plus efficace pour le décodeur d’effectuer des transformations pendant le processus de décodage que de décoder l’image entière, puis d’effectuer les transformations. Cela est particulièrement vrai pour les opérations telles que la mise à l’échelle vers une taille plus petite ou des conversions de format de pixel.


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



-   [DoesSupportTransform](#doessupporttransform)
-   [CopyPixels](#copypixels)
-   [GetClosestSize](#getclosestsize)
-   [GetClosestPixelFormat](#getclosestpixelformat)

### <a name="doessupporttransform"></a>DoesSupportTransform

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) demande si le décodeur prend en charge l’opération de rotation ou de retournement demandée. Les [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) qui peuvent être demandés sont :


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



### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) effectue le travail réel de décodage des bits d’image, tel que la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sur l’interface [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , mais la méthode [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) sur [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) est beaucoup plus puissante et peut améliorer considérablement les performances de traitement des images.

Lorsque plusieurs opérations de transformation sont demandées, le résultat est dépendant de l’ordre dans lequel les opérations sont exécutées. Pour garantir la prévisibilité et la cohérence entre les codecs, il est important que tous les codecs effectuent ces opérations dans le même ordre. Il s’agit de l’ordre canonique pour effectuer ces opérations.

1.  Scale
2.  Rogner
3.  Faire pivoter

La conversion du format de Pixel peut être effectuée à tout moment, car elle n’a aucun effet sur les autres transformations.

Le premier paramètre, *prcSrc*, est utilisé pour spécifier la région d’intérêt pour le découpage de l’image. Étant donné que la mise à l’échelle est effectuée avant le découpage par Convention, si l’image doit être mise à l’échelle et découpée, la zone d’intérêt doit être déterminée une fois l’image mise à l’échelle.

Le deuxième et le troisième paramètres indiquent la taille à laquelle la mise à l’échelle de l’image est mise à l’échelle.

Le paramètre *pguidDstFormat* indique le format de pixel demandé pour l’image décodée. Dans la mesure où WIC a déjà appelé [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), il doit s’agir d’un format de pixel que le décodeur a indiqué qu’il prend en charge.

Le paramètre *dstTransform* indique l’angle de rotation demandé et s’il faut retourner l’image verticalement, horizontalement ou les deux à la fois. Là encore, étant donné que WIC aura déjà appelé [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), la transformation demandée doit être celle que le décodeur a déjà indiqué qu’il prend en charge. N’oubliez pas que la rotation doit toujours être effectuée après la mise à l’échelle et le découpage.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) accepte deux paramètres in/out. L’appelant utilise les paramètres *puiWidth* et *puiHeight* pour spécifier la taille à laquelle l’appelant préfère le décodage de l’image. Toutefois, un décodeur peut décoder une image uniquement en une taille qui est un multiple de sa taille DCT, et les différents formats d’image peuvent avoir des tailles DCT différentes. Le décodeur doit déterminer, en fonction de sa propre taille DCT, le plus proche possible de la taille demandée, et définir les *puiWidth* et *puiHeight* sur ces dimensions au retour. Si une taille supérieure est demandée, mais que le codec ne prend pas en charge la mise à l’échelle, le fichier d’origine doit être retourné.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) est utilisé pour déterminer le format de pixel le plus proche du format de pixel demandé que le décodeur peut fournir sans perte de données. Il est toujours préférable de passer à un format de pixel plus large que plus étroit, même s’il augmente la taille de l’image, car il peut toujours être reconverti en un format plus restrictif, si nécessaire. Toutefois, une fois les données perdues, elles ne peuvent pas être récupérées.

## <a name="continued-reading"></a>Lecture continue

Pour en savoir plus sur la création d’un codec avec WIC activé, consultez [implémentation de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation de IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Implémentation de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
