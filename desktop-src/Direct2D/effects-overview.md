---
title: Effets (Direct2D)
description: Vue d’ensemble des effets Direct2D.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031607"
---
# <a name="effects"></a>Effets

## <a name="what-are-direct2d-effects"></a>Que sont les effets de Direct2D ?

Vous pouvez utiliser Direct2D pour appliquer un ou plusieurs effets de haute qualité à une image ou à un ensemble d’images. Les API Effects sont basées sur [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) et tirent parti des fonctionnalités GPU pour le traitement des images. Vous pouvez enchaîner des effets dans un graphique d’effet et composer ou mélanger la sortie d’effets.

Un effet Direct2D effectue une tâche de création d’images, telle que la modification de la luminosité, la désaturation d’une image ou la création d’une ombre portée. Les effets peuvent accepter zéro ou plusieurs images d’entrée, exposer plusieurs propriétés qui contrôlent leur fonctionnement et générer une seule image de sortie.

Chaque effet crée un graphique de transformation interne constitué de transformations individuelles. Chaque transformation représente une opération d’image unique. L’objectif principal d’une transformation est d’héberger les nuanceurs qui sont exécutés pour chaque pixel de sortie. Ces nuanceurs peuvent inclure des nuanceurs de pixels, des nuanceurs de sommets, l’étape de fusion d’un GPU et des nuanceurs de calcul.

Les [effets intégrés](built-in-effects.md) et les effets personnalisés [Direct2D](./direct2d-portal.md) que vous pouvez effectuer à l’aide de l' [API effets personnalisés](custom-effects.md) fonctionnent de cette façon.

Il existe une plage d' [effets intégrés](built-in-effects.md) à partir de catégories telles que celles-ci. Pour obtenir une liste complète, consultez la section [effets intégrés](built-in-effects.md) .

-   [Filtrage](built-in-effects.md)
-   [Composition et fusion](built-in-effects.md)
-   [Transparence](built-in-effects.md)
-   [Color](built-in-effects.md)
-   [Éclairage et stylisation](built-in-effects.md)
-   [Transformation et mise à l’échelle](built-in-effects.md)
-   [Sources](built-in-effects.md)

Vous pouvez appliquer des effets à n’importe quelle bitmap, y compris : les images chargées par le [composant WIC (Windows Imaging Component)](/windows/desktop/wic/-wic-api), les primitives dessinées par [Direct2D](./direct2d-portal.md), le texte de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)ou les scènes rendues par [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).

Avec les effets Direct2D, vous pouvez écrire vos propres effets que vous pouvez utiliser pour vos applications. Une infrastructure d’effet personnalisée vous permet d’utiliser des fonctionnalités GPU, telles que les nuanceurs de pixels, les nuanceurs de vertex et l’unité de fusion. Vous pouvez également inclure d’autres effets intégrés ou personnalisés dans votre effet personnalisé. L’infrastructure pour la création d’effets personnalisés est la même que celle utilisée pour créer les effets intégrés de [Direct2D](./direct2d-portal.md). L' [API d’effet Direct2D](custom-effects.md) fournit un ensemble d’interfaces pour créer et enregistrer des effets.

### <a name="more-effects-topics"></a>Rubriques supplémentaires sur les effets

Le reste de cette rubrique explique les principes fondamentaux des effets Direct2D, comme l’application d’un effet à une image. Le tableau ci-dessous contient des liens vers des rubriques supplémentaires sur les effets.

| Rubrique                                                                                                                    | Description                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Liaison de nuanceurs d’effet](effect-shader-linking.md)<br/>                                                            | Direct2D utilise une optimisation appelée liaison de nuanceur d’effet qui combine plusieurs passes de rendu de graphique d’effet dans une seule passe.<br/>                                               |
| [Effets personnalisés](custom-effects.md)<br/>                                                                          | Montre comment écrire vos propres effets personnalisés à l’aide du langage HLSL standard.<br/>                                                                                                                |
| [Comment charger une image dans des effets Direct2D à l’aide de FilePicker](load-a-id2d1image-using-the-filepicker.md)<br/> | Montre comment utiliser [**Windows :: Storage ::P ickers :: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) pour charger une image dans des effets Direct2D.<br/>                                      |
| [Guide pratique pour enregistrer le contenu Direct2D dans un fichier image](save-direct2d-content-to-an-image-file.md)<br/>                   | Cette rubrique montre comment utiliser [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) pour enregistrer du contenu sous la forme d’un [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) dans un fichier image encodé comme JPEG.<br/> |
| [Comment appliquer des effets aux primitives](how-to-apply-effects-to-primitives.md)<br/>                                  | Cette rubrique montre comment appliquer une série d’effets à des primitives [Direct2D](./direct2d-portal.md) et [DirectWrite](direct2d-and-directwrite.md) .<br/>                           |
| [Contrôle de la précision et du découpage numérique dans les graphiques d’effet](precision-and-clipping-in-effect-graphs.md)<br/>  | Les applications qui restituent des effets à l’aide de Direct2D doivent veiller à atteindre le niveau souhaité de qualité et de prévisibilité en ce qui concerne la précision numérique. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Application d’un effet à une image

