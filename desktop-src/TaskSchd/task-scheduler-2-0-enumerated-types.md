---
title: Types énumérés de Planificateur de tâches 2,0
description: Décrit les types énumérés qui définissent les constantes utilisées par les API Planificateur de tâches 2,0.
ms.assetid: d59f017e-df32-4826-954d-9ba338282d0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db410564ab97f0477ecac8aeda2b54b8fd655d62
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316853"
---
# <a name="task-scheduler-20-enumerated-types"></a><span data-ttu-id="d2937-103">Types énumérés de Planificateur de tâches 2,0</span><span class="sxs-lookup"><span data-stu-id="d2937-103">Task Scheduler 2.0 Enumerated Types</span></span>

<span data-ttu-id="d2937-104">Décrit les types énumérés qui définissent les constantes utilisées par les API Planificateur de tâches 2,0.</span><span class="sxs-lookup"><span data-stu-id="d2937-104">Describes the enumerated types that define the constants that are used by the Task Scheduler 2.0 APIs.</span></span>


<span data-ttu-id="d2937-105">Les types énumérés suivants sont introduits dans Planificateur de tâches 2,0.</span><span class="sxs-lookup"><span data-stu-id="d2937-105">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="d2937-106">Énumération</span><span class="sxs-lookup"><span data-stu-id="d2937-106">Enumeration</span></span>                                                                  | <span data-ttu-id="d2937-107">Description</span><span class="sxs-lookup"><span data-stu-id="d2937-107">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2937-108">**\_type d’action de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-108">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="d2937-109">Définit le type d’actions qu’une tâche peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="d2937-109">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="d2937-110">**compatibilité des tâches \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-110">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="d2937-111">Définit les versions de Planificateur de tâches ou la commande AT à laquelle la tâche est compatible.</span><span class="sxs-lookup"><span data-stu-id="d2937-111">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="d2937-112">**création de tâches \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-112">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="d2937-113">Définit le mode de création, de mise à jour ou de désactivation de la tâche par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="d2937-113">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="d2937-114">**\_indicateurs d’énumération de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-114">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="d2937-115">Définit le mode d’énumération du Planificateur de tâches par le biais des tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="d2937-115">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="d2937-116">**\_stratégie d’instances de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-116">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="d2937-117">Définit comment le Planificateur de tâches gère les instances existantes de la tâche lorsqu’il démarre une nouvelle instance de la tâche.</span><span class="sxs-lookup"><span data-stu-id="d2937-117">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="d2937-118">**TYPE de connexion à la tâche \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-118">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="d2937-119">Définit la technique d’ouverture de session requise pour exécuter une tâche.</span><span class="sxs-lookup"><span data-stu-id="d2937-119">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="d2937-120">**\_type de PROCESSTOKENSID de la tâche \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-120">**TASK\_PROCESSTOKENSID\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)             | <span data-ttu-id="d2937-121">Définit les types de SID de processus qui peuvent être utilisés par les tâches.</span><span class="sxs-lookup"><span data-stu-id="d2937-121">Defines the types of process SID that can be used by tasks.</span></span>                                                      |
| [<span data-ttu-id="d2937-122">**\_indicateurs d’exécution de tâches \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-122">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="d2937-123">Définit le mode d’exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="d2937-123">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="d2937-124">**\_type de RUNLEVEL de la tâche \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-124">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="d2937-125">Définit les indicateurs d’élévation LUA qui spécifient avec quel niveau de privilège la tâche sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="d2937-125">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="d2937-126">**\_type de \_ changement d’état de session de tâche \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-126">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="d2937-127">Définit les genres de Terminal Server modification de l’état de session que vous pouvez utiliser pour déclencher l’exécution d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="d2937-127">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="d2937-128">**État de la tâche \_**</span><span class="sxs-lookup"><span data-stu-id="d2937-128">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="d2937-129">Définit les différents États dans lesquels une tâche inscrite peut se trouver.</span><span class="sxs-lookup"><span data-stu-id="d2937-129">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="d2937-130">**\_Déclencheur de tâche \_ type2**</span><span class="sxs-lookup"><span data-stu-id="d2937-130">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="d2937-131">Définit le type de déclencheur qui peut être utilisé par les tâches.</span><span class="sxs-lookup"><span data-stu-id="d2937-131">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="d2937-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2937-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2937-133">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d2937-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d2937-134">Référence Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d2937-134">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




