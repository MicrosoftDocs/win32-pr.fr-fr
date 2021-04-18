---
title: Exemple de déclencheur d’inscription (XML)
description: Le code XML de cet exemple définit une tâche qui démarre le bloc-notes lorsque la tâche est inscrite.
ms.assetid: 976b9767-635f-42a6-84f5-7e0203478594
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09b9193f3b63f21464811609e8f5f19017539ecd
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2020
ms.locfileid: "106512711"
---
# <a name="registration-trigger-example-xml"></a><span data-ttu-id="404c4-103">Exemple de déclencheur d’inscription (XML)</span><span class="sxs-lookup"><span data-stu-id="404c4-103">Registration Trigger Example (XML)</span></span>

<span data-ttu-id="404c4-104">Le code XML de cet exemple définit une tâche qui démarre le bloc-notes lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="404c4-104">The XML in this example defines a task that starts Notepad when the task is registered.</span></span>

<span data-ttu-id="404c4-105">Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="404c4-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="404c4-106">Si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ system32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **SCHTASKS/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="404c4-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

> [!Note]  
> <span data-ttu-id="404c4-107">Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.</span><span class="sxs-lookup"><span data-stu-id="404c4-107">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="to-define-a-task-to-start-notepad-on-registration"></a><span data-ttu-id="404c4-108">Pour définir une tâche de démarrage du bloc-notes lors de l’inscription</span><span class="sxs-lookup"><span data-stu-id="404c4-108">To define a task to start Notepad on registration</span></span>

<span data-ttu-id="404c4-109">L’exemple de code XML suivant montre comment définir une tâche à l’aide d’une action d’exécution unique (démarrage du bloc-notes), d’un déclencheur d’inscription unique qui démarre la tâche lorsqu’elle est inscrite et de plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par le Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="404c4-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single registration trigger that starts the task when it is registered, and several other task settings that affect how the task is handled by the Task Scheduler.</span></span>

> [!Note]  
> <span data-ttu-id="404c4-110">Quand une tâche avec un déclencheur d’inscription est mise à jour, la tâche s’exécute une fois la mise à jour effectuée.</span><span class="sxs-lookup"><span data-stu-id="404c4-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 


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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="404c4-111">Éléments du schéma TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="404c4-111">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="404c4-112">Voici quelques éléments importants à prendre en compte lors de l’utilisation de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="404c4-112">Here are some important elements to keep in mind when using this example.</span></span>

-   <span data-ttu-id="404c4-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): contient les informations d’inscription relatives à la tâche.</span><span class="sxs-lookup"><span data-stu-id="404c4-113">[**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md): Contains registration information about the task.</span></span>
-   <span data-ttu-id="404c4-114">[**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md): définit le déclencheur qui démarre la tâche.</span><span class="sxs-lookup"><span data-stu-id="404c4-114">[**Triggers**](taskschedulerschema-triggers-tasktype-element.md): Defines the trigger that starts the task.</span></span>
-   <span data-ttu-id="404c4-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): définit le déclencheur d’inscription.</span><span class="sxs-lookup"><span data-stu-id="404c4-115">[**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md): Defines the registration trigger.</span></span> <span data-ttu-id="404c4-116">Dans ce cas, seuls deux éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé.</span><span class="sxs-lookup"><span data-stu-id="404c4-116">In this case, only two child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated.</span></span>
-   <span data-ttu-id="404c4-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): définit le contexte de sécurité sous lequel une tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="404c4-117">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   <span data-ttu-id="404c4-118">[**Paramètres**](taskschedulerschema-settings-tasktype-element.md): définit les paramètres de tâche que le planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="404c4-118">[**Settings**](taskschedulerschema-settings-tasktype-element.md): Defines the task settings that the Task Scheduler uses to perform the task.</span></span>
-   <span data-ttu-id="404c4-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): définit les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="404c4-119">[**Actions**](taskschedulerschema-actions-tasktype-element.md): Defines the actions the task performs.</span></span> <span data-ttu-id="404c4-120">Dans ce cas, exécutez le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="404c4-120">In this case, running Notepad.</span></span>

## <a name="related-topics"></a><span data-ttu-id="404c4-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="404c4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="404c4-122">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="404c4-122">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




