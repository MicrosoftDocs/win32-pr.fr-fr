---
title: Déclencheurs inactifs pour Planificateur de tâches 1,0
description: Un déclencheur inactif est un déclencheur basé sur des événements qui est déclenché un nombre spécifique de fois que l’ordinateur devient inactif. Il existe plusieurs conditions qui définissent le moment où un ordinateur devient inactif, par exemple quand aucune entrée du clavier ou de la souris ne se produit.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510201"
---
# <a name="idle-triggers-for-task-scheduler-10"></a>Déclencheurs inactifs pour Planificateur de tâches 1,0

Un déclencheur inactif est un déclencheur basé sur des événements qui est déclenché un nombre spécifique de fois que l’ordinateur devient inactif. Il existe plusieurs conditions qui définissent le moment où un ordinateur devient inactif, par exemple quand aucune entrée du clavier ou de la souris ne se produit.

Les déclencheurs inactifs sont créés en spécifiant le \_ déclencheur d’événement de tâche \_ \_ sur \_ inactif dans le membre du [**\_ \_ type de déclencheur**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) de tâche de la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Le déclencheur inactif est déclenché lorsque le système devient inactif pendant la durée spécifiée par le délai d’attente d’inactivité de l’élément de travail.

> [!Note]  
> Lorsque \_ \_ le déclencheur \_ d’événement de tâche d' \_ inactivité est spécifié, les membres **wStartHour**, **wStartMinute** et **type** de la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) sont ignorés.

 

Vous pouvez définir le délai d’attente d’inactivité d’un élément de travail en appelant la méthode [**IScheduledWorkItem :: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) . Cette méthode définit la durée (en minutes) pendant laquelle le système doit rester inactif avant le déclenchement du déclencheur et l’exécution de l’élément de travail.

Pour récupérer le temps d’inactivité d’une tâche, appelez la méthode [**IScheduledWorkItem :: GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclencheurs de tâche](task-triggers.md)
</dt> </dl>

 

 