Vous pouvez utiliser l’API Direct2D Effects pour appliquer des transformations aux images.

> [!Note]  
> Cet exemple suppose que vous avez déjà créé des objets [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) et [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) . Pour plus d’informations sur la création de ces objets, consultez le guide pratique [pour charger une image dans des effets Direct2D à l’aide des](load-a-id2d1image-using-the-filepicker.md) [contextes](devices-and-device-contexts.md)FilePicker et Device.

 

1.  Déclarez une variable [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , puis créez un effet de [source bitmap](bitmap-source.md) à l’aide de la méthode [**ID2DDeviceContext :: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  Définissez la propriété BitmapSource sur la source de bitmap WIC à l’aide de [**ID2D1Effect :: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Déclarez une variable [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , puis créez l’effet [flou gaussien](gaussian-blur.md) .

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  Définissez l’entrée pour recevoir l’image de l’effet de source bitmap. Définissez la valeur de flou de la méthode [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) et de la propriété d’écart type.

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  Utilisez le contexte de périphérique pour dessiner la sortie d’image résultante.

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    La méthode [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) doit être appelée entre les appels [**ID2DDeviceContext :: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) et [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) comme d’autres opérations de rendu Direct2D. **DrawImage** peut prendre une image ou la sortie d’un effet et la rendre sur la surface cible.

## <a name="spatial-transforms"></a>Transformations spatiales

Direct2D fournit des effets intégrés qui peuvent transformer les images en espace 2D et 3D, ainsi que la mise à l’échelle. Les effets de la mise à l’échelle et de la transformation offrent différents niveaux de qualité, tels que les cubiques les plus proches, linéaires, cubiques, linéaires, anisotrope et de haute qualité.

> [!Note]  
> Le mode anisotrope génère des mipmaps lors de la mise à l’échelle, toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets qui sont entrés dans la transformation, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



Cette utilisation de l’effet de transformation affine 2D fait pivoter légèrement le bitmap dans le sens inverse.



| Avant                                                            |
|-------------------------------------------------------------------|
| ![effet affin 2D avant image.](images/default-before.jpg)      |
| After                                                             |
| ![effet affin 2D après l’image.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Composition d’images

Certains effets acceptent plusieurs entrées et les composent en une image résultante.

Les effets composites composites et arithmétiques intégrés fournissent différents modes. pour plus d’informations, consultez la rubrique [composite](composite.md) . L’effet de [fusion](blend.md) offre un large éventail de modes d’accélération GPU disponibles.


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



L’effet composite combine les images de différentes manières selon le mode que vous spécifiez.

## <a name="pixel-adjustments"></a>Réglages des pixels

Certains effets Direct2D intégrés vous permettent de modifier les données de pixels. Par exemple, l’effet matrice de couleurs peut être utilisé pour modifier la couleur d’une image.


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Ce code prend l’image et modifie la couleur comme indiqué dans les exemples d’images ici.



| Avant                                                          |
|-----------------------------------------------------------------|
| ![effet de matrice de couleurs avant l’image.](images/default-before.jpg) |
| After                                                           |
| ![effet de matrice de couleurs après l’image.](images/15-colormatrix.png)  |



 

Pour plus d’informations, consultez la section [Color Built-in Effects](how-to-create-a-solid-color-brush.md) .

## <a name="building-effect-graphs"></a>Génération de graphiques d’effets

Vous pouvez regrouper des effets pour transformer des images. Par exemple, le code suivant applique une ombre et une transformation 2D, puis compose les résultats ensemble.


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Voici le résultat.

![sortie de l’effet d’ombre.](images/effect-overview-shadow.png)

Les effets prennent les objets [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) comme entrée. Vous pouvez utiliser un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , car l’interface est dérivée de **ID2D1Image**. Vous pouvez également utiliser [**ID2D1Effect :: GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) pour obtenir la sortie d’un objet [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) en tant que **ID2D1Image** ou utiliser la méthode **SetInputEffect** , qui convertit la sortie pour vous. Dans la plupart des cas, un graphique d’effet se compose d’objets **ID2D1Effect** chaînés directement ensemble, ce qui facilite l’application de plusieurs effets à une image pour créer des visuels attrayants.

Pour plus d’informations, consultez [comment appliquer des effets à des primitives](how-to-apply-effects-to-primitives.md) .

## <a name="related-topics"></a>Rubriques connexes

[Exemple d’effets d’images de base Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Effets intégrés](built-in-effects.md)