---
title: Effet d’opacité
description: Cet effet ajuste l’opacité d’une image en multipliant le canal alpha de l’entrée par la valeur d’opacité spécifiée. Il a une seule entrée.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511576"
---
# <a name="opacity-effect"></a>Effet d’opacité

Cet effet ajuste l’opacité d’une image en multipliant le canal alpha de l’entrée par la valeur d’opacité spécifiée. Il a une seule entrée.

Le CLSID de cet effet est CLSID \_ D2D1Opacity.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index              | Type et valeur par défaut | Description                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| Opacité D2D1 opacité du \_ \_ Prop. \_<br/> | FLOAT 1.0 f<br/>   | Multiplicateur du canal alpha de l’image d’entrée. La valeur minimale est 0.0 f et la valeur maximale est 1,0 f. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows 10 \| applications du Windows Store\] |
| Serveur minimal pris en charge | Applications de \[ Bureau Windows 10 \| applications du Windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
