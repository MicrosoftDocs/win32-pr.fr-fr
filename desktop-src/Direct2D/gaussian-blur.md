---
title: Effet Flou gaussien
description: Utilisez l’effet Flou gaussien pour créer un flou basé sur la fonction Gaussiente sur l’image d’entrée entière.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Flou gaussien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104554224"
---
# <a name="gaussian-blur-effect"></a>Effet Flou gaussien

Utilisez l’effet Flou gaussien pour créer un flou basé sur la fonction Gaussiente sur l’image d’entrée entière.

Vous pouvez utiliser cet effet pour créer des lueurs et des ombres portées et utiliser l’effet [composite](composite.md) pour appliquer le résultat à l’image d’origine. Il est utile dans le traitement des photos pour les filtres tels que les clairs et les ombres. Vous pouvez utiliser la sortie de cet effet pour l’entrée dans les effets d’éclairage, comme les effets d’éclairage [spéculaire](specular-lighting.md) ou d' [éclairage diffus](diffuse-lighting.md) , car le canal alpha est flou, et les effets d’éclairage utilisent le canal alpha pour déterminer la géométrie de surface comme une carte de hauteur.

Cet effet est utilisé par l’effet d' [ombre](drop-shadow.md) intégré.

Le CLSID de cet effet est CLSID \_ D2D1GaussianBlur.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes d’optimisation](#optimization-modes)
-   [Modes de bordure](#border-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                       |
|--------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)   |
| After                                                        |
| ![image après la transformation.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                    | Description                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> ÉCART type de D2D1 \_ GAUSSIANBLUR \_ prop \_ \_<br/> | Quantité de flou à appliquer à l’image. Vous pouvez calculer le rayon de flou du noyau en multipliant l’écart type par 3. Les unités de l’écart type et du rayon de flou sont des DIP. Une valeur de zéro DIP désactive entièrement cet effet. Le type est FLOAT.<br/> La valeur par défaut est 3.0 f.<br/> |
| Optimization<br/> Optimisation de D2D1 \_ GAUSSIANBLUR \_ prop \_<br/>             | Mode d’optimisation. Pour plus d’informations, consultez [modes d’optimisation](#optimization-modes) . Le type est D2D1 \_ GAUSSIANBLUR \_ Optimization.<br/> La valeur par défaut est D2D1 \_ GAUSSIANBLUR \_ Optimization \_ Balanced.<br/>                                                                                                            |
| BorderMode<br/> \_Mode de bordure d2d1 GAUSSIANBLUR \_ prop \_ \_<br/>               | Le mode utilisé pour calculer la bordure de l’image, soft ou Hard. Pour plus d’informations, consultez [modes de bordure](#border-modes) . <br/> Le type est D2D1 \_ GAUSSIANBLUR \_ Border \_ mode.<br/> La valeur par défaut est \_ d2d1 \_ en mode bordure \_ souple.<br/>                                                                                   |



 

## <a name="optimization-modes"></a>Modes d’optimisation



| Nom                                          | Description                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Vitesse d’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_    | Applique des optimisations internes telles que la pré-mise à l’échelle à des rayons relativement petits. Utilise le filtrage linéaire.                                  |
| D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced | Utilise les mêmes seuils d’optimisation que le mode vitesse, mais utilise le filtrage trilinéaire.                                                    |
| Qualité de l’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_  | Utilise uniquement des optimisations internes avec de grands rayons de flou, où les approximations sont moins susceptibles d’être visibles. Utilise le filtrage trilinéaire. |



 

## <a name="border-modes"></a>Modes de bordure



| Nom                     | Description                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Mode de bordure d2d1 \_ \_ | L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure qu’elle applique le noyau de flou, entraînant ainsi un contour adouci. <br/>                                                                                             |
| D2D1 \_ mode de bordure \_ \_ difficile | L’effet attache la sortie à la taille de l’image d’entrée. Lorsque l’effet applique le noyau de flou, il étend l’image d’entrée avec une transformation de bordure de type miroir pour les exemples en dehors des limites d’entrée.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La sortie de cet effet peut être supérieure à la bitmap d’entrée en fonction du rayon de flou et du mode de bordure. Si le mode de bordure est défini sur \_ d2d1 \_ en mode bordure \_ , les Ille de la sortie bitmap augmentent de la taille du noyau de flou, représentée en pixels. Ce tableau fournit une équation que vous pouvez utiliser pour calculer la bitmap de sortie.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Par conséquent, si la taille de l’image augmente de 10 pixels dans chaque direction, l’angle supérieur gauche de l’image sera situé à (-5,-5), tandis que le coin inférieur droit sera (105, 105).

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

 

