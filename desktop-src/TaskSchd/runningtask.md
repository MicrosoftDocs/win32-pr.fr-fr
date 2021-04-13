---
title: Objet RunningTask
description: Objet de script qui fournit les méthodes permettant d’obtenir des informations et de contrôler une tâche en cours d’exécution.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Objet RunningTask Planificateur de tâches
- Planificateur de tâches d’objets RunningTask, Description
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508862"
---
# <a name="runningtask-object"></a><span data-ttu-id="5d393-105">Objet RunningTask</span><span class="sxs-lookup"><span data-stu-id="5d393-105">RunningTask object</span></span>

<span data-ttu-id="5d393-106">Objet de script qui fournit les méthodes permettant d’obtenir des informations et de contrôler une tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5d393-106">Scripting object that provides the methods to get information from and control a running task.</span></span>

## <a name="members"></a><span data-ttu-id="5d393-107">Membres</span><span class="sxs-lookup"><span data-stu-id="5d393-107">Members</span></span>

<span data-ttu-id="5d393-108">L’objet **RunningTask** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5d393-108">The **RunningTask** object has these types of members:</span></span>

-   [<span data-ttu-id="5d393-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5d393-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5d393-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5d393-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5d393-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5d393-111">Methods</span></span>

<span data-ttu-id="5d393-112">L’objet **RunningTask** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5d393-112">The **RunningTask** object has these methods.</span></span>



| <span data-ttu-id="5d393-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="5d393-113">Method</span></span>                                 | <span data-ttu-id="5d393-114">Description</span><span class="sxs-lookup"><span data-stu-id="5d393-114">Description</span></span>                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="5d393-115">**Actualiser**</span><span class="sxs-lookup"><span data-stu-id="5d393-115">**Refresh**</span></span>](runningtask-refresh.md) | <span data-ttu-id="5d393-116">Actualise toutes les variables d’instance locales de la tâche.</span><span class="sxs-lookup"><span data-stu-id="5d393-116">Refreshes all of the local instance variables of the task.</span></span><br/> |
| [<span data-ttu-id="5d393-117">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="5d393-117">**Stop**</span></span>](runningtask-stop.md)       | <span data-ttu-id="5d393-118">Arrête cette instance de la tâche.</span><span class="sxs-lookup"><span data-stu-id="5d393-118">Stops this instance of the task.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="5d393-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5d393-119">Properties</span></span>

<span data-ttu-id="5d393-120">L’objet **RunningTask** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5d393-120">The **RunningTask** object has these properties.</span></span>



| <span data-ttu-id="5d393-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="5d393-121">Property</span></span>                                                      | <span data-ttu-id="5d393-122">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="5d393-122">Access type</span></span>          | <span data-ttu-id="5d393-123">Description</span><span class="sxs-lookup"><span data-stu-id="5d393-123">Description</span></span>                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d393-124">**CurrentAction**</span><span class="sxs-lookup"><span data-stu-id="5d393-124">**CurrentAction**</span></span>](runningtask-currentaction.md)<br/> | <span data-ttu-id="5d393-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d393-125">Read-only</span></span><br/> | <span data-ttu-id="5d393-126">Obtient le nom de l’action en cours exécutée par la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5d393-126">Gets the name of the current action that the running task is performing.</span></span><br/> |
| [<span data-ttu-id="5d393-127">**EnginePID**</span><span class="sxs-lookup"><span data-stu-id="5d393-127">**EnginePID**</span></span>](runningtask-enginepid.md)<br/>         | <span data-ttu-id="5d393-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d393-128">Read-only</span></span><br/> | <span data-ttu-id="5d393-129">Obtient l’ID de processus pour le moteur (processus) qui exécute la tâche.</span><span class="sxs-lookup"><span data-stu-id="5d393-129">Gets the process ID for the engine (process) which is running the task.</span></span><br/>  |
| [<span data-ttu-id="5d393-130">**InstanceGuid**</span><span class="sxs-lookup"><span data-stu-id="5d393-130">**InstanceGuid**</span></span>](runningtask-instanceguid.md)<br/>   | <span data-ttu-id="5d393-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d393-131">Read-only</span></span><br/> | <span data-ttu-id="5d393-132">Obtient l’identificateur GUID de cette instance de la tâche.</span><span class="sxs-lookup"><span data-stu-id="5d393-132">Gets the GUID identifier for this instance of the task.</span></span><br/>                  |
| [<span data-ttu-id="5d393-133">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5d393-133">**Name**</span></span>](runningtask-name.md)<br/>                   | <span data-ttu-id="5d393-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d393-134">Read-only</span></span><br/> | <span data-ttu-id="5d393-135">Obtient le nom de la tâche.</span><span class="sxs-lookup"><span data-stu-id="5d393-135">Gets the name of the task.</span></span><br/>                                               |
| [<span data-ttu-id="5d393-136">**D**</span><span class="sxs-lookup"><span data-stu-id="5d393-136">**Path**</span></span>](runningtask-path.md)<br/>                   | <span data-ttu-id="5d393-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d393-137">Read-only</span></span><br/> | <span data-ttu-id="5d393-138">Obtient le chemin d’accès à l’emplacement où la tâche est stockée.</span><span class="sxs-lookup"><span data-stu-id="5d393-138">Gets the path to where the task is stored.</span></span><br/>                               |
| [<span data-ttu-id="5d393-139">**State**</span><span class="sxs-lookup"><span data-stu-id="5d393-139">**State**</span></span>](runningtask-state.md)<br/>                 | <span data-ttu-id="5d393-140">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5d393-140">Read-only</span></span><br/> | <span data-ttu-id="5d393-141">Obtient l’état de la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5d393-141">Gets the state of the running task.</span></span> <br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="5d393-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d393-142">Requirements</span></span>



| <span data-ttu-id="5d393-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d393-143">Requirement</span></span> | <span data-ttu-id="5d393-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d393-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d393-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d393-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5d393-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d393-146">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5d393-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d393-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5d393-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d393-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d393-149">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5d393-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="5d393-150"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5d393-150"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5d393-151">DLL</span><span class="sxs-lookup"><span data-stu-id="5d393-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d393-152"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d393-152"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d393-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d393-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d393-154">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5d393-154">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="5d393-155">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5d393-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="5d393-156">**RunningTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="5d393-156">**RunningTaskCollection**</span></span>](runningtaskcollection.md)
</dt> <dt>

[<span data-ttu-id="5d393-157">**RegisteredTask. Run**</span><span class="sxs-lookup"><span data-stu-id="5d393-157">**RegisteredTask.Run**</span></span>](registeredtask-run.md)
</dt> <dt>

[<span data-ttu-id="5d393-158">**RegisteredTask.RunEx**</span><span class="sxs-lookup"><span data-stu-id="5d393-158">**RegisteredTask.RunEx**</span></span>](registeredtask-runex.md)
</dt> </dl>

 

 





