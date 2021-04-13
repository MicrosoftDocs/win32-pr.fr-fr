---
title: RegisteredTask. State, propriété
description: Pour les scripts, obtient l’état opérationnel de la tâche inscrite.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Planificateur de tâches de propriété d’État
- Propriété State Planificateur de tâches, objet RegisteredTask
- Objet RegisteredTask Planificateur de tâches, propriété State
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466770"
---
# <a name="registeredtaskstate-property"></a><span data-ttu-id="6aafd-106">RegisteredTask. State, propriété</span><span class="sxs-lookup"><span data-stu-id="6aafd-106">RegisteredTask.State property</span></span>

<span data-ttu-id="6aafd-107">Pour les scripts, obtient l’état opérationnel de la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="6aafd-107">For scripting, gets the operational state of the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aafd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aafd-108">Syntax</span></span>


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a><span data-ttu-id="6aafd-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6aafd-109">Property value</span></span>

<span data-ttu-id="6aafd-110">Constante [**d' \_ État de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_state) qui définit l’état opérationnel de la tâche.</span><span class="sxs-lookup"><span data-stu-id="6aafd-110">A [**TASK\_STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) constant that defines the operational state of the task.</span></span>



| <span data-ttu-id="6aafd-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="6aafd-111">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="6aafd-112">Signification</span><span class="sxs-lookup"><span data-stu-id="6aafd-112">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="6aafd-113"><dt>**Tâche \_ ÉTAT \_ inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6aafd-113"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="6aafd-114">L’état de la tâche est inconnu.</span><span class="sxs-lookup"><span data-stu-id="6aafd-114">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="6aafd-115"><dt>**Tâche \_ ÉTAT \_ désactivé**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6aafd-115"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="6aafd-116">La tâche est inscrite, mais elle est désactivée et aucune instance de la tâche n’est mise en file d’attente ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6aafd-116">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="6aafd-117">La tâche ne peut pas être exécutée tant qu’elle n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="6aafd-117">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="6aafd-118"><dt>**Tâche \_ État en \_ file d’attente**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6aafd-118"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="6aafd-119">Les instances de la tâche sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="6aafd-119">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="6aafd-120"><dt>**Tâche \_ ÉTAT \_ prêt**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6aafd-120"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="6aafd-121">La tâche est prête à être exécutée, mais aucune instance n’est en file d’attente ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6aafd-121">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="6aafd-122"><dt>**Tâche \_ ÉTAT \_ en cours d’exécution**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6aafd-122"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="6aafd-123">Une ou plusieurs instances de la tâche sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6aafd-123">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="6aafd-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6aafd-124">Requirements</span></span>



| <span data-ttu-id="6aafd-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6aafd-125">Requirement</span></span> | <span data-ttu-id="6aafd-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6aafd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6aafd-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aafd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6aafd-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6aafd-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6aafd-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aafd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6aafd-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6aafd-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6aafd-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6aafd-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="6aafd-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6aafd-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6aafd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6aafd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aafd-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aafd-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6aafd-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aafd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aafd-136">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="6aafd-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="6aafd-137">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="6aafd-137">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





