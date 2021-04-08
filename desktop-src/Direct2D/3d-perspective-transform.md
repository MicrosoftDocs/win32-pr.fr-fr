---
title: Effet de transformation de perspective 3D
description: Utilisez l’effet transformation de perspective 3D pour faire pivoter l’image en 3 dimensions comme si elle était affichée à partir d’une distance.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- effet transformation de perspective 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844426"
---
# <a name="3d-perspective-transform-effect"></a>Effet de transformation de perspective 3D

Utilisez l’effet transformation de perspective 3D pour faire pivoter l’image en 3 dimensions comme si elle était affichée à partir d’une distance.

La transformation de perspective 3D est plus pratique que l’effet de transformation 3D, mais expose uniquement un sous-ensemble de la fonctionnalité. Vous pouvez calculer une matrice de transformation 3D complète et appliquer une matrice de transformation plus arbitraire à une image à l’aide de l’effet [transformation 3D](3d-transform.md) .

Le CLSID de cet effet est CLSID \_ D2D13DPerspectiveTransform.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes d’interpolation](#interpolation-modes)
-   [Modes de bordure](#border-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                               |
|----------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)           |
| After                                                                |
| ![image après l’effet.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                              | Description                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> \_Mode d’interpolation d2d1 3DPERSPECTIVETRANSFORM \_ prop \_ \_<br/> | Mode d’interpolation utilisé par l’effet sur l’image. Il existe 5 modes de mise à l’échelle qui vont de la qualité et de la vitesse.<br/> Le type est D2D1 \_ 3DPERSPECTIVETRANSFORM \_ interpolation \_ mode.<br/> La valeur par défaut est D2D1 \_ 3DPERSPECTIVETRANSFORM \_ interpolation \_ mode \_ Linear.<br/>              |
| BorderMode<br/> \_Mode de bordure d2d1 3DPERSPECTIVETRANSFORM \_ prop \_ \_<br/>               | Le mode utilisé pour calculer la bordure de l’image, soft ou Hard. Pour plus d’informations, consultez [modes de bordure](https://www.bing.com/search?q=Border+modes) .<br/> Le type est D2D1 \_ Border \_ mode.<br/> La valeur par défaut est D2D1 \_ mode de bordure \_ \_ souple.<br/>                                                              |
| Profondeur<br/> \_Profondeur d2d1 3DPERSPECTIVETRANSFORM \_ prop \_<br/>                           | Distance entre le *PerspectiveOrigin* et le plan de projection. La valeur spécifiée dans DIP et doit être supérieure à 0.<br/> Le type est FLOAT.<br/> La valeur par défaut est 1000.0 f.<br/>                                                                                               |
| PerspectiveOrigin<br/> Origine de la \_ perspective d2d1 3DPERSPECTIVETRANSFORM \_ prop \_ \_<br/> | L’emplacement X et Y de la visionneuse dans la scène 3D. Cette propriété est un \_ vecteur d2d1 \_ 2F défini en tant que : (point X, point Y). Les unités sont en DIP.<br/> Vous définissez la valeur Z avec la propriété *Depth* .<br/> Le type est D2D1 \_ Vector \_ 2F.<br/> La valeur par défaut est {0.0 f, 0.0 f}.<br/> |
| LocalOffset<br/> Décalage local de D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ \_<br/>             | Translation que l’effet effectue avant de faire pivoter le plan de projection. Cette propriété est un \_ vecteur d2d1 \_ 3F défini en tant que : (X, Y, Z). Les unités sont en DIP.<br/> Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.<br/>                                        |
| GlobalOffset<br/> \_ \_ \_ Décalage global d2d1 3DPERSPECTIVETRANSFORM \_ prop<br/>           | Translation que l’effet effectue après avoir fait pivoter le plan de projection. Cette propriété est un \_ vecteur d2d1 \_ 3F défini en tant que : (X, Y, Z). Les unités sont en DIP.<br/> Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.<br/>                                         |
| RotationOrigin<br/> \_Origine de rotation d2d1 3DPERSPECTIVETRANSFORM \_ prop \_ \_<br/>       | Point central de la rotation effectuée par l’effet. Cette propriété est un \_ vecteur d2d1 \_ 3F défini en tant que : (X, Y, Z). Les unités sont en DIP.<br/> Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.<br/>                                                            |
| Rotation<br/> \_Rotation d2d1 3DPERSPECTIVETRANSFORM \_ prop \_<br/>                     | Angles de rotation pour chaque axe. Cette propriété est un \_ vecteur d2d1 \_ 3F défini en tant que : (X, Y, Z). Les unités sont en degrés.<br/> Le type est D2D1 \_ Vector \_ 3F.<br/> La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.<br/>                                                                         |



 

## <a name="interpolation-modes"></a>Modes d’interpolation



| Énumération                                                              | Description                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode d’interpolation d2d1 3DPERSPECTIVETRANSFORM \_ \_ \_ le plus proche \_ voisin     | Échantillonne le point unique le plus proche et l’utilise. Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.                                 |
| D2D1 \_ \_ mode d’interpolation \_ 3DPERSPECTIVETRANSFORM \_ linéaire                | Utilise un échantillon à quatre points et une interpolation linéaire. Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure. |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ mode d' \_ interpolation \_ cubique                 | Utilise un exemple de noyau cubique 16 pour l’interpolation. Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.                              |
| \_Mode d’interpolation d2d1 3DPERSPECTIVETRANSFORM multi- \_ \_ \_ \_ exemple \_ linéaire | Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage. Ce mode est adapté à la réduction de la taille des images avec quelques pixels.    |
| D2D1 \_ \_ mode d’interpolation \_ 3DPERSPECTIVETRANSFORM \_ anisotrope           | Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.                                                           |



 

> [!Note]  
> Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ 3DPERSPECTIVETRANSFORM \_ interpolation \_ mode \_ Linear.

 

> [!Note]  
> Le mode anisotrope génère des mipmaps lors de la mise à l’échelle. Toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets entrés dans cet effet, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.

 

## <a name="border-modes"></a>Modes de bordure



| Nom                     | Description                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Mode de bordure d2d1 \_ \_ | L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure de l’interpolation, ce qui génère une bordure douce.<br/> |
| D2D1 \_ mode de bordure \_ \_ difficile | L’effet attache la sortie à la taille de l’image d’entrée. <br/>                                         |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de l’image bitmap de sortie dépend de la matrice de transformation appliquée à l’image.

L’effet exécute l’opération de transformation, puis applique un cadre englobant autour du résultat. La bitmap de sortie correspond à la taille du cadre englobant.

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

 

