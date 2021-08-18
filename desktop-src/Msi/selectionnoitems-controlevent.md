---
description: Le contrôle SelectionTree utilise l’événement SelectionNoItems pour supprimer le texte de description de l’élément obsolète ou pour désactiver les boutons devenus inutiles. Cet événement doit être créé dans la table EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17220849c6bf50a28a0a0596bcd347e2f0a4c5af77cb53c9d9fa0041ced59abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040459"
---
# <a name="selectionnoitems-controlevent"></a>SelectionNoItems ControlEvent,

Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionNoItems pour supprimer le texte de description de l’élément obsolète ou pour désactiver les boutons devenus inutiles. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.

## <a name="published-by"></a>Publié par

[Contrôle SelectionTree](selectiontree-control.md) si la sélection n’a aucun nœud.

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Supprime le texte de description de l’élément obsolète ou désactive les boutons obsolètes.

## <a name="typical-use"></a>Utilisation courante

Peut être utilisé pour désactiver les boutons suivant, réinitialiser et DiskCost de la [boîte de dialogue de sélection](selection-dialog.md) lorsqu’une sélection n’a aucun nœud et que ces boutons deviennent inutiles.

 

 



