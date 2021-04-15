---
title: Effet de transformation 3D
description: Utilisez l’effet Transformation 3D pour appliquer une matrice de transformation 4x4 arbitraire à une image.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- transformation 3D, effet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104555569"
---
# <a name="3d-transform-effect"></a>Effet de transformation 3D

Utilisez l’effet Transformation 3D pour appliquer une matrice de transformation 4x4 arbitraire à une image.

Cet effet applique la matrice (M ?) que vous fournissez aux sommets d’angle de l’image source ( \[ x y z 1 \] ) à l’aide de ce calcul :

\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M ?

Le CLSID de cet effet est CLSID \_ D2D13DTransform.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
    -   [Modes d’interpolation](#interpolation-modes)
    -   [Modes de bordure](#border-modes)
-   [Classe de matrice de transformation 4x4](#4x4-transform-matrix-class)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                        |
|---------------------------------------------------------------|
| ![image avant la transformation.](images/default-before.jpg) |
| After                                                         |
| ![image après la transformation.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



<table>
<thead>
<tr class="header">
<th>Nom complet et énumération d’index</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>Mode d’interpolation utilisé par l’effet sur l’image. Il existe 5 modes de mise à l’échelle qui vont de la qualité et de la vitesse.<br/> Le type est D2D1_3DTRANSFORM_INTERPOLATION_MODE.<br/> La valeur par défaut est D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>BorderMode<br/> D2D1_3DTRANSFORM_PROP_BORDER_MODE<br/></td>
<td>Le mode utilisé pour calculer la bordure de l’image, soft ou Hard. Pour plus d’informations, consultez <a href="https://www.bing.com/search?q=Border+modes">modes de bordure</a> .<br/> Le type est D2D1_BORDER_MODE.<br/> La valeur par défaut est D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Matrice de transformation 4x4 appliquée au plan de projection. Le calcul de matrice suivant est utilisé pour mapper des points d’un système de coordonnées 3D au système de coordonnées 2D transformé. <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" />Où :<dl> X, Y, Z = coordonnées du plan de projection d’entrée<br />
M<sub>x, y</sub> = transformer les éléments de la matrice<br />
X, Y, Z = coordonnées du plan de projection de sortie<br />
</dl> <br/> Les éléments de matrice individuels ne sont pas limités et sont sans unité. <br/> Le type est D2D1_MATRIX_4X4_F.<br/> La valeur par défaut est Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1).<br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a>Modes d’interpolation



| Énumération                                                   | Description                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode d’interpolation d2d1 3DTRANSFORM \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                 |
| D2D1 \_ \_ mode d’interpolation \_ 3DTRANSFORM \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure. |
| D2D1 \_ 3DTRANSFORM \_ mode d' \_ interpolation \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                              |
| \_Mode d’interpolation d2d1 3DTRANSFORM multi- \_ \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.    |
| D2D1 \_ \_ mode d’interpolation \_ 3DTRANSFORM \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                           |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ 3DTRANSFORM \_ interpolation \_ mode \_ Linear.

 

> [!Note]  
> Le mode anisotrope génère des mipmaps lors de la mise à l’échelle. Toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets entrés dans cet effet, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.

 

### <a name="border-modes"></a>Modes de bordure



| Nom                     | Description                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Mode de bordure d2d1 \_ \_ | L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure de l’interpolation, ce qui génère une bordure douce.<br/> |
| D2D1 \_ mode de bordure \_ \_ difficile | L’effet attache la sortie à la taille de l’image d’entrée. <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a>Classe de matrice de transformation 4x4

Direct2D fournit une classe de matrice 4x4 pour fournir des fonctions d’assistance pour transformer l’image en 3 dimensions. Pour plus d’informations et pour obtenir une description de tous les membres de la classe, consultez la rubrique [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) .



| Fonction                                | Description                                                                                    | Matrix                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Matrix4x4F :: Scale (X, Y, Z)              | Génère une matrice de transformation qui met à l’échelle le plan de projection dans la direction X, Y et/ou Z. | ![matrice scale3d](images/3d-transform-matrix2.png)     |
| SkewX (X)                                | Génère une matrice de transformation qui incline le plan de projection dans l’axe X.               | ![Affiche une matrice inclinée sur l’axe X.](images/matrix4x4-skewx.png)             |
| Skew (Y)                                | Génère une matrice de transformation qui incline le plan de projection sur l’axe Y.               | ![matrice d’inclinaison](images/matrix4x4-skewy.png)             |
| Translation (X, Y, Z)                    | Génère une matrice de transformation qui convertit le plan de projection dans la direction X, Y ou Z. | ![translater la matrice](images/3d-transform-matrix4.png)   |
| RotationX (X)                            | Génère une matrice de transformation qui fait pivoter le plan de projection autour de l’axe X.               | ![faire pivoter la matrice x](images/3d-transform-matrix5.png)    |
| RotationY (Y)                            | Génère une matrice de transformation qui fait pivoter le plan de projection autour de l’axe Y.               | ![faire pivoter la matrice y](images/3d-transform-matrix6.png)    |
| Rotationt (Z)                            | Génère une matrice de transformation qui fait pivoter le plan de projection autour de l’axe Z.               | ![pivoter la matrice z](images/3d-transform-matrix7.png)    |
| PerspectiveProjection (D)                | Transformation de perspective avec une valeur de profondeur D.                                          | ![matrice de perspective](images/3d-transform-matrix8.png) |
| RotationArbitraryAxis (X, Y, Z, degrés) | Fait pivoter le plan de projection autour de l’axe que vous spécifiez.                                       |                                                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| Serveur minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

