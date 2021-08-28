---
description: L’action CostInitialize lance le processus d’évaluation des coûts d’installation.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Action CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959e9e250292a44050c1f4b9feb3fb29f7530fe2a1f53aa77a62bf3680ea9eeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948366"
---
# <a name="costinitialize-action"></a>Action CostInitialize

L’action CostInitialize lance le processus d' [*évaluation des coûts*](c-gly.md) d’installation.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Toutes les actions standard ou [personnalisées](custom-actions.md) qui affectent le coût doivent être séquencées avant l’action CostInitialize. Appelez l’action [FileCost](filecost-action.md) immédiatement après l’action CostInitialize. Appelez ensuite l’action [CostFinalize](costfinalize-action.md) à la suite de l’action d’action CostInitialize pour que tous les calculs de coût final soient disponibles pour le programme d’installation par le biais de la table des [composants](component-table.md) .

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Remarques

L’action CostInitialize charge la table des composants et la table des [fonctionnalités](feature-table.md) en mémoire.

Pour plus d’informations sur le processus d' [*évaluation des coûts*](c-gly.md) dans le programme d’installation, consultez [coûts des fichiers](file-costing.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Coût des fichiers](file-costing.md)
</dt> </dl>

 

 



