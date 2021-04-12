---
description: Les primitives qui se trouvent partiellement à l’intérieur (ou complètement à l’extérieur) de la vue frustum peuvent être découpées afin que seule la partie visible de la primitive soit rendue.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: État de découpage primitif (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392884"
---
# <a name="primitive-clipping-state-direct3d-9"></a>État de découpage primitif (Direct3D 9)

Les primitives qui se trouvent partiellement à l’intérieur (ou complètement à l’extérieur) de la [vue frustum](viewports-and-clipping.md) peuvent être découpées afin que seule la partie visible de la primitive soit rendue. Le découpage réduit la quantité de travail qui est effectuée uniquement pour les primitives ou les parties d’une primitive qui seront visibles.

Pour utiliser le pipeline pour le découpage, définissez l' \_ État de rendu du découpage D3DRS sur **true** (valeur par défaut) pour activer le découpage, ou sur **false** pour désactiver le découpage Direct3D.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 



