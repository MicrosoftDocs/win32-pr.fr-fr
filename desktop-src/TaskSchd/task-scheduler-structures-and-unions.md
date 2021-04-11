---
title: Structures et unions de Planificateur de tâches
description: Répertorie les structures et les unions utilisées par les API Planificateur de tâches 1,0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Planificateur de tâches Planificateur de tâches, référence, structures et unions
- déclencheurs Planificateur de tâches, structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190868"
---
# <a name="task-scheduler-structures-and-unions"></a><span data-ttu-id="103dc-105">Structures et unions de Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="103dc-105">Task Scheduler Structures and Unions</span></span>

<span data-ttu-id="103dc-106">Cette section décrit les structures et les unions utilisées par les API Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="103dc-106">This section describes the structures and unions used by the Task Scheduler APIs.</span></span>

<span data-ttu-id="103dc-107">Toutes les structures et unions ci-dessous sont utilisées par Planificateur de tâches 1,0.</span><span class="sxs-lookup"><span data-stu-id="103dc-107">All the structures and unions below are used by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="103dc-108">Nom</span><span class="sxs-lookup"><span data-stu-id="103dc-108">Name</span></span>                                               | <span data-ttu-id="103dc-109">Description</span><span class="sxs-lookup"><span data-stu-id="103dc-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="103dc-110">**QUOTIDIENNE**</span><span class="sxs-lookup"><span data-stu-id="103dc-110">**DAILY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-daily)                             | <span data-ttu-id="103dc-111">Définit l’intervalle, en jours, à partir duquel une tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="103dc-111">Defines the interval, in days, at which a task is run.</span></span>                                                                          |
| [<span data-ttu-id="103dc-112">**MONTHLYDATE**</span><span class="sxs-lookup"><span data-stu-id="103dc-112">**MONTHLYDATE**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | <span data-ttu-id="103dc-113">Définit le jour du mois auquel la tâche s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="103dc-113">Defines the day of the month the task will run.</span></span>                                                                                 |
| [<span data-ttu-id="103dc-114">**MONTHLYDOW**</span><span class="sxs-lookup"><span data-stu-id="103dc-114">**MONTHLYDOW**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | <span data-ttu-id="103dc-115">Définit la ou les date (s) d’exécution de la tâche par mois, semaine et jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="103dc-115">Defines the date(s) that the task runs by month, week, and day of the week.</span></span>                                                     |
| [<span data-ttu-id="103dc-116">**\_déclencheur de tâche**</span><span class="sxs-lookup"><span data-stu-id="103dc-116">**TASK\_TRIGGER**</span></span>](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | <span data-ttu-id="103dc-117">Définit les heures d’exécution d’un [*élément de travail*](w.md)planifié.</span><span class="sxs-lookup"><span data-stu-id="103dc-117">Defines the times to run a scheduled [*work item*](w.md).</span></span>                                                  |
| [<span data-ttu-id="103dc-118">**\_Union de type de déclencheur \_**</span><span class="sxs-lookup"><span data-stu-id="103dc-118">**TRIGGER\_TYPE\_UNION**</span></span>](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | <span data-ttu-id="103dc-119">Définit la planification d’appel du déclencheur dans le membre de **type** d’une structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="103dc-119">Defines the invocation schedule of the trigger within the **Type** member of a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> |
| [<span data-ttu-id="103dc-120">**HEBDOMADAIRE**</span><span class="sxs-lookup"><span data-stu-id="103dc-120">**WEEKLY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | <span data-ttu-id="103dc-121">Définit l’intervalle, en semaines, entre les appels d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="103dc-121">Defines the interval, in weeks, between invocations of a task.</span></span>                                                                  |



 

 

 




