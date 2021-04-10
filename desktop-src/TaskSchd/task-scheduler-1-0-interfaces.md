---
title: Interfaces Planificateur de tâches 1,0
description: Les interfaces décrites dans les rubriques suivantes fournissent un accès par programme aux fonctionnalités disponibles dans le Planificateur de tâches utilisé dans les systèmes d’exploitation Windows 2000, Windows XP et Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104199920"
---
# <a name="task-scheduler-10-interfaces"></a><span data-ttu-id="ca12a-103">Interfaces Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="ca12a-103">Task Scheduler 1.0 Interfaces</span></span>

<span data-ttu-id="ca12a-104">\[\[Cette API peut être modifiée ou indisponible dans les versions ultérieures du système d’exploitation ou du produit.</span><span class="sxs-lookup"><span data-stu-id="ca12a-104">\[\[This API may be altered or unavailable in subsequent versions of the operating system or product.</span></span> <span data-ttu-id="ca12a-105">Utilisez à la place les [Interfaces Planificateur de tâches 2,0](task-scheduler-2-0-interfaces.md) ou [Planificateur de tâches 2,0](task-scheduler-2-0-enumerated-types.md) . \]\]</span><span class="sxs-lookup"><span data-stu-id="ca12a-105">Please use the [Task Scheduler 2.0 Interfaces](task-scheduler-2-0-interfaces.md) or [Task Scheduler 2.0 Enumerated Types](task-scheduler-2-0-enumerated-types.md) instead.\] \]</span></span>

<span data-ttu-id="ca12a-106">Les interfaces décrites dans les rubriques suivantes fournissent un accès par programme aux fonctionnalités disponibles dans le Planificateur de tâches utilisé dans les systèmes d’exploitation Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ca12a-106">The interfaces that are described in the following topics provide programmatic access to the functionality that is available within the Task Scheduler that is used in the Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="ca12a-107">Ces rubriques contiennent une description de l’interface, une liste des propriétés et des méthodes définies par l’interface, ainsi que des remarques sur les circonstances spéciales qui doivent être notées lors de l’utilisation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="ca12a-107">These topics contain a description of the interface, a list of the properties and methods defined by the interface, and remarks about any special circumstances that should be noted when using the interface.</span></span>


<span data-ttu-id="ca12a-108">Les interfaces suivantes sont introduites par Planificateur de tâches 1,0.</span><span class="sxs-lookup"><span data-stu-id="ca12a-108">The following interfaces are introduced by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="ca12a-109">Interface</span><span class="sxs-lookup"><span data-stu-id="ca12a-109">Interface</span></span>                                        | <span data-ttu-id="ca12a-110">Description</span><span class="sxs-lookup"><span data-stu-id="ca12a-110">Description</span></span>                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca12a-111">**IEnumWorkItems**</span><span class="sxs-lookup"><span data-stu-id="ca12a-111">**IEnumWorkItems**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | <span data-ttu-id="ca12a-112">Fournit les méthodes pour énumérer les tâches dans le [*dossier tâches planifiées*](s.md).</span><span class="sxs-lookup"><span data-stu-id="ca12a-112">Provides the methods for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>                                                                                                              |
| [<span data-ttu-id="ca12a-113">**IProvideTaskPage**</span><span class="sxs-lookup"><span data-stu-id="ca12a-113">**IProvideTaskPage**</span></span>](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | <span data-ttu-id="ca12a-114">Fournit les méthodes pour accéder aux paramètres de la feuille de propriétés d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="ca12a-114">Provides the methods to access the property sheet settings of a task.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="ca12a-115">**IScheduledWorkItem**</span><span class="sxs-lookup"><span data-stu-id="ca12a-115">**IScheduledWorkItem**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | <span data-ttu-id="ca12a-116">Fournit les méthodes pour la gestion d' [*éléments de travail*](w.md)spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ca12a-116">Provides the methods for managing specific [*work items*](w.md).</span></span>                                                                                                                                                 |
| [<span data-ttu-id="ca12a-117">**ITask**</span><span class="sxs-lookup"><span data-stu-id="ca12a-117">**ITask**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itask)                           | <span data-ttu-id="ca12a-118">Fournit les méthodes permettant d’exécuter des tâches, d’obtenir ou de définir des informations sur les tâches et d’arrêter des tâches.</span><span class="sxs-lookup"><span data-stu-id="ca12a-118">Provides the methods for running tasks, getting or setting task information, and terminating tasks.</span></span> <span data-ttu-id="ca12a-119">Elle est dérivée de l’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) et hérite de toutes les méthodes de cette interface.</span><span class="sxs-lookup"><span data-stu-id="ca12a-119">It is derived from the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface and inherits all the methods of that interface.</span></span> |
| [<span data-ttu-id="ca12a-120">**ITaskScheduler**</span><span class="sxs-lookup"><span data-stu-id="ca12a-120">**ITaskScheduler**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | <span data-ttu-id="ca12a-121">Fournit les méthodes de planification des tâches.</span><span class="sxs-lookup"><span data-stu-id="ca12a-121">Provides the methods for scheduling tasks.</span></span>                                                                                                                                                                                            |
| [<span data-ttu-id="ca12a-122">**ITaskTrigger**</span><span class="sxs-lookup"><span data-stu-id="ca12a-122">**ITaskTrigger**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | <span data-ttu-id="ca12a-123">Fournit les méthodes permettant d’accéder aux déclencheurs d’une tâche et de les définir.</span><span class="sxs-lookup"><span data-stu-id="ca12a-123">Provides the methods for accessing and setting triggers for a task.</span></span> <span data-ttu-id="ca12a-124">Les déclencheurs spécifient les heures de début de tâche, les critères de répétition et d’autres paramètres qui contrôlent le moment où une tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="ca12a-124">Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.</span></span>                                                     |



 

 

 




