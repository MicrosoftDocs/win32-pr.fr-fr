---
title: Effet d’ombre
description: Utilisez l’effet d’ombre pour générer une ombre à partir du canal alpha d’une image.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- effet d’ombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d88924140caac22b688a0ccb6948ee74312411c770bff99360847ef2cd1b4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833048"
---
# <a name="shadow-effect"></a>Effet d’ombre

Utilisez l’effet d’ombre pour générer une ombre à partir du canal alpha d’une image. L’ombre est plus opaque pour les valeurs alpha supérieures et plus transparente pour les valeurs alpha inférieures. Vous pouvez définir la quantité de flou et la couleur de l’ombre.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes d’optimisation](#optimization-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

Le CLSID de cet effet est CLSID \_ D2D1Shadow.

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre la sortie de l’effet d’ombre qui est traduite par l’image source composite au niveau de l’emplacement d’origine. L’effet d’ombre génère uniquement l’ombre.



| Avant                                                  |
|---------------------------------------------------------|
| ![image avant l’effet.](images/8-crop.png)      |
| Après                                                   |
| ![image après la transformation.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BlurStandardDeviation<br/> \_ \_ \_ Écart type de flou \_ \_ de l’ombre d2d1<br/> | Quantité de flou à appliquer au canal alpha de l’image. Vous pouvez calculer le rayon de flou du noyau en multipliant l’écart type par 3. Les unités de l’écart type et du rayon de flou sont des DIP.<br/> Cette propriété est la même que la propriété d’écart type [flou gaussien](gaussian-blur.md) . <br/> Le type est FLOAT.<br/> La valeur par défaut est 3.0 f.<br/> |
| Couleur<br/> Couleur de l' \_ ombre d2d1 \_ \_<br/>                                     | Couleur de l'ombre portée. Cette propriété est un \_ vecteur d2d1 \_ 4F défini en tant que : (R, G, B, a). Vous devez spécifier cette couleur dans l’alpha simple.<br/> Le type est D2D1 \_ Vector \_ 4F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f, 1.0 f}.<br/>                                                                                                                                                                     |
| Optimization<br/> Optimisation de la D2D1 des \_ clichés instantanés \_ \_<br/>                       | Niveau d’optimisation des performances.<br/> Le type est D2D1 \_ Shadow \_ Optimization.<br/> La valeur par défaut est D2D1 l’optimisation de l' \_ ombre Shadow \_ \_ .<br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a>Modes d’optimisation



| Nom                                          | Description                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Vitesse d’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_    | Applique des optimisations internes telles que la pré-mise à l’échelle à des rayons relativement petits. Utilise le filtrage linéaire.                                  |
| D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced | Utilise les mêmes seuils d’optimisation que le mode vitesse, mais utilise le filtrage trilinéaire.                                                    |
| Qualité de l’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_  | Utilise uniquement des optimisations internes avec de grands rayons de flou, où les approximations sont moins susceptibles d’être visibles. Utilise le filtrage trilinéaire. |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de la bitmap de sortie est la taille de la sortie de flou. L’importance de la croissance de la bitmap de sortie par rapport à la bitmap d’origine peut être calculée à l’aide de l’équation suivante :

Croissance des bitmaps en sortie (X et Y) = BlurStandardDeviation (DIP (Device-Independent Pixel)) \* 6 \* (dpi utilisateur)/96

La sortie augmente uniformément dans tout le sens, par exemple si la taille augmente de 10 pixels dans chaque direction, l’angle supérieur gauche de la bitmap se trouve à (-5,-5) et le coin inférieur droit est (105, 105) comme indiqué dans le diagramme ici.

![diagramme de croissance de la taille de sortie de l’effet d’ombre.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

