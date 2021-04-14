---
title: Exemple de déclencheur hebdomadaire (XML)
description: Le code XML de cet exemple définit une tâche qui démarre le bloc-notes sur une base bihebdomadaire.
ms.assetid: 1911e8b1-2583-440c-a6ed-d71080b60987
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf8c2683311aecc427e9570a0452c746375eca01
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104381366"
---
# <a name="weekly-trigger-example-xml"></a>Exemple de déclencheur hebdomadaire (XML)

Le code XML de cet exemple définit une tâche qui démarre le bloc-notes sur une base bihebdomadaire.

Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe. Si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ system32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **SCHTASKS/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a>Pour définir une tâche de démarrage du bloc-notes toutes les autres semaines le lundi à 8:00 AM

L’exemple de code XML suivant montre comment définir une tâche avec une seule action d’exécution (à partir du bloc-notes), un seul déclencheur de calendrier (démarre la tâche toutes les deux semaines le lundi à 8:00 AM) et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par Planificateur de tâches.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a bi-weekly basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-05-01T09:00:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every other week on Monday at 8:00am.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-05-02T08:00:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00</EndBoundary>
            <ScheduleByWeek>
                <WeeksInterval>2</WeeksInterval>
                <DaysOfWeek>
                    <Monday/>
                </DaysOfWeek>
            </ScheduleByWeek>
        </CalendarTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <UserId>Administrator</UserId>
            <LogonType>InteractiveToken</LogonType>
        </Principal>
    </Principals>
    <Settings>
        <Enabled>true</Enabled>
        <AllowStartOnDemand>true</AllowStartOnDemand>
        <AllowHardTerminate>true</AllowHardTerminate>
    </Settings>
    <Actions>
        <Exec>
            <Command>notepad.exe</Command>
        </Exec>
    </Actions>
</Task>
```



## <a name="taskscheduler-schema-elements"></a>Éléments du schéma TaskScheduler

Voici quelques éléments importants à prendre en compte lors de l’utilisation de cet exemple.

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md)

    Contient les informations d’inscription relatives à la tâche.

-   [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md)

    Définit le déclencheur qui démarre la tâche.

-   [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)

    Définit le déclencheur hebdomadaire du calendrier. Dans ce cas, seuls quatre éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé, la planification hebdomadaire et les jours de la semaine où la tâche sera exécutée. L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de calendrier.

-   [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    Définit la planification hebdomadaire. Dans ce cas, l’intervalle est défini pour effectuer la tâche toutes les deux semaines le lundi.

-   [**Directeur**](taskschedulerschema-principal-principaltype-element.md)

    Définit le contexte de sécurité sous lequel une tâche s’exécute.

-   [**Paramètres**](taskschedulerschema-settings-tasktype-element.md)

    Définit les paramètres de tâche que Planificateur de tâches utilise pour effectuer la tâche.

-   [**Actions**](taskschedulerschema-actions-tasktype-element.md)

    Définit les actions exécutées par la tâche (dans ce cas, le bloc-notes).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




