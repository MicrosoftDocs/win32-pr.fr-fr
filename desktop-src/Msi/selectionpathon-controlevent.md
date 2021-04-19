---
description: Le contrôle SelectionTree utilise l’événement SelectionPathOn pour publier une valeur booléenne indiquant si un tracé de sélection est associé à la fonctionnalité actuellement sélectionnée. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527713"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent,

Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionPathOn pour publier une valeur booléenne indiquant si un tracé de sélection est associé à la fonctionnalité actuellement sélectionnée. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Le SelectionPathOn ControlEvent, n’est jamais publié pendant une [installation de maintenance](maintenance-installation.md).

## <a name="published-by"></a>Publié par

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Aucun

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun

## <a name="typical-use"></a>Utilisation courante

Un contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que SelectionTree doit s’abonner à l’événement via la [table EventMapping](eventmapping-table.md). Le contrôle de texte affiche la légende du chemin de sélection. Ce contrôle de texte est visible ou masqué en fonction de l’événement.

 

 



