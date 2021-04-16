---
title: T (Planificateur de tâches)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508245"
---
# <a name="t-task-scheduler"></a><span data-ttu-id="e85e9-103">T (Planificateur de tâches)</span><span class="sxs-lookup"><span data-stu-id="e85e9-103">T (Task Scheduler)</span></span>

<span data-ttu-id="e85e9-104">A B C D [e](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="e85e9-104">A B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e85e9-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**objets de tâche**</span><span class="sxs-lookup"><span data-stu-id="e85e9-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**task objects**</span></span>
</dt> <dd>

<span data-ttu-id="e85e9-106">Instances d’un objet qui fournit des méthodes pour la gestion des tâches.</span><span class="sxs-lookup"><span data-stu-id="e85e9-106">Instances of an object that provides methods for managing tasks.</span></span> <span data-ttu-id="e85e9-107">Cela comprend les méthodes de définition et de récupération des propriétés. exécution, arrêt et suppression de tâches ; et la création de nouveaux déclencheurs et la récupération des anciens déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="e85e9-107">This includes methods for setting and retrieving properties; running, terminating, and deleting tasks; and creating new triggers and retrieving old triggers.</span></span>

<span data-ttu-id="e85e9-108">L’objet de tâche est créé par des appels à [**IScheduledWorkItem :: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) et [**IScheduledWorkItem :: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="e85e9-108">The task object is created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

</dd> <dt>

<span data-ttu-id="e85e9-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**objets du planificateur de tâches**</span><span class="sxs-lookup"><span data-stu-id="e85e9-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**task scheduler objects**</span></span>
</dt> <dd>

<span data-ttu-id="e85e9-110">Instances d’un objet qui représente le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="e85e9-110">Instances of an object the represents the Task Scheduler service.</span></span> <span data-ttu-id="e85e9-111">Cet objet prend en charge deux interfaces : **IUnknown** et [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (actuellement, les tâches sont le seul type d’éléments de travail pris en charge par le service Planificateur de tâches).</span><span class="sxs-lookup"><span data-stu-id="e85e9-111">This object supports two interfaces: **IUnknown** and [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (currently tasks are the only type of work items supported by the Task Scheduler service).</span></span>

<span data-ttu-id="e85e9-112">Les objets du planificateur de tâches sont créés par des appels à **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e85e9-112">Task scheduler objects are created by calls to **CoCreateInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="e85e9-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**objets de déclencheur de tâche**</span><span class="sxs-lookup"><span data-stu-id="e85e9-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**task trigger objects**</span></span>
</dt> <dd>

<span data-ttu-id="e85e9-114">Instances d’un objet fournit des méthodes pour définir et récupérer des déclencheurs de tâche.</span><span class="sxs-lookup"><span data-stu-id="e85e9-114">Instances of an object the provides methods for setting and retrieving task triggers.</span></span> <span data-ttu-id="e85e9-115">Cet objet prend en charge deux interfaces : **IUnknown** et [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span><span class="sxs-lookup"><span data-stu-id="e85e9-115">This object supports two interfaces: **IUnknown** and [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span></span>

<span data-ttu-id="e85e9-116">Les objets déclencheurs de tâche sont créés par des appels à [**IScheduledWorkItem :: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) et [**IScheduledWorkItem :: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="e85e9-116">Task trigger objects are created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

<span data-ttu-id="e85e9-117">Voir aussi : *déclencheurs*.</span><span class="sxs-lookup"><span data-stu-id="e85e9-117">See also: *triggers*.</span></span>

</dd> <dt>

<span data-ttu-id="e85e9-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**décrites**</span><span class="sxs-lookup"><span data-stu-id="e85e9-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tasks**</span></span>
</dt> <dd>

<span data-ttu-id="e85e9-119">Tout élément que l’Planificateur de tâches peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="e85e9-119">Any item that the Task Scheduler can execute.</span></span> <span data-ttu-id="e85e9-120">Ces éléments peuvent inclure l’un des éléments suivants (pris en charge par le système d’exploitation sur lequel la tâche s’exécute) : les applications Win32®, les applications Win16, les applications du système d’exploitation/2, les applications MS-DOS®, les fichiers de commandes ( \* . bat), les fichiers de commandes ( \* . cmd) ou tout type de fichier correctement inscrit.</span><span class="sxs-lookup"><span data-stu-id="e85e9-120">These items may include any of the following (as supported by the operating system on which the task will execute): Win32® applications, Win16 applications, OS/2 applications, MS-DOS® applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

</dd> <dt>

<span data-ttu-id="e85e9-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Dossier tâches**</span><span class="sxs-lookup"><span data-stu-id="e85e9-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks folder**</span></span>
</dt> <dd>

<span data-ttu-id="e85e9-122">Dossier qui répertorie tous les fichiers de tâches (actuellement, les tâches sont les seuls éléments de travail disponibles).</span><span class="sxs-lookup"><span data-stu-id="e85e9-122">The folder that lists all task files (currently, tasks are the only work items available).</span></span> <span data-ttu-id="e85e9-123">Ces fichiers contiennent des informations sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="e85e9-123">These files contain the information about the task.</span></span> <span data-ttu-id="e85e9-124">Le nom de ces fichiers reflète le nom de la tâche.</span><span class="sxs-lookup"><span data-stu-id="e85e9-124">The name of these files reflects the name of the task.</span></span>

<span data-ttu-id="e85e9-125">Vous pouvez récupérer l’emplacement du dossier tâches à partir du registre en obtenant les données pour la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="e85e9-125">You can retrieve the location of the Tasks folder from the registry by getting data for the following value:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span data-ttu-id="e85e9-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="e85e9-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**triggers**</span></span>
</dt> <dd>

<span data-ttu-id="e85e9-127">Ensemble de critères qui, lorsqu’il est rempli, entraîne l’exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="e85e9-127">A set of criteria that, when met, will cause a task to be executed.</span></span> <span data-ttu-id="e85e9-128">Planificateur de tâches fournit des déclencheurs temporels et basés sur des événements qui peuvent spécifier des heures de début de tâche, des critères de répétition et d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="e85e9-128">Task Scheduler provides time-based and event-based triggers that can specify task start times, repetition criteria, and other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="e85e9-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**chaînes de déclencheur**</span><span class="sxs-lookup"><span data-stu-id="e85e9-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**trigger strings**</span></span>
</dt> <dd>

<span data-ttu-id="e85e9-130">Chaîne qui décrit le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="e85e9-130">A string that describes the trigger.</span></span> <span data-ttu-id="e85e9-131">Cette chaîne est créée par le service Planificateur de tâches et s’affiche dans l’interface utilisateur Planificateur de tâches dans un format semblable à « à 2PM chaque jour, à partir du 5/11/97. »</span><span class="sxs-lookup"><span data-stu-id="e85e9-131">This string is created by the Task Scheduler service, and appears in the Task Scheduler user interface in a form similar to "At 2PM every day, starting 5/11/97."</span></span>

</dd> <dt>

<span data-ttu-id="e85e9-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**structures de déclencheur**</span><span class="sxs-lookup"><span data-stu-id="e85e9-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**trigger structures**</span></span>
</dt> <dd>

<span data-ttu-id="e85e9-133">Structure [**de \_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) utilisée lors de la définition ou de la récupération des critères définissant le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="e85e9-133">The [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure used when setting or retrieving the criteria that defines the trigger.</span></span> <span data-ttu-id="e85e9-134">Les critères incluent le moment où le déclencheur se déclenche et le type du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="e85e9-134">The criteria includes when the trigger will fire, and the type of the trigger.</span></span>

</dd> </dl>

 

 




