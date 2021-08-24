---
description: à partir de Windows 8.1, le codec JPEG du composant Windows Imaging Component (WIC) prend en charge la lecture et l’écriture des données d’image dans sa forme YCbCr native.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: Prise en charge d’JPEG YCbCr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f8548a458f70265d248e1d686ad3bc300d7cfee2bc1e0ab2262ee652f0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086803"
---
# <a name="jpeg-ycbcr-support"></a>Prise en charge d’JPEG YCbCr

à partir de Windows 8.1, le codec JPEG du [composant Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) prend en charge la lecture et l’écriture des données d’image dans son format natif YC<sub>b</sub>C<sub>r</sub> . La prise en charge de WIC YC<sub>b</sub>c<sub>r</sub> peut être utilisée conjointement avec [Direct2D](../direct2d/direct2d-portal.md) pour restituer les données de pixels YC<sub>b</sub>c<sub>r</sub> avec un effet d’image. En outre, le codec WIC JPEG peut consommer des données de pixels YC<sub>b</sub>C<sub>r</sub> produites par certains pilotes d’appareil photo via Media Foundation.

Les données de pixels YC<sub>b</sub>C<sub>r</sub> consomment beaucoup moins de mémoire que les formats de pixel standard BGRA. En outre, l’accès aux données YC<sub>b</sub>C<sub>r</sub> vous permet de décharger certaines étapes du pipeline de décodage/codage JPEG vers Direct2D, ce qui accélère l’accélération du GPU. En utilisant YC<sub>b</sub>C<sub>r</sub>, votre application peut réduire la consommation de mémoire JPEG et les temps de chargement pour les mêmes images de taille et de qualité. Ou bien, votre application peut utiliser plus de images JPEG de résolution plus élevée sans subir de pénalités en matière de performances.

Cette rubrique décrit le fonctionnement<sub>des données de</sub> l’YC<sub>b</sub>C et comment l’utiliser dans WIC et Direct2D.

