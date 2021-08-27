---
title: Effet de transformation affine 2D
description: L’effet de transformation affine 2D applique une transformation spatiale à une image basée sur une matrice matrice à l’aide de la transformation de matrice Direct2D et de l’un des six modes d’interpolation.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Effet de transformation affine 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337168db7a422a8a22785316d2af1960e3a78b2f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478095"
---
# <a name="2d-affine-transform-effect"></a>Effet de transformation affine 2D

L’effet de transformation affine 2D applique une transformation spatiale à une image basée sur une matrice matrice à l’aide de la [transformation](direct2d-transforms-overview.md) de matrice Direct2D et de l’un des six modes d’interpolation. Vous pouvez utiliser cet effet pour faire pivoter, mettre à l’échelle, incliner ou traduire une image. Vous pouvez combiner ces opérations. Les transferts affin préservent les lignes parallèles et le ratio des distances entre les trois points d’une image.

Le CLSID de cet effet est CLSID \_ D2D12DAffineTransform.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de bordure](#border-modes)
-   [Modes d’interpolation](#interpolation-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                             |
|--------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)         |
| Après                                                              |
| ![image après la transformation.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



Cet effet effectue cette opération de matrice :

![opération de matrice affine](images/affine-matrix-calculation.png)

Bien que la matrice d’entrée soit définie en tant que matrice matrice, la dernière colonne est remplie avec 0, 0 et 1 pour produire une matrice carrée. Cela permet la multiplication de matrice, afin que les transformations puissent être concaténées en une seule matrice.

## <a name="effect-properties"></a>Propriétés d’effet




| Nom complet et énumération d’index | Description | 
|------------------------------------|-------------|
| InterpolationMode<br /> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br /> | Mode d’interpolation utilisé pour mettre à l’échelle l’image. Il existe 6 modes de mise à l’échelle qui vont de la qualité et de la vitesse.<br /> Le type est D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.<br /> La valeur par défaut est D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.<br /> | 
| BorderMode<br /> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br /> | Le mode utilisé pour calculer la bordure de l’image, soft ou Hard. Pour plus d’informations, consultez <a href="https://www.bing.com/search?q=Border+modes">modes de bordure</a> . <br /> Le type est D2D1_BORDER_MODE.<br /> La valeur par défaut est D2D1_BORDER_MODE_SOFT.<br /> | 
| TransformMatrix<br /> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br /> | Matrice matrice pour transformer l’image à l’aide de la <a href="direct2d-transforms-overview.md">transformation</a>de matrice Direct2D. <br /> Le type est D2D1_MATRIX_3X2_F.<br /> La valeur par défaut est Matrix3x2F :: Identity ().<br /> | 
| Netteté<br /> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br /> | Dans le mode d’interpolation cubique de haute qualité, le niveau de netteté du filtre de mise à l’échelle est une valeur float comprise entre 0 et 1. Les valeurs sont sans unité. Vous pouvez utiliser la netteté pour ajuster la qualité d’une image lors de la mise à l’échelle de l’image.<br /> Le facteur de netteté affecte la forme du noyau. Plus le facteur de netteté est élevé, plus le noyau est petit. <br /><blockquote>[!Note]<br />Cette propriété affecte uniquement le mode d’interpolation cubique de haute qualité.</blockquote><br /> Le type est FLOAT.<br /> La valeur par défaut est 1,0 f.<br /> | 




 

## <a name="border-modes"></a>Modes de bordure



| Name                     | Description                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Mode de bordure d2d1 \_ \_ | L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure de l’interpolation, ce qui génère une bordure douce.<br/> |
| D2D1 \_ mode de bordure \_ \_ difficile | L’effet attache la sortie à la taille de l’image d’entrée. <br/>                                         |



 

## <a name="interpolation-modes"></a>Modes d’interpolation



| Énumération                                                         | Description                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode d’interpolation d2d1 2DAFFINETRANSFORM \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                                                           |
| D2D1 \_ \_ mode d’interpolation \_ 2DAFFINETRANSFORM \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ mode d' \_ interpolation \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                                                                        |
| \_Mode d’interpolation d2d1 2DAFFINETRANSFORM multi- \_ \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.                                              |
| D2D1 \_ \_ mode d’interpolation \_ 2DAFFINETRANSFORM \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                                                                     |
| D2D1 \_ 2DAFFINETRANSFORM \_ mode d’interpolation de \_ \_ haute \_ qualité \_ cubique  | Utilise un noyau cubique de haute qualité variable pour effectuer une pré-réduire de l’image si downscaling est impliqué dans la matrice de transformation. Utilise ensuite le mode d’interpolation cubique pour la sortie finale. |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ 2DAFFINETRANSFORM \_ interpolation \_ mode \_ Linear.

 

> [!Note]  
> Le mode anisotrope génère des mipmaps lors de la mise à l’échelle. Toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets entrés dans cet effet, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.

 

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de l’image bitmap de sortie dépend de la matrice de transformation appliquée à l’image.

L’effet exécute l’opération de transformation, puis applique un cadre englobant autour du résultat. La bitmap de sortie correspond à la taille du cadre englobant.

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

 

