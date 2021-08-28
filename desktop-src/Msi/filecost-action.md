---
description: FileCostaction lance des actions d’installation standard costingof standard.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Action FileCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b49cbb4357b33ebe735eaff501f1c155c411bc969c7fea96a1cab7417c803a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947054"
---
# <a name="filecost-action"></a>Action FileCost

Le FileCostaction lance un [*coût*](c-gly.md)dynamique des actions d’installation standard.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Toutes les actions standard ou [personnalisées](custom-actions.md) qui affectent le coût doivent être séquencées avant l’action [CostInitialize](costinitialize-action.md) . Appelez l’action FileCost immédiatement après l’action CostInitialize. Appelez ensuite l’action [CostFinalize](costfinalize-action.md) à la suite de l’action CostInitialize pour que tous les calculs de coût final soient disponibles pour le programme d’installation par le biais de la table des [composants](component-table.md) .

L’action [CostInitialize](costinitialize-action.md) doit être exécutée avant l’action FileCost. Le programme d’installation détermine ensuite le coût de l’espace disque de chaque fichier de la table de [fichiers](file-table.md) , en fonction du composant (voir [table des composants](component-table.md)), en prenant à la fois le clustering de [*volumes*](v-gly.md) et la présence de fichiers existants qui peuvent avoir besoin d’être remplacés en compte. Toutes les actions qui consomment ou libèrent de l’espace disque sont également prises en compte. Si un fichier existant est trouvé, une vérification de la version du fichier est effectuée pour déterminer si le nouveau fichier doit réellement être installé ou non. Si le numéro de version du fichier existant est égal ou supérieur, le fichier existant n’est pas remplacé et aucun coût d’espace disque n’est encouru. Dans tous les cas, le programme d’installation utilise les résultats de la vérification du numéro de version pour définir l’état d’installation de chaque fichier.

L’action FileCost Initialise le calcul du coût avec TheInstaller. Le [*coût*](c-gly.md) dynamique réel ne se produit pas tant que l’action [CostFinalize](costfinalize-action.md) n’est pas exécutée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Coût des fichiers](file-costing.md)
</dt> </dl>

 

 