-   [À propos des données JPEG YC<sub>b</sub>C<sub>r</sub>](#about-jpeg-ycbcr-data)
    -   [Modèle de couleurs YC<sub>b</sub>C<sub>r</sub>](#ycbcr-color-model)
    -   [Dispositions de mémoire planaires et entrelacées](#planar-versus-interleaved-memory-layouts)
    -   [Sous-échantillonnage de chrominance](#chroma-subsampling)
    -   [Utilisation JPEG de YC<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Utilisation de données JPEG YC<sub>b</sub>C<sub>r</sub>](#using-jpeg-ycbcr-data)
    -   [Utilisation d’images JPEG YC<sub>b</sub>C<sub>r</sub>](#using-ycbcr-jpeg-images)
    -   [Windows API du composant de création d’images](#windows-imaging-component-apis)
    -   [API Direct2D](#direct2d-apis)
    -   [Détermination de la prise en charge de la configuration YC<sub>b</sub>C<sub>r</sub>](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Décodage des données de pixels YC<sub>b</sub>C<sub>r</sub>](#decoding-ycbcr-pixel-data)
    -   [Transformation des données de pixels YC<sub>b</sub>C<sub>r</sub>](#transforming-ycbcr-pixel-data)
    -   [Encodage de données de pixels YC<sub>b</sub>C<sub>r</sub>](#encoding-ycbcr-pixel-data)
    -   [Décodage des données de pixels YC<sub>b</sub>C<sub>r</sub> en Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [Rubriques connexes](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>À propos des données JPEG YC<sub>b</sub>C<sub>r</sub>

Cette section explique quelques concepts clés nécessaires pour comprendre le fonctionnement de la prise en charge de l’YC<sub>b</sub>C<sub>r</sub> dans WIC et ses principaux avantages.

### <a name="ycsubbsubcsubrsub-color-model"></a>Modèle de couleurs YC<sub>b</sub>C<sub>r</sub>

WIC dans Windows 8 et versions antérieures prend en charge quatre [modèles de couleurs](-wic-codec-native-pixel-formats.md)différents, le plus courant étant rvb/BGR. Ce modèle de couleurs définit les données de couleur à l’aide des composants rouge, vert et bleu. un quatrième composant alpha peut également être utilisé.

L’image ci-dessous est décomposée en ses composants rouge, vert et bleu.

![une image décomposée en ses composants rouge, vert et bleu.](graphics/ycbcr1.png)

YC<sub>b</sub>C<sub>r</sub> est un autre modèle de couleurs qui définit les données de couleur à l’aide d’un composant de luminance (Y) et de deux composants de chrominance (c<sub>b</sub> et c<sub>r</sub>). Il est couramment utilisé dans les scénarios de création d’images numériques et de vidéo. Le terme YC<sub>b</sub>C<sub>r</sub> est souvent utilisé de façon interchangeable avec YUV, bien que les deux soient techniquement distincts.

Il existe plusieurs variantes de YC<sub>b</sub>C<sub>r</sub> qui diffèrent dans l’espace de couleurs et les définitions de plages dynamiques : WIC prend en charge spécifiquement les données JPEG JFIF YC<sub>b</sub>C<sub>r</sub> . Pour plus d’informations, reportez-vous à la [spécification ITU-T81 JPEG](https://www.w3.org/Graphics/JPEG/itu-t81.pdf).

Voici une image décomposée de ses composants Y, C<sub>b</sub>et c<sub>r</sub> .

![une image décomposée en ses composants y, CB et CR.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Dispositions de mémoire planaires et entrelacées

Cette section décrit certaines différences entre l’accès et le stockage des données de pixels RVB en<sub></sub>mémoire par rapport aux données<sub>r C r</sub> YC.

Les données de pixels RVB sont généralement stockées à l’aide d’une disposition de mémoire entrelacée. Cela signifie que les données pour un composant de couleur unique sont entrelacées entre les pixels, et chaque pixel est stocké de façon contiguë en mémoire.

Voici une figure qui montre les données de pixels RVBA stockées dans une disposition de mémoire entrelacée.

![figure qui montre les données de pixels RVBA stockées dans une disposition de mémoire entrelacée.](graphics/ycbcr3.png)

Les données YC<sub>b</sub>C<sub>r</sub> sont généralement stockées à l’aide d’une disposition de mémoire planaire. Cela signifie que chaque composant de couleur est stocké séparément dans son propre plan contigu, pour un total de trois plans. Dans une autre configuration courante, les composants C<sub>b</sub> et c<sub>r</sub> sont entrelacés et stockés ensemble, tandis que le composant Y reste dans son propre plan, pour un total de deux plans.

Voici une figure présentant les données<sub>de pixels planaires</sub> Y et entrelacées c<sub>b</sub>c, une disposition courante de<sub></sub>mémoire<sub>r c r</sub> .

![Figure présentant les données de pixels planaires y et entrelacées CbCr, une disposition de mémoire YCbCr courante.](graphics/ycbcr4.png)

Dans WIC et Direct2D, chaque plan de couleur est traité comme son propre objet distinct ( [IWICBitmapSource](-wic-imp-iwicbitmapsource.md) ou [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)), et collectivement ces plans forment les données de stockage pour une image YC <sub>b</sub>C <sub>r</sub> .

Alors que WIC prend en charge l’accès aux données YC<sub>b</sub>C<sub>r</sub> dans les configurations à 2 et 3 plans, Direct2D ne prend en charge que le premier (Y et c<sub>b</sub>c<sub>r</sub>). Par conséquent, lors de l’utilisation conjointe de WIC et de Direct2D, vous devez toujours utiliser la configuration à 2 plans YC<sub>b</sub>C<sub>r</sub> .

### <a name="chroma-subsampling"></a>Sous-échantillonnage de chrominance

Le modèle de couleurs YC<sub>b</sub>C<sub>r</sub> est bien adapté aux scénarios de création d’images numériques, car il peut tirer parti de certains aspects du système visuel humain. En particulier, les êtres humains sont plus sensibles aux modifications de luminance (luminosité) d’une image et moins sensibles à la chrominance (couleur). En fractionnant les données de couleur en composants de luminance et de chrominance distincts, nous pouvons compresser de manière sélective uniquement les composants de chrominance pour réaliser des économies d’espace avec une perte de qualité minimale.

Une technique pour ce faire est appelée « sous-échantillonnage Chroma ». Les plans C<sub>b</sub> et c<sub>r</sub> sont sous-échantillonnés (downscaled) dans l’une des dimensions horizontales et verticales (ou les deux). Pour des raisons historiques, chaque mode de sous-échantillonnage Chroma est généralement appelé à l’aide d’un ratio J :a: b en trois parties.



| Mode de sous-échantillonnage | Réduire horizontal | Réduire vertical | Bits par pixel\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | x 2                   | 1x                 | 16               |
| 4:4:0            | 1x                   | x 2                 | 16               |
| 4:2:0            | x 2                   | x 2                 | 12               |



 

\* Comprend des données Y.

Dans le tableau ci-dessus, si vous utilisez YC<sub>b</sub>C<sub>r</sub> pour stocker des données d’image non compressées, vous pouvez réaliser des économies de mémoire de 25 à 62,5% par rapport aux données de 32 bits par pixel RVBA, en fonction du mode de sous-échantillonnage de chrominance utilisé.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>Utilisation JPEG de YC<sub>b</sub>C<sub>r</sub>

À un niveau élevé, le pipeline de décompression JPEG se compose des étapes suivantes :

1.  Effectuer une décompression d’entropie (par exemple, Huffman)
2.  Effectuer une DÉQUANTIFICATION
3.  Effectuer une transformation cosinus discrète inverse
4.  Effectuer un échantillonnage Chroma sur les données C<sub>b</sub>c<sub>r</sub>
5.  Convertir les données YC<sub>b</sub>C<sub>r</sub> en RVBA (si nécessaire)

En faisant en sorte que le codec JPEG produise des données YC<sub>b</sub>C<sub>r</sub> , nous pouvons éviter les deux dernières étapes du processus de décodage, ou les reporter au GPU. Outre les économies de mémoire indiquées dans la section précédente, cela réduit considérablement le temps total nécessaire pour décoder l’image. Les mêmes économies s’appliquent lors de l’encodage des données YC<sub>b</sub>C<sub>r</sub> .

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Utilisation de données JPEG YC<sub>b</sub>C<sub>r</sub>

Cette section explique comment utiliser WIC et Direct2D pour fonctionner sur des données YC<sub>b</sub>C<sub>r</sub> .

Pour consulter les instructions de ce document utilisées dans la pratique, consultez l' [exemple optimisations JPEG d’images JPEG dans Direct2D et WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) , qui illustre toutes les étapes nécessaires au décodage<sub></sub>et au rendu du contenu<sub>r C r</sub> YC dans une application Direct2D.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Utilisation d’images JPEG YC<sub>b</sub>C<sub>r</sub>

La grande majorité des images JPEG sont stockées sous la forme YC<sub>b</sub>C<sub>r</sub>. Certains JPEG contiennent des données CMJN ou nuances de gris et n’utilisent pas YC<sub>b</sub>C<sub>r</sub>. Cela signifie que vous pouvez généralement, mais pas toujours, utiliser directement du contenu JPEG préexistant sans aucune modification.

WIC et Direct2D ne prennent pas en charge toutes les configurations possibles de YC<sub>b</sub>c<sub>r</sub> , et la prise en charge de YC<sub>b</sub>c<sub>r</sub> dans Direct2D dépend du matériel et du pilote graphiques sous-jacents. Pour cette raison, un pipeline d’imagerie à usage général doit être robuste pour les images qui n’utilisent pas YC<sub>b</sub>c<sub>r</sub> (y compris les autres formats d’image courants tels que png ou BMP) ou dans les cas où la prise en charge de l’YC<sub>b</sub>c<sub>r</sub> n’est pas disponible. Nous vous recommandons de conserver votre pipeline d’images BGRA existant et d’activer YC<sub>b</sub>C<sub>r</sub> comme optimisation des performances lorsqu’il est disponible.

### <a name="windows-imaging-component-apis"></a>Windows API du composant de création d’images

le WIC dans Windows 8.1 ajoute trois nouvelles interfaces pour fournir l’accès aux données JPEG YC<sub>b</sub>C<sub>r</sub> .

### <a name="iwicplanarbitmapsourcetransform"></a>IWICPlanarBitmapSourceTransform

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) est analogue à [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), à ceci près qu’il produit des pixels dans une configuration planaire, y compris les données r <sub>C</sub><sub>r</sub> YC. Vous pouvez obtenir cette interface en appelant QueryInterface sur une implémentation de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) qui prend en charge l’accès Planar. Cela comprend l’implémentation du codec JPEG de [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) , ainsi que [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)et [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform).

### <a name="iwicplanarbitmapframeencode"></a>IWICPlanarBitmapFrameEncode

[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) offre la possibilité d’encoder des données de pixels planaires, y compris les données <sub>r C r</sub> <sub>Yc.</sub> Vous pouvez obtenir cette interface en appelant QueryInterface sur l’implémentation de [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)du codec JPEG.

### <a name="iwicplanarformatconverter"></a>IWICPlanarFormatConverter

[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) permet à [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) de consommer des données de pixels planaires, y compris YC <sub>b</sub>C <sub>r</sub>, et de les convertir au format de pixel entrelacé. Elle n’expose pas la possibilité de convertir des données de pixels entrelacées en un format Planar. vous pouvez obtenir cette interface en appelant QueryInterface sur le Windows implémentation de **IWICFormatConverter** fournie.

### <a name="direct2d-apis"></a>API Direct2D

Direct2D dans Windows 8.1 prend en charge les données de pixels planaires c c<sub>r</sub> yc avec le nouvel effet d'<sub>image c</sub><sub>r</sub> yc<sub>b</sub>. Cet effet offre la possibilité de restituer les données<sub>r</sub> YC<sub>b</sub>C. L’effet prend comme entrée deux interfaces [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) : l’une contenant les données planaires Y au format dxgi \_ \_ R8 \_ UNORM et l’autre contenant les données CbCr entrelacées au format dxgi \_ R8G8 \_ \_ UNORM. En général, vous utilisez cet effet à la place des **ID2D1Bitmap** qui contenaient des données de pixels BGRA.

L’effet de l’image<sub>r</sub> YC<sub>b</sub>c est destiné à être utilisé conjointement avec les API WIC YC<sub>b</sub>c<sub>r</sub> qui fournissent les données YC<sub>b</sub>c<sub>r</sub> . Cela permet de décharger une partie du travail de décodage de l’UC vers le GPU, où il peut être traité plus rapidement et en parallèle.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Détermination de la prise en charge de la configuration YC<sub>b</sub>C<sub>r</sub>

Comme indiqué précédemment, votre application doit être fiable dans les cas où la prise en charge de YC<sub>b</sub>C<sub>r</sub> n’est pas disponible. Cette section décrit les conditions que votre application doit vérifier. Si l’une des vérifications suivantes échoue, votre application doit revenir à un pipeline BGRA standard.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>Le composant WIC prend-il en charge l’accès aux données YC<sub>b</sub>C<sub>r</sub> ?

seuls les Windows codec JPEG fournis et certaines transformations WIC prennent en charge l’accès aux données YC<sub>b</sub>C<sub>r</sub> . pour obtenir une liste complète, reportez-vous à la section [api du composant de création d’images Windows](#windows-imaging-component-apis) .

Pour obtenir l’une des interfaces c++<sub></sub>YC b<sub>r</sub> planaires, appelez QueryInterface sur l’interface d’origine. Cela échoue si le composant ne prend pas en charge l’accès aux données YC<sub>b</sub>C<sub>r</sub> .

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>La transformation WIC demandée est-elle prise en charge pour YC<sub>b</sub>C<sub>r</sub>?

Après avoir obtenu un [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform), vous devez d’abord appeler [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform). Cette méthode prend comme paramètres d’entrée l’ensemble complet des transformations que vous souhaitez appliquer aux données planaires<sub>b</sub>C<sub>r</sub> planes, et retourne une valeur booléenne indiquant la prise en charge, ainsi que les dimensions les plus proches de la taille demandée qui peut être retournée. Vous devez vérifier les trois valeurs avant d’accéder aux données de pixels avec [**IWICPlanarBitmapSourceTransform :: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels).

Ce modèle est similaire à la façon dont [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) est utilisé.

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>Le pilote Graphics prend-il en charge les fonctionnalités nécessaires à l’utilisation de YC<sub>b</sub>C<sub>r</sub> avec Direct2D ?

Cette vérification n’est nécessaire que si vous utilisez l’effet Direct2D YC<sub>b</sub>c<sub>r</sub> pour restituer le contenu<sub>r</sub> YC<sub>b</sub>c. Direct2D stocke les données YC<sub>b</sub>C<sub>r</sub> à l’aide du \_ format dxgi \_ R8 \_ UNORM et dxgi \_ format \_ R8G8 \_ UNORM pixel formats, qui ne sont pas disponibles à partir de tous les pilotes graphiques.

Avant d’utiliser l’effet de l’image C <sub>r</sub> YC <sub>b</sub>, vous devez appeler [**ID2D1DeviceContext :: IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) pour vous assurer que les deux formats sont pris en charge par le pilote.

### <a name="sample-code"></a>Exemple de code

Vous trouverez ci-dessous un exemple de code illustrant les vérifications recommandées. Cet exemple a été extrait des [optimisations JPEG YCbCr dans Direct2D et WIC Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
bool DirectXSampleRenderer::DoesWicSupportRequestedYCbCr()
{
    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    HRESULT hr = m_wicScaler.As(&wicPlanarSource);
    if (SUCCEEDED(hr))
    {
        BOOL isTransformSupported;
        uint32 supportedWidth = m_cachedBitmapPixelWidth;
        uint32 supportedHeight = m_cachedBitmapPixelHeight;
        DX::ThrowIfFailed(
            wicPlanarSource->DoesSupportTransform(
                &supportedWidth,
                &supportedHeight,
                WICBitmapTransformRotate0,
                WICPlanarOptionsDefault,
                SampleConstants::WicYCbCrFormats,
                m_planeDescriptions,
                SampleConstants::NumPlanes,
                &isTransformSupported
                )
            );

        // The returned width and height may be larger if IWICPlanarBitmapSourceTransform does not
        // exactly support what is requested.
        if ((isTransformSupported == TRUE) &&
            (supportedWidth == m_cachedBitmapPixelWidth) &&
            (supportedHeight == m_cachedBitmapPixelHeight))
        {
            return true;
        }
    }

    return false;
}

bool DirectXSampleRenderer::DoesDriverSupportYCbCr()
{
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    return (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8_UNORM)) &&
        (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8G8_UNORM));
}
```



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Décodage des données de pixels YC<sub>b</sub>C<sub>r</sub>

Si vous souhaitez obtenir des données de pixels YC <sub>b</sub>C <sub>r</sub> , vous devez appeler [**IWICPlanarBitmapSourceTransform :: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels). Cette méthode copie les données de pixels dans un tableau de structures [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) remplies, une pour chaque plan de données souhaité (par exemple, Y et c <sub>b</sub>c <sub>r</sub>). Un **WICBitmapPlane** contient des informations sur les données de pixels et pointe vers la mémoire tampon qui recevra les données.

Si vous souhaitez utiliser les données de pixels YC <sub>b</sub>C <sub>r</sub> avec d’autres API WIC, vous devez créer un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)correctement configuré, appeler [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) pour obtenir la mémoire tampon sous-jacente et associer la mémoire tampon au [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) utilisé pour recevoir les données de pixels YC <sub>b</sub>C <sub>r</sub> . Vous pouvez ensuite utiliser le [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) normalement.

Enfin, si vous souhaitez restituer les données YC <sub>b</sub>c <sub>r</sub> dans Direct2D, vous devez créer un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à partir de chaque [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) et les utiliser en tant que source pour l’effet de l’image C <sub>r</sub> YC <sub>b</sub>. WIC vous permet de demander plusieurs configurations planaires. En cas d’interopérabilité avec Direct2D, vous devez demander deux plans, l’un utilisant le GUID \_ WICPixelFormat8bppY et l’autre à l’aide du GUID \_ WICPixelFormat16bppCbCr, car il s’agit de la configuration attendue par Direct2D.

### <a name="code-sample"></a>Exemple de code

Vous trouverez ci-dessous un exemple de code illustrant les étapes de décodage et de rendu des données YC<sub>b</sub>C<sub>r</sub> dans Direct2D. Cet exemple a été extrait des [optimisations JPEG YCbCr dans Direct2D et WIC Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
void DirectXSampleRenderer::CreateYCbCrDeviceResources()
{
    auto wicFactory = m_deviceResources->GetWicImagingFactory();
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    DX::ThrowIfFailed(
        m_wicScaler.As(&wicPlanarSource)
        );

    ComPtr<IWICBitmap> bitmaps[SampleConstants::NumPlanes];
    ComPtr<IWICBitmapLock> locks[SampleConstants::NumPlanes];
    WICBitmapPlane planes[SampleConstants::NumPlanes];

    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        DX::ThrowIfFailed(
            wicFactory->CreateBitmap(
                m_planeDescriptions[i].Width,
                m_planeDescriptions[i].Height,
                m_planeDescriptions[i].Format,
                WICBitmapCacheOnLoad,
                &bitmaps[i]
                )
            );

        LockBitmap(bitmaps[i].Get(), WICBitmapLockWrite, nullptr, &locks[i], &planes[i]);
    }

    DX::ThrowIfFailed(
        wicPlanarSource->CopyPixels(
            nullptr, // Copy the entire source region.
            m_cachedBitmapPixelWidth,
            m_cachedBitmapPixelHeight,
            WICBitmapTransformRotate0,
            WICPlanarOptionsDefault,
            planes,
            SampleConstants::NumPlanes
            )
        );

    DX::ThrowIfFailed(d2dContext->CreateEffect(CLSID_D2D1YCbCr, &m_d2dYCbCrEffect));

    ComPtr<ID2D1Bitmap1> d2dBitmaps[SampleConstants::NumPlanes];
    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        // IWICBitmapLock must be released before using the IWICBitmap.
        locks[i] = nullptr;

        // First ID2D1Bitmap1 is DXGI_FORMAT_R8 (Y), second is DXGI_FORMAT_R8G8 (CbCr).
        DX::ThrowIfFailed(d2dContext->CreateBitmapFromWicBitmap(bitmaps[i].Get(), &d2dBitmaps[i]));
        m_d2dYCbCrEffect->SetInput(i, d2dBitmaps[i].Get());
    }
}

void DirectXSampleRenderer::LockBitmap(
    _In_ IWICBitmap *pBitmap,
    DWORD bitmapLockFlags,
    _In_opt_ const WICRect *prcSource,
    _Outptr_ IWICBitmapLock **ppBitmapLock,
    _Out_ WICBitmapPlane *pPlane
    )
{
    // ComPtr guarantees the IWICBitmapLock is released if an exception is thrown.
    ComPtr<IWICBitmapLock> lock;
    DX::ThrowIfFailed(pBitmap->Lock(prcSource, bitmapLockFlags, &lock));
    DX::ThrowIfFailed(lock->GetStride(&pPlane->cbStride));
    DX::ThrowIfFailed(lock->GetDataPointer(&pPlane->cbBufferSize, &pPlane->pbBuffer));
    DX::ThrowIfFailed(lock->GetPixelFormat(&pPlane->Format));
    *ppBitmapLock = lock.Detach();
}
```



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Transformation des données de pixels YC<sub>b</sub>C<sub>r</sub>

La transformation des données YC <sub>b</sub>C <sub>r</sub> est quasiment identique au décodage, car les deux impliquent [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). La seule différence est l’objet WIC à partir duquel vous avez obtenu l’interface. le Windows scaler, rotate rotate et color transform prennent tous en charge l’accès YC<sub>b</sub>C<sub>r</sub> .

### <a name="chaining-transforms-together"></a>Chaînage des transformations

WIC prend en charge la notion de chaînage de plusieurs transformations. Par exemple, vous pouvez créer le pipeline WIC suivant :

![diagramme d’un pipeline WIC à partir d’un décodeur JPEG.](graphics/ycbcr5.png)

Vous pouvez ensuite appeler QueryInterface sur [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) pour obtenir [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). La transformation de couleur peut communiquer avec les transformations précédentes et peut exposer les fonctionnalités d’agrégation de chaque étape dans le pipeline. Le WIC permet de garantir que les données C<sub>r</sub> YC<sub>b</sub>sont conservées tout au long du processus. Ce chaînage fonctionne uniquement lorsque vous utilisez des composants qui prennent en charge l’accès à YC<sub>b</sub>C<sub>r</sub> .

### <a name="jpeg-codec-optimizations"></a>Optimisations du codec JPEG

À l’instar de l’implémentation du décodage de cadre JPEG de [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), l’implémentation du décodage de cadre JPEG de [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) prend en charge la mise à l’échelle et la rotation de domaine. Vous pouvez demander une puissance de deux réduire ou une rotation directement à partir du décodeur JPEG. Cela entraîne généralement une meilleure qualité et des performances supérieures à celles des transformations discrètes.

En outre, lorsque vous chaînez une ou plusieurs transformations WIC après le décodeur JPEG, elle peut tirer parti de la mise à l’échelle et de la rotation JPEG natives pour répondre à l’opération d’agrégation demandée.

### <a name="format-conversions"></a>Conversions de format

Utilisez [**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) pour convertir les données de pixels YC <sub>b</sub>C <sub>r</sub> planaires en un format de pixel entrelacé, tel que le GUID \_ WICPixelFormat32bppPBGRA. le WIC dans Windows 8.1 ne permet pas de convertir un format de pixel YC<sub>b</sub>C<sub>r</sub> planaire.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Encodage de données de pixels YC<sub>b</sub>C<sub>r</sub>

Utilisez [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) pour encoder les données de pixels YC <sub>b</sub>C <sub>r</sub> sur l’encodeur JPEG. L’encodage des données YC <sub>b</sub>C <sub>r</sub> **IWICPlanarBitmapFrameEncode** est similaire, mais pas identique à l’encodage des données entrelacées à l’aide de [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). L’interface planaire expose uniquement la possibilité d’écrire des données d’image planaire. vous devez continuer à utiliser l’interface de codage de frames pour définir des métadonnées ou une miniature et pour valider à la fin de l’opération.

Pour les cas typiques, procédez comme suit :

1.  Obtenez le [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) comme d’habitude. Si vous souhaitez configurer le sous-échantillonnage Chroma, définissez l’option encodeur [**JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) lors de la création du frame.
2.  Si vous avez besoin de définir des métadonnées ou une miniature, utilisez [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) comme normal.
3.  QueryInterface pour [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).
4.  Définissez les données de pixels YC <sub>b</sub>C <sub>r</sub> à l’aide de [**IWICPlanarBitmapFrameEncode :: WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) ou [**IWICPlanarBitmapFrameEncode :: WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels). Contrairement à leurs équivalents [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , vous fournissez ces méthodes avec un tableau de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) ou [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) qui contient les plans de pixels YC <sub>b</sub>C <sub>r</sub> .
5.  Lorsque vous avez terminé, appelez [**IWICBitmapFrameEncode :: Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Décodage des données de pixels YC<sub>b</sub>C<sub>r</sub> en Windows 10

à partir de Windows 10 build 1507, Direct2D fournit [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), un moyen plus simple de décoder les fichiers jpeg en Direct2D tout en tirant parti des optimisations YC <sub>b</sub>C <sub>r</sub> . **ID2D1ImageSourceFromWic** effectue automatiquement toutes les vérifications de la <sub>capacité</sub>C <sub>r</sub> YC nécessaires. elle utilise les codePath optimisés lorsque cela est possible et utilise un secours dans le cas contraire. Il permet également de nouvelles optimisations, telles que la mise en cache des sous-régions de l’image qui sont nécessaires à la fois.

Pour plus d’informations sur l’utilisation de [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), reportez-vous à l' [exemple](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)du kit de développement logiciel (SDK) Direct2D.

## <a name="related-topics"></a>Rubriques connexes

* [Optimisations JPEG YCbCr dans Direct2D et WIC, exemple](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
