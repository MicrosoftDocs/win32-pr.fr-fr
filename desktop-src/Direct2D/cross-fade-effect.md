---
title: Effet fondu croisé
description: Cet effet combine deux images en ajoutant des pixels pondérés à partir des images d’entrée. Il a deux entrées, nommées destination et source.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508542"
---
# <a name="cross-fade-effect"></a>Effet fondu croisé

Cet effet combine deux images en ajoutant des pixels pondérés à partir des images d’entrée. Il a deux entrées, nommées destination et source.

La formule de fondu croisé est **sortie = poids \* destination + (1-poids) \* source**.

Le CLSID de cet effet est CLSID \_ D2D1CrossFade.

## <a name="effect-properties"></a>Propriétés d’effet

| Nom complet et énumération d’index             | Type et valeur par défaut | Description                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poids de la \_ prop de fondu WeightD2D1 \_ \_<br/> | FLOAT 0.5 f<br/>   | Mesure du poids des valeurs de couleur de l’image source par rapport à l’image de destination. La valeur minimale est 0.0 f (utilisez exclusivement l’image de destination pour déterminer la sortie) et la valeur maximale est 1,0 f (utilisez exclusivement l’image source pour déterminer la sortie). |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows 10 \| applications du Windows Store\] |
| Serveur minimal pris en charge | Applications de \[ Bureau Windows 10 \| applications du Windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
