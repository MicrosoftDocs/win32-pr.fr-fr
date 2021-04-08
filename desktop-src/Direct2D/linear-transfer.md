---
title: Effet de transfert linéaire
description: Utilisez l’effet de transfert linéaire pour mapper les intensités de couleur d’une image à l’aide d’une fonction linéaire créée à partir d’une liste de valeurs que vous fournissez pour chaque canal.
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- effet de transfert linéaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfedbb79f057ee871ce23cc086034afc3e6cdda0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743948"
---
# <a name="linear-transfer-effect"></a>Effet de transfert linéaire

Utilisez l’effet de transfert linéaire pour mapper les intensités de couleur d’une image à l’aide d’une fonction linéaire créée à partir d’une liste de valeurs que vous fournissez pour chaque canal.

Le CLSID de cet effet est CLSID \_ D2D1LinearTransfer.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image



| Avant                                                          |
|-----------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)      |
| After                                                           |
| ![image après la transformation.](images/13-lineartransfer.png) |



 


```C++
ComPtr<ID2D1Effect> linearTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LinearTransfer, &linearTransferEffect);

linearTransferEffect->SetInput(0, bitmap);

linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_SLOPE, 2.5f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE, 5.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(linearTransferEffect.Get());
m_d2dContext->EndDraw();
```



La fonction de transfert linéaire est créée en fonction de la pente et de l’intersection y pour chaque canal que vous spécifiez. L’intensité en pixels en sortie C est calculée avec l’équation : C' = mC + B, où m est la pente de la fonction linéaire et B est l’interception Y de la fonction linéaire.

Cet effet fonctionne sur les images alpha directes et prémultipliées. L’effet génère des bitmaps alpha prémultipliés.

## <a name="effect-properties"></a>Propriétés d’effet

> [!Note]  
> Pour tous les canaux des propriétés de transfert linéaire :
>
> -   L’interception Y n’est pas limitée et est sans unité.
> -   La pente n’est pas limitée et est sans unité.

 



| Nom complet et énumération d’index                                                    | Type et valeur par défaut           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ rouge \_ Y d' \_ intersection<br/>     | FLOAT<br/> 0.0f<br/> | L’interception Y de la fonction linéaire pour le canal rouge.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RedSlope<br/> \_ \_ \_ Pente rouge d2d1 LINEARTRANSFER \_ prop<br/>                 | FLOAT<br/> supérieures<br/> | Pente de la fonction linéaire pour le canal rouge.                                                                                                                                                                                                                                                                                                                                                                                                         |
| RedDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ rouge \_ Disable<br/>             | BOOL<br/> FALSE<br/> | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal rouge. Si vous affectez la valeur FALSe, l’effet applique la fonction RedLinearTransfer au canal rouge.                                                                                                                                                                                                                                                                    |
| GreenYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ vert \_ Y \_ intersection<br/> | FLOAT<br/> 0.0f<br/> | L’interception Y de la fonction linéaire pour le canal vert.                                                                                                                                                                                                                                                                                                                                                                                                 |
| GreenSlope<br/> \_ \_ \_ Pente verte d2d1 LINEARTRANSFER \_ prop<br/>             | FLOAT<br/> supérieures<br/> | Pente de la fonction linéaire pour le canal vert.                                                                                                                                                                                                                                                                                                                                                                                                       |
| GreenDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ vert \_ Disable<br/>         | BOOL<br/> FALSE<br/> | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal vert. Si vous définissez cette valeur sur FALSe, elle applique la fonction GreenLinearTransfer au canal vert.                                                                                                                                                                                                                                                                      |
| BlueYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ bleu \_ \_ intersection Y<br/>   | FLOAT<br/> 0.0f<br/> | L’interception Y de la fonction linéaire pour le canal bleu.                                                                                                                                                                                                                                                                                                                                                                                                  |
| BlueSlope<br/> \_ \_ \_ Pente bleue d2d1 LINEARTRANSFER \_ prop<br/>               | FLOAT<br/> supérieures<br/> | Pente de la fonction linéaire pour le canal bleu.                                                                                                                                                                                                                                                                                                                                                                                                        |
| BlueDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ bleu \_ Disable<br/>           | BOOL<br/> FALSE<br/> | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal bleu. Si vous définissez cette valeur sur FALSe, elle applique la fonction BlueLinearTransfer au canal bleu.                                                                                                                                                                                                                                                                         |
| AlphaYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ alpha \_ Y \_ intersection<br/> | FLOAT<br/> 0.0f<br/> | L’interception Y de la fonction linéaire pour le canal alpha.                                                                                                                                                                                                                                                                                                                                                                                                 |
| AlphaSlope<br/> \_ \_ \_ Pente alpha d2d1 LINEARTRANSFER \_ prop<br/>             | FLOAT<br/> 0.0f<br/> | Pente de la fonction linéaire pour le canal alpha.                                                                                                                                                                                                                                                                                                                                                                                                       |
| AlphaDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ alpha \_ Disable<br/>         | BOOL<br/> FALSE<br/> | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal alpha. Si vous définissez cette valeur sur FALSe, elle applique la fonction AlphaLinearTransfer au canal alpha.                                                                                                                                                                                                                                                                      |
| ClampOutput<br/> \_Sortie de Clamp d2d1 LINEARTRANSFER \_ prop \_ \_<br/>           | BOOL<br/> FALSE<br/> | Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique. L’effet serre les valeurs avant de prémultiplier le alpha.<br/> Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées. Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.<br/> |



 

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

 

