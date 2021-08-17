---
title: Exemple de déclencheur d’inscription (XML)
description: le code XML de cet exemple définit une tâche qui démarre Bloc-notes lorsque la tâche est inscrite.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b111f5c8c0801bb404e12cee20faf19208d7372d1a3980f7368c6efd2bcbfd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759580"
---
# <a name="registration-trigger-example-xml"></a>Exemple de déclencheur d’inscription (XML)

le code XML de cet exemple définit une tâche qui démarre Bloc-notes lorsque la tâche est inscrite.

Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe. si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ System32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **schtasks/create/xml** *<path to the XML file containing the task definition>* **/tn** *<task name>* .

> [!Note]  
> Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a>pour définir une tâche afin de démarrer Bloc-notes lors de l’inscription

l’exemple de code XML suivant montre comment définir une tâche avec une action d’exécution unique (à partir de Bloc-notes), un déclencheur d’inscription unique qui démarre la tâche lorsqu’elle est inscrite et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par l’Planificateur de tâches.

> [!Note]  
> Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when
the task is registered.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Task starts after registration.</Description>
    </RegistrationInfo>
    <Triggers>
        <RegistrationTrigger>
        </RegistrationTrigger>
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
-   [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): définit le déclencheur d’inscription. Dans ce cas, seuls deux éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé.
-   [**Principal**](taskschedulerschema-principal-principaltype-element.md): définit le contexte de sécurité sous lequel une tâche s’exécute.
-   [**Paramètres**](taskschedulerschema-settings-tasktype-element.md): définit les paramètres de tâche que le Planificateur de tâches utilise pour effectuer la tâche.
-   [**Actions**](taskschedulerschema-actions-tasktype-element.md): définit les actions effectuées par la tâche. dans ce cas, l’exécution de Bloc-notes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’Planificateur de tâches](using-the-task-scheduler.md)
</dt> </dl>

 

 




