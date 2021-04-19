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
# <a name="idle-triggers-for-task-scheduler-10"></a><span data-ttu-id="2f876-104">Déclencheurs inactifs pour Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="2f876-104">Idle Triggers for Task Scheduler 1.0</span></span>

<span data-ttu-id="2f876-105">Un déclencheur inactif est un déclencheur basé sur des événements qui est déclenché un nombre spécifique de fois que l’ordinateur devient inactif.</span><span class="sxs-lookup"><span data-stu-id="2f876-105">An idle trigger is an event-based trigger that is fired a specific number of times after the computer becomes idle.</span></span> <span data-ttu-id="2f876-106">Il existe plusieurs conditions qui définissent le moment où un ordinateur devient inactif, par exemple quand aucune entrée du clavier ou de la souris ne se produit.</span><span class="sxs-lookup"><span data-stu-id="2f876-106">There are multiple conditions that define when a computer becomes idle, such as when no keyboard or mouse input occurs.</span></span>

<span data-ttu-id="2f876-107">Les déclencheurs inactifs sont créés en spécifiant le \_ déclencheur d’événement de tâche \_ \_ sur \_ inactif dans le membre du [**\_ \_ type de déclencheur**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) de tâche de la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="2f876-107">Idle triggers are created by specifying TASK\_EVENT\_TRIGGER\_ON\_IDLE in the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="2f876-108">Le déclencheur inactif est déclenché lorsque le système devient inactif pendant la durée spécifiée par le délai d’attente d’inactivité de l’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="2f876-108">The idle trigger is fired when the system becomes idle for the amount of time that is specified by the idle wait time of the work item.</span></span>

> [!Note]  
> <span data-ttu-id="2f876-109">Lorsque \_ \_ le déclencheur \_ d’événement de tâche d' \_ inactivité est spécifié, les membres **wStartHour**, **wStartMinute** et **type** de la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="2f876-109">When TASK\_EVENT\_TRIGGER\_ON\_IDLE is specified, the **wStartHour**, **wStartMinute**, and **Type** members of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure are ignored.</span></span>

 

<span data-ttu-id="2f876-110">Vous pouvez définir le délai d’attente d’inactivité d’un élément de travail en appelant la méthode [**IScheduledWorkItem :: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) .</span><span class="sxs-lookup"><span data-stu-id="2f876-110">You can set the idle wait time of a work item by calling the [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) method.</span></span> <span data-ttu-id="2f876-111">Cette méthode définit la durée (en minutes) pendant laquelle le système doit rester inactif avant le déclenchement du déclencheur et l’exécution de l’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="2f876-111">This method sets the amount of time (in minutes) that the system must remain idle before the trigger is fired and the work item is executed.</span></span>

<span data-ttu-id="2f876-112">Pour récupérer le temps d’inactivité d’une tâche, appelez la méthode [**IScheduledWorkItem :: GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .</span><span class="sxs-lookup"><span data-stu-id="2f876-112">To retrieve the idle time of a task, call the [**IScheduledWorkItem::GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f876-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f876-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f876-114">Déclencheurs de tâche</span><span class="sxs-lookup"><span data-stu-id="2f876-114">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




