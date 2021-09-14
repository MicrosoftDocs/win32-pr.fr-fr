---
description: L’action CostFinalize termine le processus de coût d’installation interne commencé par l’action CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Action CostFinalize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091937"
---
# <a name="costfinalize-action"></a>Action CostFinalize

L’action CostFinalize termine le processus de [*coût*](c-gly.md) d’installation interne commencé par l’action [CostInitialize](costinitialize-action.md) .

## <a name="sequence-restrictions"></a>Restrictions de séquence

Toutes les actions standard ou [personnalisées](custom-actions.md) qui affectent le coût doivent être séquencées avant l’action [CostInitialize](costinitialize-action.md) . Appelez l’action [FileCost](filecost-action.md) immédiatement après l’action CostInitialize, puis appelez l’action CostFinalize pour que tous les calculs des coûts finaux soient disponibles pour le programme d’installation par le biais de la table des [composants](component-table.md) .

L’action CostFinalize doit être exécutée avant le démarrage d’une séquence d’interface utilisateur qui permet à l’utilisateur d’afficher ou de modifier les sélections ou les répertoires de la table de [fonctionnalités](feature-table.md) .

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

L’action CostFinalize interroge la table de [conditions](condition-table.md) pour déterminer les fonctionnalités qui sont planifiées pour être installées. L’évaluation des coûts est effectuée pour chaque composant de la table des [composants](component-table.md) .

L’action CostFinalize vérifie également que tous les répertoires cibles sont accessibles en écriture avant d’autoriser l’installation à continuer.

> [!Note]  
> Au cours d’une [installation d’administration](administrative-installation.md), CostFinalize définit toutes les fonctionnalités pour l’installation, à l’exception des fonctionnalités avec 0 créé dans la colonne niveau de la [table des fonctionnalités](feature-table.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Coût des fichiers](file-costing.md)
</dt> </dl>

 

 



