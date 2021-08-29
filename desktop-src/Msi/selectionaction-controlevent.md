---
description: Le contrôle SelectionTree utilise cet événement pour publier une chaîne décrivant l’élément mis en surbrillance. La chaîne est l’un des &\# 0034 ; Sel \* & \# 0034 ; chaînes de la table UIText. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: SelectionAction ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2353c967eb6a7a0160a647b51ac0eff87ad187499147f3c051bc8eb33086df88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040649"
---
# <a name="selectionaction-controlevent"></a>SelectionAction ControlEvent,

Le [contrôle SelectionTree](selectiontree-control.md) utilise cet événement pour publier une chaîne décrivant l’élément mis en surbrillance. La chaîne est l’une des chaînes « sel \* » de la [table UIText](uitext-table.md). Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.

## <a name="published-by"></a>Publié par

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un contrôle de [texte](text-control.md) dans la même boîte de dialogue modale que SelectionTree doit s’abonner à cet événement via la [table EventMapping](eventmapping-table.md). Le contrôle de texte affiche l’explication de l’élément sélectionné.

 

 



