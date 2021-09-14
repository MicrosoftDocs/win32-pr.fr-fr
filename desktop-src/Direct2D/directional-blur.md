---
title: Effet flou directionnel
description: L’effet de flou directionnel est semblable au flou gaussien, sauf que vous pouvez incliner le flou dans une direction particulière.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- flou directionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113282"
---
# <a name="directional-blur-effect"></a>Effet flou directionnel

L’effet de flou directionnel est semblable au [flou gaussien](gaussian-blur.md), sauf que vous pouvez incliner le flou dans une direction particulière. Vous pouvez utiliser cet effet pour donner à une image l’apparence si elle est en mouvement ou pour mettre en évidence une image animée.

Le CLSID de cet effet est CLSID \_ D2D1DirectionalBlur.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Modes d’optimisation](#optimization-modes)
-   [Modes de bordure](#border-modes)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                          |
|-----------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)      |
| After                                                           |
| ![image après la transformation.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> ÉCART type de D2D1 \_ DIRECTIONALBLUR \_ prop \_ \_<br/> | Quantité de flou à appliquer à l’image. Vous pouvez calculer le rayon de flou du noyau en multipliant l’écart type par 3. Les unités de l’écart type et du rayon de flou sont des DIP. La valeur 0 DIP désactive cet effet. Le type est FLOAT.<br/> La valeur par défaut est 3.0 f.<br/>                                                                            |
| Angle<br/> \_Angle d2d1 DIRECTIONALBLUR \_ prop \_<br/>                           | Angle du flou par rapport à l’axe x, dans le sens inverse des aiguilles d’une passe. Les unités sont spécifiées en degrés.<br/> Le noyau de flou est d’abord généré à l’aide du même processus que pour l’effet [flou gaussien](gaussian-blur.md) . Les valeurs de noyau sont ensuite transformées en fonction de l’angle de flou.<br/> Le type est FLOAT.<br/> La valeur par défaut est 0.0 f.<br/> |
| Optimization<br/> Optimisation de D2D1 \_ DIRECTIONALBLUR \_ prop \_<br/>             | Mode d’optimisation. Pour plus d’informations, consultez [modes d’optimisation](#optimization-modes) .<br/> Le type est D2D1 \_ DIRECTIONALBLUR \_ Optimization.<br/> La valeur par défaut est D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced. <br/>                                                                                                                                                         |
| BorderMode<br/> \_Mode de bordure d2d1 DIRECTIONALBLUR \_ prop \_ \_<br/>               | Le mode utilisé pour calculer la bordure de l’image, soft ou Hard. Pour plus d’informations, consultez [modes de bordure](#border-modes) .<br/> Le type est D2D1 \_ Border \_ mode.<br/> La valeur par défaut est \_ d2d1 \_ en mode bordure \_ souple.<br/>                                                                                                                                                                 |



 

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

La taille de la bitmap de sortie augmente en fonction de l’écart type, de l’angle de l’effet et du mode de bordure. Si le mode de bordure est défini sur le \_ mode de bordure d2d1 \_ \_ , la taille de la bitmap de sortie augmente de la taille du noyau de flou, représentée en pixels. Ces équations peuvent être utilisées pour calculer la taille de l’image bitmap de sortie.



| Condition requise | Valeur |
|------------------------|-------------------------------------------------------------------|
| Croissance bitmap en sortie X | StandardDeviation (DIP) \* 6 \* ((PPP utilisateur)/96) \* cos (angle)) |
| Croissance des bitmaps en sortie Y | StandardDeviation (DIP) \* 6 \* ((PPP utilisateur)/96) \* Sin (angle)) |



 

## <a name="requirements"></a>Spécifications



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

 

