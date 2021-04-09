---
title: Objet RegisteredTask
description: Objet de script qui fournit les méthodes utilisées pour exécuter immédiatement la tâche, récupérez les instances en cours d’exécution de la tâche, récupérez ou définissez les informations d’identification utilisées pour enregistrer la tâche et les propriétés qui décrivent la tâche.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Objet RegisteredTask Planificateur de tâches
- Planificateur de tâches d’objets RegisteredTask, Description
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740469"
---
# <a name="registeredtask-object"></a><span data-ttu-id="cb4e5-105">Objet RegisteredTask</span><span class="sxs-lookup"><span data-stu-id="cb4e5-105">RegisteredTask object</span></span>

<span data-ttu-id="cb4e5-106">Objet de script qui fournit les méthodes utilisées pour exécuter immédiatement la tâche, récupérez les instances en cours d’exécution de la tâche, récupérez ou définissez les informations d’identification utilisées pour enregistrer la tâche et les propriétés qui décrivent la tâche.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-106">Scripting object that provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.</span></span>

## <a name="members"></a><span data-ttu-id="cb4e5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cb4e5-107">Members</span></span>

<span data-ttu-id="cb4e5-108">L’objet **RegisteredTask** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb4e5-108">The **RegisteredTask** object has these types of members:</span></span>

