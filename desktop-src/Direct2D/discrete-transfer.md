---
title: Effet de transfert discret
description: Utilisez l’effet de transfert discret pour mapper les intensités de couleur d’une image à l’aide d’une fonction de transfert par étape créée à partir d’une liste de valeurs que vous fournissez.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- effet de transfert discret
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104564742"
---
# <a name="discrete-transfer-effect"></a>Effet de transfert discret

Utilisez l’effet de transfert discret pour mapper les intensités de couleur d’une image à l’aide d’une fonction de transfert par étape créée à partir d’une liste de valeurs que vous fournissez.

Le CLSID de cet effet est CLSID \_ D2D1DiscreteTransfer.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’image ci-dessous montre l’entrée et la sortie de l’effet de transfert discret.



| Avant                                                            |
|-------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)        |
| After                                                             |
| ![image après la transformation.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



La fonction de transfert est basée sur la liste des entrées : V = (v0, v1, v2, V3, V ? , V<sub>N</sub>), où N est le nombre d’éléments-1.

L’intensité en pixels d’entrée est représentée par C. L’intensité en pixels de sortie, C est calculée avec l’équation :

Pour une valeur C, choisissez une valeur k, telle que :

![formule du processus.](images/discrete-transfer1.png)

La sortie C peut être calculée à l’aide de l’équation : C' = V ?

Cet effet fonctionne sur les images alpha directes et prémultipliées. L’effet génère des bitmaps alpha prémultipliés.

Voici à quoi ressemble le graphique de la fonction de transfert discret si les entrées sont `[0.25, 0.5, 0.75, 1.0]` .

![graphique d’intensité de pixel pour la fonction de transfert discrète.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>Propriétés d’effet

> [!Note]  
> Les valeurs de tous les canaux des propriétés de transfert discrètes sont sans unité et ont un minimum de 0,0 et un maximum de 1,0.

 



| Nom complet et énumération d’index                                              | Type et valeur par défaut                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> \_ \_ \_ Table rouge d2d1 DISCRETETRANSFER \_ prop<br/>         | DISSOCIÉ\[\]<br/> {0.0 f, 1.0 f}<br/> | Liste des valeurs utilisées pour définir la fonction de transfert pour le canal rouge.                                                                                                                                                                                                                                                                                                                                                                                 |
| RedDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ rouge \_ Disable<br/>     | BOOL<br/> FALSE<br/>             | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal rouge. Si vous affectez la valeur FALSe, l’effet applique la fonction RedDiscreteTransfer au canal rouge.                                                                                                                                                                                                                                                                 |
| GreenTable<br/> \_ \_ \_ Table verte d2d1 DISCRETETRANSFER \_ prop<br/>     | DISSOCIÉ\[\]<br/> {0.0 f, 1.0 f}<br/> | Liste des valeurs qui définissent la fonction de transfert pour le canal vert.                                                                                                                                                                                                                                                                                                                                                                                  |
| GreenDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ vert \_ Disable<br/> | BOOL<br/> FALSE<br/>             | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal vert. Si vous affectez la valeur FALSe, l’effet applique la fonction GreenDiscreteTransfer au canal vert.                                                                                                                                                                                                                                                           |
| BlueTable<br/> \_ \_ \_ Table bleue d2d1 DISCRETETRANSFER \_ prop<br/>       | DISSOCIÉ\[\]<br/> {0.0 f, 1.0 f}<br/> | Liste des valeurs qui définissent la fonction de transfert pour le canal bleu.                                                                                                                                                                                                                                                                                                                                                                                   |
| BlueDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ bleu \_ Disable<br/>   | BOOL<br/> FALSE<br/>             | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal bleu. Si vous affectez la valeur FALSe, l’effet applique la fonction BlueDiscreteTransfer au canal bleu.                                                                                                                                                                                                                                                              |
| AlphaTable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ alpha, \_ table<br/>     | DISSOCIÉ\[\]<br/> {0.0 f, 1.0 f}<br/> | Liste des valeurs qui définissent la fonction de transfert pour le canal alpha.                                                                                                                                                                                                                                                                                                                                                                                  |
| AlphaDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ alpha \_ Disable<br/> | BOOL<br/> FALSE<br/>             | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal alpha. Si vous affectez la valeur FALSe, l’effet applique la fonction AlphaDiscreteTransfer au canal alpha.                                                                                                                                                                                                                                                           |
| ClampOutput<br/> \_Sortie de Clamp d2d1 DISCRETETRANSFER \_ prop \_ \_<br/>   | BOOL<br/> FALSE<br/>             | Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique. L’effet serre les valeurs avant de prémultiplier le alpha.<br/> Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées. Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.<br/> |



 

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

 

