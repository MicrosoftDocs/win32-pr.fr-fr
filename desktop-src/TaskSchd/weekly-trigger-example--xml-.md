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
# <a name="weekly-trigger-example-xml"></a><span data-ttu-id="0fa1d-103">Exemple de déclencheur hebdomadaire (XML)</span><span class="sxs-lookup"><span data-stu-id="0fa1d-103">Weekly Trigger Example (XML)</span></span>

<span data-ttu-id="0fa1d-104">Le code XML de cet exemple définit une tâche qui démarre le bloc-notes sur une base bihebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-104">The XML in this example defines a task that starts Notepad on a bi-weekly basis.</span></span>

<span data-ttu-id="0fa1d-105">Pour inscrire une tâche définie en XML, vous pouvez utiliser la fonction [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) ([**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour l’écriture de scripts) ou l’outil de ligne de commande Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-105">To register a task that is defined in XML, you can use either the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) function ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) for scripting) or the Schtasks.exe command-line tool.</span></span> <span data-ttu-id="0fa1d-106">Si vous utilisez l’outil Schtasks.exe (situé dans le répertoire C : \\ Windows \\ system32), vous pouvez utiliser la commande suivante pour inscrire la tâche : **SCHTASKS/Create/XML** *<path to the XML file containing the task definition>* **/TN** *<task name>* .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-106">If you use the Schtasks.exe tool (located in the C:\\Windows\\System32 directory), then you can use the following command to register the task: **schtasks /create /XML** *<path to the XML file containing the task definition>* **/tn** *<task name>*.</span></span>

## <a name="to-define-a-task-to-start-notepad-every-other-week-on-monday-at-800-am"></a><span data-ttu-id="0fa1d-107">Pour définir une tâche de démarrage du bloc-notes toutes les autres semaines le lundi à 8:00 AM</span><span class="sxs-lookup"><span data-stu-id="0fa1d-107">To define a task to start Notepad every other week on Monday at 8:00 AM</span></span>

<span data-ttu-id="0fa1d-108">L’exemple de code XML suivant montre comment définir une tâche avec une seule action d’exécution (à partir du bloc-notes), un seul déclencheur de calendrier (démarre la tâche toutes les deux semaines le lundi à 8:00 AM) et plusieurs autres paramètres de tâche qui affectent la façon dont la tâche est gérée par Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-108">The following XML example shows how to define a task with a single execution action (starting Notepad), a single calendar trigger (starts the task every other week on Monday at 8:00 AM), and several other task settings that affect how the task is handled by Task Scheduler.</span></span>


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



## <a name="taskscheduler-schema-elements"></a><span data-ttu-id="0fa1d-109">Éléments du schéma TaskScheduler</span><span class="sxs-lookup"><span data-stu-id="0fa1d-109">TaskScheduler Schema Elements</span></span>

<span data-ttu-id="0fa1d-110">Voici quelques éléments importants à prendre en compte lors de l’utilisation de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-110">Here are some important elements to keep in mind when using this example.</span></span>

-   [<span data-ttu-id="0fa1d-111">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="0fa1d-111">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md)

    <span data-ttu-id="0fa1d-112">Contient les informations d’inscription relatives à la tâche.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-112">Contains registration information about the task.</span></span>

-   [<span data-ttu-id="0fa1d-113">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="0fa1d-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)

    <span data-ttu-id="0fa1d-114">Définit le déclencheur qui démarre la tâche.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-114">Defines the trigger that starts the task.</span></span>

-   [<span data-ttu-id="0fa1d-115">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="0fa1d-115">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)

    <span data-ttu-id="0fa1d-116">Définit le déclencheur hebdomadaire du calendrier.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-116">Defines the weekly calendar trigger.</span></span> <span data-ttu-id="0fa1d-117">Dans ce cas, seuls quatre éléments enfants sont utilisés : les limites de début et de fin qui spécifient le moment où le déclencheur est activé et désactivé, la planification hebdomadaire et les jours de la semaine où la tâche sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-117">In this case, only four child elements are used: the start and end boundaries that specify when the trigger is activated and deactivated, the weekly schedule, and the days of the week that the task will run on.</span></span> <span data-ttu-id="0fa1d-118">L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de calendrier.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-118">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for calendar triggers.</span></span>

-   [<span data-ttu-id="0fa1d-119">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="0fa1d-119">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)

    <span data-ttu-id="0fa1d-120">Définit la planification hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-120">Defines the weekly schedule.</span></span> <span data-ttu-id="0fa1d-121">Dans ce cas, l’intervalle est défini pour effectuer la tâche toutes les deux semaines le lundi.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-121">In this case, the interval is set to perform the task every other week on a Monday.</span></span>

-   [<span data-ttu-id="0fa1d-122">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="0fa1d-122">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md)

    <span data-ttu-id="0fa1d-123">Définit le contexte de sécurité sous lequel une tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-123">Defines the security context that a task runs under.</span></span>

-   [<span data-ttu-id="0fa1d-124">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="0fa1d-124">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)

    <span data-ttu-id="0fa1d-125">Définit les paramètres de tâche que Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-125">Defines the task settings that Task Scheduler uses to perform the task.</span></span>

-   [<span data-ttu-id="0fa1d-126">**Actions**</span><span class="sxs-lookup"><span data-stu-id="0fa1d-126">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)

    <span data-ttu-id="0fa1d-127">Définit les actions exécutées par la tâche (dans ce cas, le bloc-notes).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-127">Defines the actions the task performs (in this case, running Notepad).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fa1d-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0fa1d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fa1d-129">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0fa1d-129">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




