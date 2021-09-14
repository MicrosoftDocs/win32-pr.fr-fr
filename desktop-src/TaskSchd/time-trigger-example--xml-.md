---
title: Exemple de déclencheur de temps (XML)
description: le code XML de cet exemple définit une tâche qui démarre Bloc-notes à un moment donné.
ms.assetid: dde3627b-e268-45ef-9c26-08877bfe484f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c683c831aa3a07eeb3a41db9cd2768caeb6307a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233027"
---
# <a name="time-trigger-example-xml"></a>Exemple de déclencheur de temps (XML)

le code XML de cet exemple définit une tâche qui démarre Bloc-notes à un moment donné.

Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe. si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ System32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **schtasks/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-at-a-specific-time"></a>pour définir une tâche afin qu’elle démarre Bloc-notes à un moment donné

l’exemple de code XML suivant montre comment définir une tâche avec une action d’exécution unique (à partir de Bloc-notes), un déclencheur à temps unique qui démarre la tâche à une heure spécifiée et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par l’Planificateur de tâches.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe at a specific time.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after at a specified time.</Description>
    </RegistrationInfo>
    <Triggers>
        <TimeTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </TimeTrigger>
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

Voici quelques éléments importants à prendre en compte lors de l’utilisation de cet exemple :

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contient les informations d’inscription relatives à la tâche.
-   [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md): définit le déclencheur qui démarre la tâche.
-   [**Timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md): définit le déclencheur d’heure. Dans ce cas, trois éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé, et le délai d’exécution qui spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur. L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de temps.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): définit le contexte de sécurité sous lequel une tâche s’exécute.
-   [**Paramètres**](taskschedulerschema-settings-tasktype-element.md): définit les paramètres de tâche que le Planificateur de tâches utilise pour effectuer la tâche.
-   [**actions**](taskschedulerschema-actions-tasktype-element.md): définit les actions exécutées par la tâche (dans ce cas, en cours d’exécution Bloc-notes).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




