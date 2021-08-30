---
description: Le contrôle SelectionTree utilise l’événement SelectionDescription pour publier une chaîne qui contient la description de l’élément mis en surbrillance. Cette chaîne est le champ Description de la table de fonctionnalités. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac1d7a6fdfa4e215e0f659b5f3341404e2376f5e82f3c1d019a35e833995e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040579"
---
# <a name="selectiondescription-controlevent"></a>SelectionDescription ControlEvent,

Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionDescription pour publier une chaîne qui contient la description de l’élément mis en surbrillance. Cette chaîne est le champ **Description** de la [table de fonctionnalités](feature-table.md). Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le [contrôle SelectionTree](selectiontree-control.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un contrôle de [texte](text-control.md) sur la même boîte de dialogue modale que le SelectionTree s’abonne à ce ControlEvent, via la [table EventMapping](eventmapping-table.md). Le contrôle de texte utilise cet événement pour afficher la description de l’élément mis en surbrillance.

 

 



