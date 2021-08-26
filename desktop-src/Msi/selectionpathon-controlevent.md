---
description: Le contrôle SelectionTree utilise l’événement SelectionPathOn pour publier une valeur booléenne indiquant si un tracé de sélection est associé à la fonctionnalité actuellement sélectionnée. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea32926117c200f466bd2c40ac611e7ccbc47fb6a231a5dcf93ffa2ee0446b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040429"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent,

Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionPathOn pour publier une valeur booléenne indiquant si un tracé de sélection est associé à la fonctionnalité actuellement sélectionnée. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Le SelectionPathOn ControlEvent, n’est jamais publié pendant une [installation de maintenance](maintenance-installation.md).

## <a name="published-by"></a>Publié par

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que SelectionTree doit s’abonner à l’événement via la [table EventMapping](eventmapping-table.md). Le contrôle de texte affiche la légende du chemin de sélection. Ce contrôle de texte est visible ou masqué en fonction de l’événement.

 

 



