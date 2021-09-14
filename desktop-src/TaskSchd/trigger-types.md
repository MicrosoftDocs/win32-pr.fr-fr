---
title: Types de déclencheurs
description: Les déclencheurs basés sur l’heure et les événements qui sont décrits ci-dessous vous permettent de démarrer des tâches de différentes façons.
ms.assetid: 2f577103-3892-49ce-9a3b-7a4839da8a83
keywords:
- déclencheurs Planificateur de tâches, types
- déclencheur de démarrage Planificateur de tâches
- Planificateur de tâches de déclencheur de démarrage, Description
- Planificateur de tâches du déclencheur d’inscription
- Planificateur de tâches de déclencheur d’inscription, Description
- déclencheur de calendrier Planificateur de tâches
- Planificateur de tâches de déclencheur de calendrier, Description
- Planificateur de tâches de déclencheur quotidien
- Planificateur de tâches de déclencheur quotidien, Description
- déclencheur hebdomadaire Planificateur de tâches
- Planificateur de tâches de déclencheur hebdomadaire, Description
- Planificateur de tâches de déclencheur mensuelle
- Planificateur de tâches de déclencheur mensuel, Description
- déclencheur monthlyDOW Planificateur de tâches
- Planificateur de tâches du déclencheur monthlyDOW, décrit
- déclencheur d’événements Planificateur de tâches
- Planificateur de tâches du déclencheur d’événements, décrit
- déclencheur de connexion Planificateur de tâches
- Planificateur de tâches de déclencheur de connexion, Description
- Planificateur de tâches de déclencheur inactif
- Planificateur de tâches de déclencheur inactif, Description
- Planificateur de tâches du déclencheur de jour de la semaine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee1e846e4b2fa8138f675cdd39e926884d2bfae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857247"
---
# <a name="trigger-types"></a>Types de déclencheurs

Les déclencheurs basés sur l’heure et les événements qui sont décrits ci-dessous vous permettent de démarrer des tâches de différentes façons.

## <a name="task-scheduler-20-triggers"></a>Déclencheurs Planificateur de tâches 2,0

