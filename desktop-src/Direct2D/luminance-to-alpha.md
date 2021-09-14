---
title: Effet luminance vers alpha
description: Utilisez l’effet luminance pour Alpha pour définir le canal alpha sur la luminance de l’image et définir les canaux de couleur sur 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- effet luminance vers alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112658"
---
# <a name="luminance-to-alpha-effect"></a>Effet luminance vers alpha

Utilisez l’effet luminance pour Alpha pour définir le canal alpha sur la luminance de l’image et définir les canaux de couleur sur 0. Vous pouvez utiliser la sortie de cet effet pour créer une superposition translucide en fonction de la luminosité de l’image d’entrée. Ou vous pouvez l’utiliser pour créer un masque d’image.

> [!Note]  
> Cet effet n’a pas de propriétés.

 

Le CLSID de cet effet est CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Exemple d’image

Cet exemple montre la sortie de l’effet luminance vers alpha composite sur une surface blanche pour afficher l’opacité.



| Avant                                                            |
|-------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)        |
| Après                                                             |
| ![image après la transformation.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Cet effet définit le canal alpha de la sortie sur la luminance de l’image d’entrée à l’aide de cette matrice de couleurs.

![matrice de couleurs utilisée par l’effet pour définir le canal alpha.](images/luminance-to-alpha-math1.png)

Cet effet consomme et génère des images alpha prémultipliées. L’effet ne fonctionne pas sur les images alpha directes, sauf si elles sont entièrement opaques.

> [!Note]
>
> Étant donné que les images sont stockées dans un format compensé gamma, avant de calculer la luminance pour une image, vous devez d’abord effectuer une correction gamma inverse pour obtenir les valeurs de couleur vraies pour l’image. Étant donné que les images sont normalement stockées à 2,2 de gamma, vous pouvez utiliser l’effet de transfert gamma avec un exposant de (1/2.2), puis utiliser la sortie de cet effet.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La sortie a la même taille que l’image d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
