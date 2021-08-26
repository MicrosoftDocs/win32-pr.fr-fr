---
description: Le contrôle SelectionTree utilise l’événement SelectionBrowse pour générer une boîte de dialogue de navigation, ce qui permet de modifier le chemin d’accès de l’élément mis en surbrillance.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70d7c50e69921a5fefe7cff3c88c2351cacdecda42a164e8334c9afb3977bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040609"
---
# <a name="selectionbrowse-controlevent"></a>SelectionBrowse ControlEvent,

Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionBrowse pour générer une boîte de dialogue de **navigation** , ce qui permet de modifier le chemin d’accès de l’élément mis en surbrillance.

Cet événement doit être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le contrôle qui s’abonne à cet événement. L’événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Tous les contrôles qui publient un événement SelectionBrowse sont désactivés si une fonctionnalité sélectionnée est déjà installée, n’est pas configurable ou n’est pas sélectionnée pour une installation locale. Pour pouvoir être configurée, la fonctionnalité doit avoir une [propriété publique](public-properties.md) entrée dans le \_ champ Directory de la [table Feature](feature-table.md).

## <a name="published-by"></a>Publié par

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argument

Nom de la boîte de dialogue à générer.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) dans la même boîte de dialogue modale que le SelectionTree utilise cet événement pour déclencher la boîte de dialogue **Parcourir** .

 

 



