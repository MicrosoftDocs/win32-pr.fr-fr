---
title: Exemple de déclencheur de démarrage (XML)
description: Le code XML de cet exemple définit une tâche qui démarre le bloc-notes au démarrage du système.
ms.assetid: 6dd7155c-6163-4408-9cef-c313134beeb0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8f9f5ea10f92979b0798b12a6225f8ba74a38ee
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104314059"
---
# <a name="boot-trigger-example-xml"></a>Exemple de déclencheur de démarrage (XML)

Le code XML de cet exemple définit une tâche qui démarre le bloc-notes au démarrage du système.

Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe. Si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ system32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **SCHTASKS/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a>Pour définir une tâche de démarrage du bloc-notes au démarrage du système

L’exemple de code XML suivant montre comment définir une tâche avec une seule action d’exécution (démarrage du bloc-notes), un seul déclencheur de démarrage qui démarre la tâche lorsque le système est démarré et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par le Planificateur de tâches.


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the system is booted.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad on system boot.</Description>
    </RegistrationInfo>
    <Triggers>
        <BootTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <ExecutionTimeLimit>PT5M</ExecutionTimeLimit>
        </BootTrigger>
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

-   [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contient les informations d’inscription relatives à la tâche.
-   [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md): définit le déclencheur qui démarre la tâche.
-   [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): définit le déclencheur de démarrage. Dans ce cas, seuls deux éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): définit le contexte de sécurité sous lequel une tâche s’exécute.
-   [**Paramètres**](taskschedulerschema-settings-tasktype-element.md): définit les paramètres de tâche que le planificateur de tâches utilise pour effectuer la tâche.
-   [**Actions**](taskschedulerschema-actions-tasktype-element.md): définit les actions effectuées par la tâche. Dans ce cas, exécutez le bloc-notes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




