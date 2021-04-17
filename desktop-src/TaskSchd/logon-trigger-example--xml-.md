---
title: Exemple de déclencheur LOGON (XML)
description: Le code XML de cet exemple définit une tâche qui démarre le bloc-notes lorsqu’un utilisateur ouvre une session.
ms.assetid: c1cce95f-7558-489e-b092-c82d55b42165
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d66766ce4cae33c3526ac9d30071ff2082ddc1f2
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104381372"
---
# <a name="logon-trigger-example-xml"></a><span data-ttu-id="fa9f5-103">Exemple de déclencheur LOGON (XML)</span><span class="sxs-lookup"><span data-stu-id="fa9f5-103">Logon Trigger Example (XML)</span></span>

<span data-ttu-id="fa9f5-104">Le code XML de cet exemple définit une tâche qui démarre le bloc-notes lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-104">The XML in this example defines a task that starts Notepad when a user logs on.</span></span>

<span data-ttu-id="fa9f5-105">Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="fa9f5-106">Si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ system32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **SCHTASKS/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="fa9f5-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="fa9f5-107">Pour définir une tâche de démarrage du bloc-notes au démarrage du système</span><span class="sxs-lookup"><span data-stu-id="fa9f5-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="fa9f5-108">L’exemple de code XML suivant montre comment définir une tâche avec une action d’exécution unique (démarrage du bloc-notes), un déclencheur d’ouverture de session unique qui démarre la tâche lorsqu’un utilisateur ouvre une session et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single logon trigger that starts the task when a user logs on, and several other task settings that affect how the task is handled by Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="fa9f5-109">Définissez la valeur de l’élément **userid** sur un nom d’utilisateur sur l’ordinateur sur lequel la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-109">Set the value of the **UserId** element to a user name on the computer on which the task is registered.</span></span>

 


```XML
<?xml version="1.0" ?>
<!--
This sample schedules a task to start notepad.exe when a user logs on.
-->
<Task xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
    <RegistrationInfo>
        <Date>2005-10-11T13:21:17-08:00</Date>
        <Author>AuthorName</Author>
        <Version>1.0.0</Version>
        <Description>Starts Notepad when a specified user logs on.</Description>
    </RegistrationInfo>
    <Triggers>
        <LogonTrigger>
            <StartBoundary>2005-10-11T13:21:17-08:00</StartBoundary>
            <EndBoundary>2006-01-01T00:00:00-08:00</EndBoundary>
            <Enabled>true</Enabled>
            <UserId>DOMAIN_NAME\UserName</UserId>
        </LogonTrigger>
    </Triggers>
    <Principals>
        <Principal>
            <GroupId>Builtin\Administrators</GroupId>
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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="fa9f5-110">Éléments du schéma TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="fa9f5-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="fa9f5-111">Voici quelques éléments importants à prendre en compte lors de l’utilisation de cet exemple :</span><span class="sxs-lookup"><span data-stu-id="fa9f5-111">The following are some important elements to keep in mind when using this example:</span></span>

-   <span data-ttu-id="fa9f5-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contient les informations d’inscription relatives à la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-112">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="fa9f5-113">[**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md): définit le déclencheur qui démarre la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-113">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="fa9f5-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): définit le déclencheur Logon.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-114">[**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md): Defines the logon trigger.</span></span> <span data-ttu-id="fa9f5-115">Dans ce cas, trois éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé, et l’élément [**userid**](taskschedulerschema-userid-logontriggertype-element.md) qui identifie l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-115">In this case, three child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, and the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element that identifier of the user.</span></span> <span data-ttu-id="fa9f5-116">La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-116">The task is started when this user logs on to the computer..</span></span>
-   <span data-ttu-id="fa9f5-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): définit le contexte de sécurité sous lequel une tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="fa9f5-118">[**Paramètres**](taskschedulerschema-settings-tasktype-element.md): définit les paramètres de tâche que le planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="fa9f5-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): définit les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="fa9f5-120">Dans ce cas, exécutez le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="fa9f5-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa9f5-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fa9f5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa9f5-122">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="fa9f5-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




