---
title: Interfaces de déclencheur
description: Les API utilisées pour gérer les déclencheurs varient en fonction de la version de la Planificateur de tâches. Toutefois, dans les deux cas, ces API vous permettent de créer des déclencheurs, de récupérer et de mettre à jour des déclencheurs existants et de supprimer des déclencheurs qui ne sont plus nécessaires.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- déclencheurs Planificateur de tâches, interfaces
- déclencheurs Planificateur de tâches, interfaces, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5515f2b1e2f5b4a7694dec28bb8831c690da0d303cda53338714c1b0e03ddaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002183"
---
# <a name="trigger-interfaces"></a>Interfaces de déclencheur

Les API utilisées pour gérer les déclencheurs varient en fonction de la version de la Planificateur de tâches. Toutefois, dans les deux cas, ces API vous permettent de créer des déclencheurs, de récupérer et de mettre à jour des déclencheurs existants et de supprimer des déclencheurs qui ne sont plus nécessaires.


Les applications développées à l’aide de Planificateur de tâches 2,0 peuvent utiliser des objets et des interfaces pour créer, récupérer, modifier et supprimer les déclencheurs d’une tâche.

Dans l’illustration suivante, une tâche spécifie une collection de déclencheurs à l’aide de sa propriété déclencheurs. Cette collection contient une ou plusieurs API de déclencheur individuelles avec chaque API spécifiant un type de déclencheur spécifique. Par exemple, dans l’illustration ci-dessous, la collection de déclencheurs contient un déclencheur de démarrage, un déclencheur d’ouverture de session et un déclencheur quotidien.

![interfaces de déclencheur du planificateur de tâches 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>API d’objet pour le développement de scripts

Pour plus d’informations sur les méthodes et les propriétés des objets utilisés pour spécifier des déclencheurs, consultez :

-   [**TaskDefinition**](taskdefinition.md)
-   [**TriggerCollection**](triggercollection.md)
-   [**Déclencheur**](trigger.md)
-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a>Interfaces API pour le développement C++

Pour plus d’informations sur les méthodes et les propriétés des interfaces utilisées pour spécifier des déclencheurs, consultez :

-   [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [**ITrigger**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a>Interfaces de déclencheur Planificateur de tâches 1,0

Les applications existantes développées à l’aide de Planificateur de tâches 1,0 peuvent utiliser les méthodes disponibles à partir des interfaces Planificateur de tâches 1,0 pour créer, récupérer, modifier et supprimer les déclencheurs d’un [*élément de travail*](w.md). Toutefois, Notez que toutes les interfaces, énumérations et structures Planificateur de tâches 1,0 sont obsolètes et ne doivent pas être utilisées pour le développement de nouvelles applications.

Les deux interfaces utilisées pour effectuer cette opération sont présentées dans l’illustration suivante. L’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) est utilisée pour gérer tous les déclencheurs associés à un élément de travail (ce type de gestion comprend la création d’un déclencheur pour l’élément de travail). L’interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) est utilisée pour gérer un déclencheur spécifique.

![interfaces de déclencheur du planificateur de tâches 1,0](images/tsktri2.png)

L’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fournit des méthodes pour créer un déclencheur pour un élément de travail, récupérer le nombre de déclencheurs associés à un élément de travail, récupérer les [*structures de déclencheur*](t.md) associées à l’élément de travail, récupérer les [*chaînes de déclencheur*](t.md) associées à l’élément de travail et supprimer des déclencheurs.

Une fois que l’objet déclencheur est disponible, vous pouvez utiliser l’interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) pour récupérer la structure du déclencheur et la chaîne du déclencheur et pour définir les critères utilisés pour activer le déclencheur. Cette interface est utilisée uniquement lorsque vous travaillez avec un [*objet déclencheur de tâche*](t.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclencheurs de tâche](task-triggers.md)
</dt> <dt>

[Types de déclencheurs](trigger-types.md)
</dt> <dt>

[Structures de déclencheur](trigger-structures.md)
</dt> </dl>

 

 