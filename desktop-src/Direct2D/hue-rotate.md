---
title: Effet de rotation de la teinte
description: Utilisez l’effet rotation de la teinte pour modifier la teinte d’une image en appliquant une matrice de couleurs en fonction de l’angle de rotation.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- effet de rotation de la teinte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104554878"
---
# <a name="hue-rotatation-effect"></a>Effet de rotation de la teinte

Utilisez l’effet rotation de la teinte pour modifier la teinte d’une image en appliquant une matrice de couleurs en fonction de l’angle de rotation.

Le CLSID de cet effet est CLSID \_ D2D1HueRotation.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’exemple ci-dessous montre les images d’entrée et de sortie de l’effet de rotation de la teinte avec un angle de rotation de 270 degrés.



| Avant                                                       |
|--------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)   |
| After                                                        |
| ![image après la transformation.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



L’effet calcule une matrice de couleurs en fonction de l’angle de rotation (*?*) que vous spécifiez avec la \_ propriété d2d1 HUEROTATION \_ prop \_ angle. Voici les équations de matrice.

![calculs de rotation de teinte](images/hue-formula.png)

La matrice créée dépend uniquement de l’angle de rotation. Vous pouvez utiliser l’effet [matrice de couleurs](color-matrix.md) si vous avez besoin d’une matrice spécifique.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                         | Type et valeur par défaut           | Description                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| Angle<br/> \_Angle d2d1 HUEROTATION \_ prop \_<br/> | FLOAT<br/> 0.0f<br/> | Angle de rotation de la teinte, en degrés. |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de la bitmap de sortie est la même que la taille de la bitmap d’entrée.

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

 

