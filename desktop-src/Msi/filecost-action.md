---
description: FileCostaction lance des actions d’installation standard costingof standard.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Action FileCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042883"
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

 

 



