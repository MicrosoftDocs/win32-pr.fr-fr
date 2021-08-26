---
description: Le contrôle SelectionTree utilise l’événement SelectionPath pour publier le chemin d’accès de l’élément mis en surbrillance.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45dfcb017c18b026f03bf9fa9b89d7be33db49bafc3dd9f899846cbada1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040439"
---
# <a name="selectionpath-controlevent"></a>SelectionPath ControlEvent,

Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionPath pour publier le chemin d’accès de l’élément mis en surbrillance. Si l’élément est sélectionné pour être exécuté à partir de la source, il s’agit du chemin d’accès de la source. Si l’élément est sélectionné pour être absent, la chaîne est la chaîne **AbsentPath** de la [table UIText](uitext-table.md). Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.

## <a name="published-by"></a>Publié par

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que SelectionTree doit s’abonner à l’événement via la [table EventMapping](eventmapping-table.md). Le contrôle de texte affiche le chemin d’accès de l’élément mis en surbrillance.

 

 



