---
title: Effet de bordure
description: Utilisez l’effet de bordure pour étendre une image à partir des bords.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- effet de bordure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce125a96730ee59f63b18cfd1a08abd2432af6f3fdc6b5f06cfc2e9272a7a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928991"
---
# <a name="border-effect"></a>Effet de bordure

Utilisez l’effet de bordure pour étendre une image à partir des bords. Vous pouvez utiliser cet effet pour répéter les pixels à partir des bords de l’image, habiller les pixels de l’extrémité opposée de l’image ou mettre en miroir les pixels sur la bordure de l’image bitmap pour étendre la région de la bitmap.

Le CLSID de cet effet est CLSID \_ D2D1Border.

## <a name="example-images"></a>Exemples d’images

Les exemples ci-dessous illustrent la sortie de l’effet de bordure à l’aide de chaque mode. La taille de sortie est infinie, mais ces exemples d’images sont rognés à deux fois la taille.

### <a name="mirror"></a>Miroir



| Avant                                                    |
|-----------------------------------------------------------|
| ![Capture d’écran qui affiche l’image avant l’effet.](images/border-before.jpg) |
| Après                                                     |
| ![Capture d’écran qui montre l’image après la transformation.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Avant                                                        |
|---------------------------------------------------------------|
| ![Capture d’écran qui montre l’image avant l’effet d’une bride.](images/border-before.jpg)     |
| Après                                                         |
| ![Capture d’écran qui montre l’image après la transformation d’une bride.](images/10-border-clamp.png) |



 

### <a name="wrap"></a>Encapsuler



| Avant                                                       |
|--------------------------------------------------------------|
| ![Capture d’écran qui montre l’image avant l’effet d’un retour à la ligne.](images/border-before.jpg)    |
| Après                                                        |
| ![Capture d’écran qui montre l’image après la transformation d’un retour à la ligne.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                  | Description                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode bord X<br/> D2D1 \_ bordure \_ prop \_ \_ en mode Edge \_ X<br/> | Mode de bord dans la direction X de l’effet. Vous pouvez définir cette valeur sur clamp, Wrap ou Mirror. Pour plus d’informations, consultez [modes de bord](#edge-modes) .<br/> Le type est D2D1 \_ \_ Edge bord \_ mode.<br/> La valeur par défaut est \_ d2d1 \_ en mode bord de bordure \_ \_ .<br/> |
| Mode bord Y<br/> D2D1 \_ frontière \_ prop \_ \_ en mode Edge \_ Y<br/> | Mode de bord dans l’axe Y de l’effet. Vous pouvez définir cette valeur sur clamp, Wrap ou Mirror. Pour plus d’informations, consultez [modes de bord](#edge-modes) .<br/> Le type est D2D1 \_ \_ Edge bord \_ mode.<br/> La valeur par défaut est \_ d2d1 \_ en mode bord de bordure \_ \_ .<br/> |



 

## <a name="edge-modes"></a>Modes de bord



| Nom complet et énumération d’index                            | Description                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> D2D1 de \_ mode de bordure de \_ bord \_ \_<br/>   | Répète les pixels à partir des bords de l’image.      |
| Encapsuler<br/> D2D1 le \_ mode de bordure de \_ bord \_ \_<br/>     | Utilise des pixels du bord de fin opposé de l’image. |
| Miroir<br/> D2D1 \_ en \_ mode Edge frontière \_ \_<br/> | Reflète les pixels sur le bord de l’image.         |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de la bitmap de sortie est infinie pour toutes les entrées, à l’exception d’une image d’entrée de 0 taille. Si la hauteur ou la largeur d’une image d’entrée est égale à 0, la taille de sortie est 0.

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

 

