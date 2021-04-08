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
# <a name="daily-trigger-example-xml"></a><span data-ttu-id="2b081-103">Exemple de déclencheur quotidien (XML)</span><span class="sxs-lookup"><span data-stu-id="2b081-103">Daily Trigger Example (XML)</span></span>

<span data-ttu-id="2b081-104">Le code XML de cet exemple définit une tâche qui démarre le bloc-notes à 8:00 AM tous les jours.</span><span class="sxs-lookup"><span data-stu-id="2b081-104">The XML in this example defines a task that starts Notepad at 8:00 AM every day.</span></span> <span data-ttu-id="2b081-105">L’exemple montre également comment définir un modèle de répétition pour le déclencheur afin de répéter la tâche.</span><span class="sxs-lookup"><span data-stu-id="2b081-105">The example also shows how to set a repetition pattern for the trigger to repeat the task.</span></span>

<span data-ttu-id="2b081-106">Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="2b081-106">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="2b081-107">Si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ system32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **SCHTASKS/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="2b081-107">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-day-at-800-am"></a><span data-ttu-id="2b081-108">Pour définir une tâche de démarrage du bloc-notes tous les jours à 8:00 AM</span><span class="sxs-lookup"><span data-stu-id="2b081-108">To define a task to start Notepad every day at 8:00 AM</span></span>

<span data-ttu-id="2b081-109">L’exemple de code XML suivant montre comment définir une tâche avec une seule action d’exécution (démarrage du bloc-notes), un seul déclencheur de calendrier (démarre la tâche chaque jour à 8:00 AM) et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="2b081-109">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every day at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="2b081-110">Éléments du schéma TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="2b081-110">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="2b081-111">Voici quelques éléments importants à prendre en compte lors de l’utilisation de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="2b081-111">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="2b081-112">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="2b081-112">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="2b081-113">Contient les informations d’inscription relatives à la tâche.</span><span class="sxs-lookup"><span data-stu-id="2b081-113">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="2b081-114">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="2b081-114">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="2b081-115">Définit le déclencheur qui démarre la tâche.</span><span class="sxs-lookup"><span data-stu-id="2b081-115">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="2b081-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="2b081-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="2b081-117">Définit le déclencheur de calendrier quotidien.</span><span class="sxs-lookup"><span data-stu-id="2b081-117">Defines the daily calendar trigger.</span></span> <span data-ttu-id="2b081-118">Dans ce cas, quatre éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé, la planification quotidienne et le modèle de répétition pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="2b081-118">In this case, four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the daily schedule, and the repetition pattern for the task.</span></span> <span data-ttu-id="2b081-119">L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de calendrier.</span><span class="sxs-lookup"><span data-stu-id="2b081-119">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="2b081-120">**ScheduleByDay**</span><span class="sxs-lookup"><span data-stu-id="2b081-120">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)

    <span data-ttu-id="2b081-121">Définit la planification quotidienne.</span><span class="sxs-lookup"><span data-stu-id="2b081-121">Defines the daily schedule.</span></span> <span data-ttu-id="2b081-122">Dans ce cas, l’intervalle est défini pour effectuer la tâche tous les jours.</span><span class="sxs-lookup"><span data-stu-id="2b081-122">In this case, the interval is set to perform the task every day.</span></span>

-   <span data-ttu-id="2b081-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): définit le contexte de sécurité sous lequel une tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="2b081-123">[**Principal**](taskschedulerschema-principal-principaltype-element.md): Defines the security context that a task runs under.</span></span>
-   [<span data-ttu-id="2b081-124">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="2b081-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="2b081-125">Définit les paramètres de tâche que Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="2b081-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="2b081-126">**Actions**</span><span class="sxs-lookup"><span data-stu-id="2b081-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="2b081-127">Définit les actions exécutées par la tâche (dans ce cas, le bloc-notes).</span><span class="sxs-lookup"><span data-stu-id="2b081-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b081-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b081-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b081-129">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2b081-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




