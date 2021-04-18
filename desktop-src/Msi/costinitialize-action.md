---
description: L’action CostInitialize lance le processus d’évaluation des coûts d’installation.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Action CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536701"
---
# <a name="costinitialize-action"></a>Action CostInitialize

L’action CostInitialize lance le processus d' [*évaluation des coûts*](c-gly.md) d’installation.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Toutes les actions standard ou [personnalisées](custom-actions.md) qui affectent le coût doivent être séquencées avant l’action CostInitialize. Appelez l’action [FileCost](filecost-action.md) immédiatement après l’action CostInitialize. Appelez ensuite l’action [CostFinalize](costfinalize-action.md) à la suite de l’action d’action CostInitialize pour que tous les calculs de coût final soient disponibles pour le programme d’installation par le biais de la table des [composants](component-table.md) .

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

L’action CostInitialize charge la table des composants et la table des [fonctionnalités](feature-table.md) en mémoire.

Pour plus d’informations sur le processus d' [*évaluation des coûts*](c-gly.md) dans le programme d’installation, consultez [coûts des fichiers](file-costing.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Coût des fichiers](file-costing.md)
</dt> </dl>

 

 



