---
title: Effet de transfert de table
description: Utilisez l’effet de transfert de table pour mapper les intensités de couleur d’une image à l’aide d’une fonction de transfert créée à partir de l’interpolation d’une liste de valeurs que vous fournissez.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- effet de transfert de table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c533b55fd55c983b976633b766a6d8d273631d6111de9e2e36387f711f5f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665004"
---
# <a name="table-transfer-effect"></a>Effet de transfert de table

Utilisez l’effet de transfert de table pour mapper les intensités de couleur d’une image à l’aide d’une fonction de transfert créée à partir de l’interpolation d’une liste de valeurs que vous fournissez.

Le CLSID de cet effet est CLSID \_ D2D1TableTransfer.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

L’image ci-dessous montre l’entrée et la sortie de l’effet de transfert de table.



| Avant                                                         |
|----------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)     |
| Après                                                          |
| ![image après la transformation.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



La fonction de transfert est basée sur une liste d’entrées V = (v0, v1, v2, V3, V ? , V<sub>N</sub>), où N est le nombre d’éléments-1.

L’intensité en pixels d’entrée est représentée par C. L’intensité en pixels de sortie, C peut être calculée avec l’équation.

Pour une valeur C, choisissez une valeur k, telle que : k/N = C < (k + 1)/N

La sortie C est calculée à l’aide de l’équation suivante : C' = V ? + (C-k/N) \* N \* (V ??? 1,0? -V ?)

Cet effet fonctionne sur les images alpha directes et prémultipliées. L’effet génère des bitmaps alpha prémultipliés.

Voici à quoi ressemble le graphique de la fonction de transfert de table si la propriété de table a la valeur `[0.0, 0.25, 1.0]` .

![graphique d’intensité de pixel pour la fonction de transfert de table.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Propriétés d’effet

> [!Note]  
> Les valeurs de tous les canaux des propriétés de transfert de table sont sans unité et ont un minimum de 0,0 et un maximum de 1,0.

 



| Nom complet et énumération d’index                                           | Type et valeur par défaut                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> \_ \_ \_ Table rouge d2d1 TABLETRANSFER \_ prop<br/>         | DISSOCIÉ\[\]<br/> {0.0 f, 1.0 f}<br/> | Liste des valeurs utilisées pour définir la fonction de transfert pour le canal rouge.                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ rouge \_ Disable<br/>     | BOOL<br/> FALSE<br/>             | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal rouge. Si vous définissez cette valeur sur FALSe, elle applique la fonction RedTableTransfer au canal rouge.                                                                                                                                                                                                                                                                             |
| GreenTable<br/> \_ \_ \_ Table verte d2d1 TABLETRANSFER \_ prop<br/>     | DISSOCIÉ\[\]<br/> {0.0 f, 1.0 f}<br/> | Liste des valeurs utilisées pour définir la fonction de transfert pour le canal vert.                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ vert \_ Disable<br/> | BOOL<br/> FALSE<br/>             | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal vert. Si vous définissez cette valeur sur FALSe, elle applique la fonction GreenTableTransfer au canal vert.                                                                                                                                                                                                                                                                       |
| BlueTable<br/> \_ \_ \_ Table bleue d2d1 TABLETRANSFER \_ prop<br/>       | DISSOCIÉ\[\]<br/> {0.0 f, 1.0 f}<br/> | Liste des valeurs utilisées pour définir la fonction de transfert pour le canal bleu.                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ bleu \_ Disable<br/>   | BOOL<br/> FALSE<br/>             | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal bleu. Si vous définissez cette valeur sur FALSe, elle applique la fonction BlueTableTransfer au canal bleu.                                                                                                                                                                                                                                                                          |
| AlphaTable<br/> \_ \_ \_ \_ Table alpha de transfert de table d2d1 \_<br/>   | DISSOCIÉ\[\]<br/> {0.0 f, 1.0 f}<br/> | Liste des valeurs utilisées pour définir la fonction de transfert pour le canal alpha.                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ alpha \_ Disable<br/> | BOOL<br/> FALSE<br/>             | Si vous affectez la valeur TRUE, l’effet n’applique pas la fonction de transfert au canal alpha. Si vous définissez cette valeur sur FALSe, elle applique la fonction AlphaTableTransfer au canal alpha.                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> \_Sortie de Clamp d2d1 TABLETRANSFER \_ prop \_ \_<br/>   | BOOL<br/> FALSE<br/>             | Si l’effet fixe les valeurs de couleur entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique. L’effet serre les valeurs avant de prémultiplier le alpha.<br/> Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées. Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.<br/> |



 

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

 

