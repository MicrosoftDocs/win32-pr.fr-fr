---
title: Effet de vignette
description: Utilisez l’effet de vignette pour répéter la région spécifiée de l’image.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- effet de vignette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032940"
---
# <a name="tile-effect"></a>Effet de vignette

Utilisez l’effet de vignette pour répéter la région spécifiée de l’image.

Le CLSID de cet effet est CLSID \_ D2D1Tile.

## <a name="example-image"></a>Exemple d’image



| Avant                                                     |
|------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg) |
| After                                                      |
| ![image après la transformation.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                | Type et valeur par défaut                                              | Description                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1 de \_ vignette \_ prop \_ Rect<br/> | D2D1 \_ vecteur \_ 4F<br/> {0.0 f, 0.0 f, 100,0 f, 100,0 f}<br/> | Zone de l’image à présenter en mosaïque. Cette propriété est un \_ vecteur d2d1 \_ 4F défini comme suit : (gauche, haut, droite, bas). Les unités sont en DIP.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de sortie

Cet effet génère une image bitmap de taille infinie logiquement.

Vous pouvez juxtaposer une image et générer une certaine taille sans effets supplémentaires en définissant la taille quand vous appelez [**ID2D1DeviceContext ::D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).

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

 

