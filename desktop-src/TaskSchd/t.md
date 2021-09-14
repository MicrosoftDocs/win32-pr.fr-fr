---
title: T (Planificateur de tâches)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120605"
---
# <a name="t-task-scheduler"></a>T (Planificateur de tâches)

A B C D [e](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**objets de tâche**
</dt> <dd>

Instances d’un objet qui fournit des méthodes pour la gestion des tâches. Cela comprend les méthodes de définition et de récupération des propriétés. exécution, arrêt et suppression de tâches ; et la création de nouveaux déclencheurs et la récupération des anciens déclencheurs.

L’objet de tâche est créé par des appels à [**IScheduledWorkItem :: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) et [**IScheduledWorkItem :: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

</dd> <dt>

<span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**objets du planificateur de tâches**
</dt> <dd>

Instances d’un objet qui représente le service Planificateur de tâches. Cet objet prend en charge deux interfaces : **IUnknown** et [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (actuellement, les tâches sont le seul type d’éléments de travail pris en charge par le service Planificateur de tâches).

Les objets du planificateur de tâches sont créés par des appels à **CoCreateInstance**.

</dd> <dt>

<span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**objets de déclencheur de tâche**
</dt> <dd>

Instances d’un objet fournit des méthodes pour définir et récupérer des déclencheurs de tâche. Cet objet prend en charge deux interfaces : **IUnknown** et [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).

Les objets déclencheurs de tâche sont créés par des appels à [**IScheduledWorkItem :: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) et [**IScheduledWorkItem :: GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

Voir aussi : *déclencheurs*.

</dd> <dt>

<span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**décrites**
</dt> <dd>

Tout élément que l’Planificateur de tâches peut exécuter. Ces éléments peuvent inclure l’un des éléments suivants (pris en charge par le système d’exploitation sur lequel la tâche s’exécute) : Win32® applications, applications Win16, applications OS/2, applications MS-DOS®, fichiers de commandes ( \*.bat), fichiers de commandes ( \* . cmd) ou n’importe quel type de fichier correctement inscrit.

</dd> <dt>

<span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Dossier tâches**
</dt> <dd>

Dossier qui répertorie tous les fichiers de tâches (actuellement, les tâches sont les seuls éléments de travail disponibles). Ces fichiers contiennent des informations sur la tâche. Le nom de ces fichiers reflète le nom de la tâche.

Vous pouvez récupérer l’emplacement du dossier tâches à partir du registre en obtenant les données pour la valeur suivante :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**déclencheurs**
</dt> <dd>

Ensemble de critères qui, lorsqu’il est rempli, entraîne l’exécution d’une tâche. Planificateur de tâches fournit des déclencheurs temporels et basés sur des événements qui peuvent spécifier des heures de début de tâche, des critères de répétition et d’autres paramètres.

</dd> <dt>

<span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**chaînes de déclencheur**
</dt> <dd>

Chaîne qui décrit le déclencheur. Cette chaîne est créée par le service Planificateur de tâches et s’affiche dans l’interface utilisateur Planificateur de tâches dans un format semblable à « à 2PM chaque jour, à partir du 5/11/97. »

</dd> <dt>

<span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**structures de déclencheur**
</dt> <dd>

Structure [**de \_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) utilisée lors de la définition ou de la récupération des critères définissant le déclencheur. Les critères incluent le moment où le déclencheur se déclenche et le type du déclencheur.

</dd> </dl>

 

 




