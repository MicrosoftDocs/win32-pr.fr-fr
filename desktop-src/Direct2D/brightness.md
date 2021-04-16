---
title: Effet de luminosité
description: Utilisez l’effet luminosité pour contrôler la luminosité de l’image.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- effet de luminosité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104558921"
---
# <a name="brightness-effect"></a>Effet de luminosité

Utilisez l’effet luminosité pour contrôler la luminosité de l’image.

Le CLSID de cet effet est CLSID \_ D2D1Brightness.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Bitmap de sortie](#output-bitmap)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                      |
|-------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)  |
| After                                                       |
| ![image après la transformation.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet de la propriété                                                 | Type et valeur par défaut                              | Description                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WhitePoint<br/> \_ \_ \_ Point blanc du prop \_ d2d1 de la luminosité<br/> | \_Vecteur d2d1 \_ 2F<br/> {1.0 f, 1.0 f}<br/> | Partie supérieure de la courbe de transfert de luminosité. Le point blanc ajuste l’apparence des parties plus claires de l’image. Cette propriété est pour la valeur x et la valeur y, dans cet ordre. Chacune des valeurs de cette propriété est comprise entre 0 et 1 inclus. |
| BlackPoint<br/> \_ \_ \_ Point noir du prop \_ d2d1 de luminosité<br/> | \_Vecteur d2d1 \_ 2F<br/> {0.0 f, 0.0 f}<br/> | La partie inférieure de la courbe de transfert de luminosité. Le point noir ajuste l’apparence des parties plus sombres de l’image. Cette propriété est pour la valeur x et la valeur y, dans cet ordre. Chacune des valeurs de cette propriété est comprise entre 0 et 1 inclus.   |



 

Cet effet utilise les points noir et blanc spécifiés pour générer une fonction de transfert utilisée pour ajuster l’image bitmap. L’équation suivante décrit la fonction de transfert. Les intensités d’entrée sont définies entre 0 et 1.

![algorithme de luminosité](images/brightness-formula1.png)

L’algorithme Effect implémente une équation qui crée la fonction de transfert. Nous utilisons cette fonction pour ajuster les pixels de l’image. Les valeurs x et y du point noir et du point blanc sont les coordonnées dans deux dimensions qui sont connectées pour former la transformation. Chaque partie de l’équation de sortie finale :

1.  Convertit les données d’image de l’espace linéaire en espace non linéaire à l’aide de cette équation :![fonction d’assistance 1](images/brightness-formula2.png)

2.  Ajuste l’image en fonction de ces valeurs :
    -   l' *entrée* correspond aux valeurs d’intensité en pixels de l’image d’entrée de 0 à 1.

    -   *PT blanc (x, y)* emplacement de la courbe de transformation pour des intensités de pixel plus claires.

    -   Le *point noir (x, y)* est l’emplacement de la courbe de transformation pour les intensités de pixel DIMM.

3.  Reconvertit les données de l’image en espace linéaire à l’aide de cette équation : ![fonction d’assistance 2](images/brightness-formula3.png)

L’équation de sortie finale et les parties de composant sont indiquées ici.

![calculs complets pour l’ajustement de la luminosité](images/brightness-formula4.png)

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

 

