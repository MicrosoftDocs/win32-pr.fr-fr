---
description: Le contrôle SelectionTree utilise l’événement de sélection pour publier la taille de l’élément mis en surbrillance.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: Sélection de ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c8733c0155adc085343c0a5db1a42e3aa219719babb5b342781c5bb9923ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040359"
---
# <a name="selectionsize-controlevent"></a>Sélection de ControlEvent,

Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement de sélection pour publier la taille de l’élément mis en surbrillance. S’il s’agit d’un élément parent, le nombre d’enfants sélectionnés est également publié. La chaîne est l’une des chaînes **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** ou **SelParentCostNegNeg** de la [table UIText](uitext-table.md). Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.

## <a name="published-by"></a>Publié par

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que le contrôle SelectionTree via la [table EventMapping](eventmapping-table.md). Le contrôle de texte utilise cet événement pour afficher la taille de l’élément mis en surbrillance.

 

 