Les types de déclencheurs suivants sont définis par l’énumération [**\_ \_ type2 du déclencheur de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .

| Déclencheur                                                                                                                                                                                                                                                                                                                                                                                                                | Description                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Déclencheur d’événements (déclencheur basé sur les événements) pour le développement de scripts, consultez [**EventTrigger**](eventtrigger.md).<br/> Pour le développement C++, consultez [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger).<br/> Pour le développement XML, consultez l' [**élément EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md).<br/>                                                                                             | Démarre la tâche lorsqu’un événement système spécifique se produit.                                                                                                                                         |
| Déclencheur de temps (déclencheur basé sur l’heure) pour le développement de scripts, consultez [**timetrigger**](timetrigger.md).<br/> Pour le développement C++, consultez [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger).<br/> Pour le développement XML, consultez [**élément timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md).<br/>                                                                                                      | Démarre la tâche à une date et une heure spécifiques.                                                                                                                                                 |
| Déclencheur quotidien (déclencheur de calendrier basé sur le temps) pour le développement de scripts, consultez [**DailyTrigger**](dailytrigger.md).<br/> Pour le développement C++, consultez [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger).<br/> Pour le développement XML, consultez [**élément CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                                | Démarre la tâche à une heure spécifique selon une planification quotidienne. Par exemple, la tâche commence à 8:00 AM tous les jours ou tous les jours.                                                                |
| Déclencheur hebdomadaire (déclencheur de calendrier basé sur le temps) pour le développement de scripts, consultez [**WeeklyTrigger**](weeklytrigger.md).<br/> Pour le développement C++, consultez [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger).<br/> Pour le développement XML, consultez [**élément CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                           | Démarre la tâche à une heure spécifique selon une planification hebdomadaire. Par exemple, la tâche commence à 8:00 AM un jour spécifique de la semaine chaque semaine ou un jour spécifique de la semaine chaque semaine. |
| Déclencheur mensuel (déclencheur de calendrier basé sur le temps) pour le développement de scripts, consultez [**MonthlyTrigger**](monthlytrigger.md).<br/> Pour le développement C++, consultez [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger).<br/> Pour le développement XML, consultez [**élément CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                                                      | Démarre la tâche à une heure spécifique selon une planification mensuelle. Par exemple, la tâche commence à 8:00 AM sur des jours spécifiques du mois sur des mois spécifiques.                                          |
| Déclencheur de jour de semaine (DOW) mensuel (déclencheur de calendrier basé sur le temps) pour le développement de scripts, consultez [**MonthlyDOWTrigger**](monthlydowtrigger.md).<br/> Pour le développement C++, consultez [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger).<br/> Pour le développement XML, consultez [**élément CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md).<br/>                                        | Démarre la tâche à une heure spécifique selon une planification mensuelle de jour de la semaine. Par exemple, la tâche commence à 8:00 AM sur des jours spécifiques de la semaine, des semaines du mois et des mois de l’année.      |
| Déclencheur inactif (déclencheur basé sur les événements) pour le développement de scripts, consultez [**IdleTrigger**](idletrigger.md).<br/> Pour le développement C++, consultez [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger).<br/> Pour le développement XML, consultez [**élément IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md).<br/>                                                                                                     | Démarre la tâche lorsque l’ordinateur passe à l’état inactif.                                                                                                                                      |
| Déclencheur d’inscription (déclencheur basé sur les événements) pour le développement de scripts, consultez [**RegistrationTrigger**](registrationtrigger.md).<br/> Pour le développement C++, consultez [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger).<br/> Pour le développement XML, consultez [**élément RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md).<br/>                                             | Démarre la tâche lorsque la tâche est inscrite ou mise à jour.                                                                                                                                      |
| Déclencheur de démarrage (déclencheur basé sur les événements) pour le développement de scripts, consultez [**BootTrigger**](boottrigger.md).<br/> Pour le développement C++, consultez [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger).<br/> Pour le développement XML, consultez [**élément BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md).<br/>                                                                                                     | Démarre la tâche lors du démarrage du système.                                                                                                                                                   |
| Déclencheur d’ouverture de session (déclencheur basé sur les événements) pour le développement de scripts, consultez [**LogonTrigger**](logontrigger.md).<br/> Pour le développement C++, consultez [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger).<br/> Pour le développement XML, consultez [**élément LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md).<br/>                                                                                              | Démarre la tâche lorsqu’un utilisateur ouvre une session.                                                                                                                                                         |
| Déclencheur de changement d’état de session (déclencheur basé sur les événements) pour le développement de scripts, consultez [**SessionStateChangeTrigger**](sessionstatechangetrigger.md).<br/> Pour le développement C++, consultez [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger).<br/> Pour le développement XML, consultez [**élément SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md).<br/> | Démarre la tâche quand une session de Terminal Server change d’État.                                                                                                                                |



 

## <a name="task-scheduler-10-triggers"></a>Déclencheurs Planificateur de tâches 1,0

Les types de déclencheurs suivants sont définis par l’énumération de [**\_ \_ type de déclencheur de tâche**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) . Pour implémenter l’un des déclencheurs suivants, consultez la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .

-   Déclencheur once : démarre la tâche une seule fois.
-   Déclencheur quotidien : démarre la tâche sur un intervalle quotidien.
-   Déclencheur hebdomadaire : démarre la tâche selon une planification hebdomadaire.
-   Déclencheur mensuel : démarre la tâche selon une planification mensuelle.
-   Déclencheur DOW mensuel : démarre la tâche selon une planification mensuelle de jour de semaine.
-   Déclencheur inactif : démarre la tâche lorsque l’ordinateur est dans un état d’inactivité.
-   Déclencheur de démarrage système : démarre la tâche lors du démarrage de l’ordinateur.
-   Déclencheur d’ouverture de session : démarre la tâche lorsqu’un utilisateur spécifique ouvre une session.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclencheurs de tâche](task-triggers.md)
</dt> <dt>

[Interfaces de déclencheur](trigger-interfaces.md)
</dt> <dt>

[Structures de déclencheur](trigger-structures.md)
</dt> </dl>

 