-   [<span data-ttu-id="cb4e5-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb4e5-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb4e5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb4e5-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb4e5-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb4e5-111">Methods</span></span>

<span data-ttu-id="cb4e5-112">L’objet **RegisteredTask** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-112">The **RegisteredTask** object has these methods.</span></span>



| <span data-ttu-id="cb4e5-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb4e5-113">Method</span></span>                                                                | <span data-ttu-id="cb4e5-114">Description</span><span class="sxs-lookup"><span data-stu-id="cb4e5-114">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb4e5-115">**GetInstances**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-115">**GetInstances**</span></span>](registeredtask-getinstances.md)                   | <span data-ttu-id="cb4e5-116">Retourne toutes les instances de la tâche inscrite en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-116">Returns all instances of the registered task that are currently running.</span></span><br/>             |
| [<span data-ttu-id="cb4e5-117">**GetRunTimes**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-117">**GetRunTimes**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | <span data-ttu-id="cb4e5-118">Obtient le nombre de fois que la tâche inscrite est planifiée pour s’exécuter pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-118">Gets the times that the registered task is scheduled to run during a specified time.</span></span><br/> |
| [<span data-ttu-id="cb4e5-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-119">**GetSecurityDescriptor**</span></span>](registeredtask-getsecuritydescriptor.md) | <span data-ttu-id="cb4e5-120">Obtient le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-120">Gets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="cb4e5-121">**Utilisez**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-121">**Run**</span></span>](registeredtask-run.md)                                     | <span data-ttu-id="cb4e5-122">Exécute la tâche inscrite immédiatement.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-122">Runs the registered task immediately.</span></span><br/>                                                |
| [<span data-ttu-id="cb4e5-123">**RunEx**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-123">**RunEx**</span></span>](registeredtask-runex.md)                                 | <span data-ttu-id="cb4e5-124">Exécute la tâche inscrite immédiatement à l’aide des indicateurs spécifiés et d’un identificateur de session.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-124">Runs the registered task immediately using specified flags and a session identifier.</span></span><br/> |
| [<span data-ttu-id="cb4e5-125">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-125">**SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md) | <span data-ttu-id="cb4e5-126">Définit le descripteur de sécurité utilisé comme informations d’identification pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-126">Sets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="cb4e5-127">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-127">**Stop**</span></span>](registeredtask-stop.md)                                   | <span data-ttu-id="cb4e5-128">Arrête immédiatement la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-128">Stops the registered task immediately.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="cb4e5-129">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb4e5-129">Properties</span></span>

<span data-ttu-id="cb4e5-130">L’objet **RegisteredTask** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-130">The **RegisteredTask** object has these properties.</span></span>



| <span data-ttu-id="cb4e5-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="cb4e5-131">Property</span></span>                                                                   | <span data-ttu-id="cb4e5-132">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="cb4e5-132">Access type</span></span>           | <span data-ttu-id="cb4e5-133">Description</span><span class="sxs-lookup"><span data-stu-id="cb4e5-133">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb4e5-134">**Définition**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-134">**Definition**</span></span>](registeredtask-definition.md)<br/>                 | <span data-ttu-id="cb4e5-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-135">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-136">Obtient la définition de la tâche.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-136">Gets the definition of the task.</span></span><br/>                                               |
| [<span data-ttu-id="cb4e5-137">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-137">**Enabled**</span></span>](registeredtask-enabled.md)<br/>                       | <span data-ttu-id="cb4e5-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cb4e5-138">Read/write</span></span><br/> | <span data-ttu-id="cb4e5-139">Obtient ou définit une valeur booléenne qui indique si la tâche inscrite est activée.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-139">Gets or set a Boolean value that indicates if the registered task is enabled.</span></span><br/>  |
| [<span data-ttu-id="cb4e5-140">**LastRunTime**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-140">**LastRunTime**</span></span>](registeredtask-lastruntime.md)<br/>               | <span data-ttu-id="cb4e5-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-141">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-142">Obtient l’heure de la dernière exécution de la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-142">Gets the time the registered task was last run.</span></span><br/>                                |
| [<span data-ttu-id="cb4e5-143">**LastTaskResult**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-143">**LastTaskResult**</span></span>](registeredtask-lasttaskresult.md)<br/>         | <span data-ttu-id="cb4e5-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-144">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-145">Obtient les résultats qui ont été retournés lors de la dernière exécution de la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-145">Gets the results that were returned the last time the registered task was run.</span></span><br/> |
| [<span data-ttu-id="cb4e5-146">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-146">**Name**</span></span>](registeredtask-name.md)<br/>                             | <span data-ttu-id="cb4e5-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-147">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-148">Obtient le nom de la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-148">Gets the name of the registered task.</span></span><br/>                                          |
| [<span data-ttu-id="cb4e5-149">**NextRunTime**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-149">**NextRunTime**</span></span>](registeredtask-nextruntime.md)<br/>               | <span data-ttu-id="cb4e5-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-150">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-151">Obtient l’heure à laquelle la tâche inscrite est planifiée pour s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-151">Gets the time when the registered task is next scheduled to run.</span></span><br/>               |
| [<span data-ttu-id="cb4e5-152">**NumberOfMissedRuns**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-152">**NumberOfMissedRuns**</span></span>](registeredtask-numberofmissedruns.md)<br/> | <span data-ttu-id="cb4e5-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-153">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-154">Obtient le nombre de fois où la tâche inscrite a manqué une exécution planifiée.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-154">Gets the number of times the registered task has missed a scheduled run.</span></span><br/>       |
| [<span data-ttu-id="cb4e5-155">**D**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-155">**Path**</span></span>](registeredtask-path.md)<br/>                             | <span data-ttu-id="cb4e5-156">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-156">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-157">Obtient le chemin d’accès à l’emplacement où la tâche inscrite est stockée.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-157">Gets the path to where the registered task is stored.</span></span><br/>                          |
| [<span data-ttu-id="cb4e5-158">**State**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-158">**State**</span></span>](registeredtask-state.md)<br/>                           | <span data-ttu-id="cb4e5-159">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-159">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-160">Obtient l’état opérationnel de la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-160">Gets the operational state of the registered task.</span></span><br/>                             |
| [<span data-ttu-id="cb4e5-161">**LANGAGE**</span><span class="sxs-lookup"><span data-stu-id="cb4e5-161">**XML**</span></span>](registeredtask-xml.md)<br/>                               | <span data-ttu-id="cb4e5-162">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb4e5-162">Read-only</span></span><br/>  | <span data-ttu-id="cb4e5-163">Obtient les informations d’inscription au format XML pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="cb4e5-163">Gets the XML-formatted registration information for the registered task.</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="cb4e5-164">Exemples</span><span class="sxs-lookup"><span data-stu-id="cb4e5-164">Examples</span></span>

<span data-ttu-id="cb4e5-165">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md) et [affichage des noms et des États des tâches (script)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="cb4e5-165">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) and [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4e5-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb4e5-166">Requirements</span></span>



| <span data-ttu-id="cb4e5-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb4e5-167">Requirement</span></span> | <span data-ttu-id="cb4e5-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb4e5-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4e5-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb4e5-169">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4e5-170">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb4e5-170">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cb4e5-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb4e5-171">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4e5-172">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb4e5-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb4e5-173">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cb4e5-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb4e5-174"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cb4e5-174"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cb4e5-175">DLL</span><span class="sxs-lookup"><span data-stu-id="cb4e5-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb4e5-176"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb4e5-176"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





