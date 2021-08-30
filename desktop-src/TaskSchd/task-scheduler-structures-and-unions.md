---
title: Structures et unions de Planificateur de tâches
description: Répertorie les structures et les unions utilisées par les API Planificateur de tâches 1,0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Planificateur de tâches Planificateur de tâches, référence, structures et unions
- déclencheurs Planificateur de tâches, structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47610012666d2d84b192235470674c2d34c700601fa581a2e948ec342dd5f93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100099"
---
# <a name="task-scheduler-structures-and-unions"></a>Structures et unions de Planificateur de tâches

Cette section décrit les structures et les unions utilisées par les API Planificateur de tâches.

Toutes les structures et unions ci-dessous sont utilisées par Planificateur de tâches 1,0.



| Nom                                               | Description                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**QUOTIDIENNE**](/windows/desktop/api/Mstask/ns-mstask-daily)                             | Définit l’intervalle, en jours, à partir duquel une tâche est exécutée.                                                                          |
| [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | Définit le jour du mois auquel la tâche s’exécutera.                                                                                 |
| [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | Définit la ou les date (s) d’exécution de la tâche par mois, semaine et jour de la semaine.                                                     |
| [**\_déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | Définit les heures d’exécution d’un [*élément de travail*](w.md)planifié.                                                  |
| [**\_Union de type de déclencheur \_**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | Définit la planification d’appel du déclencheur dans le membre de **type** d’une structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . |
| [**HEBDOMADAIRE**](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | Définit l’intervalle, en semaines, entre les appels d’une tâche.                                                                  |



 

 

 




