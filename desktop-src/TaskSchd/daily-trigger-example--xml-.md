---
title: Exemple de déclencheur quotidien (XML)
description: Le code XML de cet exemple définit une tâche qui démarre le bloc-notes à 8 00 AM tous les jours.
ms.assetid: b7818071-12b6-41df-85b9-282c08cf6e31
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe673a764e6e7e4e3ae5089022da2232821d9184
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2020
ms.locfileid: "103679525"
---
# <a name="daily-trigger-example-xml"></a>Exemple de déclencheur quotidien (XML)

Le code XML de cet exemple définit une tâche qui démarre le bloc-notes à 8:00 AM tous les jours. L’exemple montre également comment définir un modèle de répétition pour le déclencheur afin de répéter la tâche.

Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe. Si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ system32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **SCHTASKS/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a>Pour définir une tâche de démarrage du bloc-notes tous les jours à 8:00 AM

L’exemple de code XML suivant montre comment définir une tâche avec une seule action d’exécution (démarrage du bloc-notes), un seul déclencheur de calendrier (démarre la tâche chaque jour à 8:00 AM) et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par Planificateur de tâches.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start on a daily basis.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Notepad starts every day.</Description>
    </RegistrationInfo>
    <Triggers>
        <CalendarTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Repetition>
                <Interval>PT1M</Interval>
                <Duration>PT4M</Duration>
            </Repetition>
            <ScheduleByDay>
                <DaysInterval>1</DaysInterval>
            </ScheduleByDay>
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

    Définit le déclencheur de calendrier quotidien. Dans ce cas, quatre éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé, la planification quotidienne et le modèle de répétition pour la tâche. L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de calendrier.

-   [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    Définit la planification quotidienne. Dans ce cas, l’intervalle est défini pour effectuer la tâche tous les jours.

-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): définit le contexte de sécurité sous lequel une tâche s’exécute.
-   [**Paramètres**](taskschedulerschema-settings-tasktype-element.md)

    Définit les paramètres de tâche que Planificateur de tâches utilise pour effectuer la tâche.

-   [**Actions**](taskschedulerschema-actions-tasktype-element.md)

    Définit les actions exécutées par la tâche (dans ce cas, le bloc-notes).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




