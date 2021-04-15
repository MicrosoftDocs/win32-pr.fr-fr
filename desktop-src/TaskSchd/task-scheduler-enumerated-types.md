---
title: Types énumérés Planificateur de tâches
description: Répertorie les énumérations utilisées par les API Planificateur de tâches.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Planificateur de tâches Planificateur de tâches, référence, types énumérés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508209"
---
# <a name="task-scheduler-enumerated-types"></a><span data-ttu-id="f9537-104">Types énumérés Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f9537-104">Task Scheduler Enumerated Types</span></span>

<span data-ttu-id="f9537-105">Décrit les types énumérés qui définissent les constantes utilisées par les API Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="f9537-105">Describes the enumerated types that define the constants that are used by the Task Scheduler APIs.</span></span>


<span data-ttu-id="f9537-106">Les types énumérés suivants sont introduits dans Planificateur de tâches 2,0.</span><span class="sxs-lookup"><span data-stu-id="f9537-106">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="f9537-107">Énumération</span><span class="sxs-lookup"><span data-stu-id="f9537-107">Enumeration</span></span>                                                                  | <span data-ttu-id="f9537-108">Description</span><span class="sxs-lookup"><span data-stu-id="f9537-108">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9537-109">**\_type d’action de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-109">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="f9537-110">Définit le type d’actions qu’une tâche peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="f9537-110">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="f9537-111">**compatibilité des tâches \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-111">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="f9537-112">Définit les versions de Planificateur de tâches ou la commande AT à laquelle la tâche est compatible.</span><span class="sxs-lookup"><span data-stu-id="f9537-112">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="f9537-113">**création de tâches \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-113">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="f9537-114">Définit le mode de création, de mise à jour ou de désactivation de la tâche par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="f9537-114">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="f9537-115">**\_indicateurs d’énumération de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-115">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="f9537-116">Définit le mode d’énumération du Planificateur de tâches par le biais des tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="f9537-116">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="f9537-117">**\_stratégie d’instances de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-117">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="f9537-118">Définit comment le Planificateur de tâches gère les instances existantes de la tâche lorsqu’il démarre une nouvelle instance de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f9537-118">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="f9537-119">**TYPE de connexion à la tâche \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-119">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="f9537-120">Définit la technique d’ouverture de session requise pour exécuter une tâche.</span><span class="sxs-lookup"><span data-stu-id="f9537-120">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="f9537-121">**TYPE de PROCESSTOKENSID de la tâche \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-121">**TASK\_PROCESSTOKENSID TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | <span data-ttu-id="f9537-122">Définit les types de SID de processus qui peuvent être utilisés par les tâches.</span><span class="sxs-lookup"><span data-stu-id="f9537-122">Defines the types of process SID that can used by tasks.</span></span>                                                         |
| [<span data-ttu-id="f9537-123">**\_indicateurs d’exécution de tâches \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-123">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="f9537-124">Définit le mode d’exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="f9537-124">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="f9537-125">**\_type de RUNLEVEL de la tâche \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-125">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="f9537-126">Définit les indicateurs d’élévation LUA qui spécifient avec quel niveau de privilège la tâche sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="f9537-126">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="f9537-127">**\_type de \_ changement d’état de session de tâche \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-127">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="f9537-128">Définit les genres de Terminal Server modification de l’état de session que vous pouvez utiliser pour déclencher l’exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="f9537-128">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="f9537-129">**État de la tâche \_**</span><span class="sxs-lookup"><span data-stu-id="f9537-129">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="f9537-130">Définit les différents États dans lesquels une tâche inscrite peut se trouver.</span><span class="sxs-lookup"><span data-stu-id="f9537-130">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="f9537-131">**\_Déclencheur de tâche \_ type2**</span><span class="sxs-lookup"><span data-stu-id="f9537-131">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="f9537-132">Définit le type de déclencheur qui peut être utilisé par les tâches.</span><span class="sxs-lookup"><span data-stu-id="f9537-132">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 


> [!WARNING]
> <span data-ttu-id="f9537-133">Les énumérations Planificateur de tâches 1,0 sont uniquement disponibles dans les systèmes d’exploitation Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f9537-133">The Task Scheduler 1.0 enumerations are available only in Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f9537-134">Ils sont déconseillés à partir de Windows Vista et peuvent être supprimés complètement à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="f9537-134">They are deprecated as of Windows Vista and may be removed completely in the future.</span></span> <span data-ttu-id="f9537-135">Utilisez à la place les énumérations Planificateur de tâches 2,0 listées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="f9537-135">Please use the Task Scheduler 2.0 enumerations listed above instead.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f9537-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9537-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9537-137">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f9537-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f9537-138">Référence Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f9537-138">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




