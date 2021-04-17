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
# <a name="boot-trigger-example-xml"></a><span data-ttu-id="9c2de-103">Exemple de déclencheur de démarrage (XML)</span><span class="sxs-lookup"><span data-stu-id="9c2de-103">Boot Trigger Example (XML)</span></span>

<span data-ttu-id="9c2de-104">Le code XML de cet exemple définit une tâche qui démarre le bloc-notes au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="9c2de-104">The XML in this example defines a task that starts Notepad when the system is booted.</span></span>

<span data-ttu-id="9c2de-105">Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="9c2de-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="9c2de-106">Si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ system32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **SCHTASKS/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="9c2de-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-on-system-boot"></a><span data-ttu-id="9c2de-107">Pour définir une tâche de démarrage du bloc-notes au démarrage du système</span><span class="sxs-lookup"><span data-stu-id="9c2de-107">To define a task to start Notepad on system boot</span></span>

<span data-ttu-id="9c2de-108">L’exemple de code XML suivant montre comment définir une tâche avec une seule action d’exécution (démarrage du bloc-notes), un seul déclencheur de démarrage qui démarre la tâche lorsque le système est démarré et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par le Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="9c2de-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single boot trigger that starts the task when the system is booted, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>


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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="9c2de-109">Éléments du schéma TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="9c2de-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="9c2de-110">Voici quelques éléments importants à prendre en compte lors de l’utilisation de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="9c2de-110">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="9c2de-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contient les informations d’inscription relatives à la tâche.</span><span class="sxs-lookup"><span data-stu-id="9c2de-111">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="9c2de-112">[**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md): définit le déclencheur qui démarre la tâche.</span><span class="sxs-lookup"><span data-stu-id="9c2de-112">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="9c2de-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): définit le déclencheur de démarrage.</span><span class="sxs-lookup"><span data-stu-id="9c2de-113">[**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md): Defines the boot trigger.</span></span> <span data-ttu-id="9c2de-114">Dans ce cas, seuls deux éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé.</span><span class="sxs-lookup"><span data-stu-id="9c2de-114">In this case only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="9c2de-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): définit le contexte de sécurité sous lequel une tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="9c2de-115">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="9c2de-116">[**Paramètres**](taskschedulerschema-settings-tasktype-element.md): définit les paramètres de tâche que le planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="9c2de-116">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="9c2de-117">[**Actions**](taskschedulerschema-actions-tasktype-element.md): définit les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="9c2de-117">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="9c2de-118">Dans ce cas, exécutez le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="9c2de-118">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c2de-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c2de-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c2de-120">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="9c2de-120">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




