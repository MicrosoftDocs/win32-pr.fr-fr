---
title: Objet TaskFolder
description: Objet de script qui fournit les méthodes utilisées pour inscrire (créer) des tâches dans le dossier, supprimer des tâches du dossier et créer ou supprimer des sous-dossiers du dossier.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Objet TaskFolder Planificateur de tâches
- Planificateur de tâches d’objets TaskFolder, Description
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509122"
---
# <a name="taskfolder-object"></a><span data-ttu-id="744ec-105">Objet TaskFolder</span><span class="sxs-lookup"><span data-stu-id="744ec-105">TaskFolder object</span></span>

<span data-ttu-id="744ec-106">Objet de script qui fournit les méthodes utilisées pour inscrire (créer) des tâches dans le dossier, supprimer des tâches du dossier et créer ou supprimer des sous-dossiers du dossier.</span><span class="sxs-lookup"><span data-stu-id="744ec-106">Scripting object that provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.</span></span>

## <a name="members"></a><span data-ttu-id="744ec-107">Membres</span><span class="sxs-lookup"><span data-stu-id="744ec-107">Members</span></span>

<span data-ttu-id="744ec-108">L’objet **TaskFolder** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="744ec-108">The **TaskFolder** object has these types of members:</span></span>

-   [<span data-ttu-id="744ec-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="744ec-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="744ec-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="744ec-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="744ec-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="744ec-111">Methods</span></span>

<span data-ttu-id="744ec-112">L’objet **TaskFolder** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="744ec-112">The **TaskFolder** object has these methods.</span></span>



| <span data-ttu-id="744ec-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="744ec-113">Method</span></span>                                                              | <span data-ttu-id="744ec-114">Description</span><span class="sxs-lookup"><span data-stu-id="744ec-114">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="744ec-115">**CreateFolder**</span><span class="sxs-lookup"><span data-stu-id="744ec-115">**CreateFolder**</span></span>](taskfolder-createfolder.md)                     | <span data-ttu-id="744ec-116">Crée un dossier pour les tâches associées.</span><span class="sxs-lookup"><span data-stu-id="744ec-116">Creates a folder for related tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="744ec-117">**DeleteFolder**</span><span class="sxs-lookup"><span data-stu-id="744ec-117">**DeleteFolder**</span></span>](taskfolder-deletefolder.md)                     | <span data-ttu-id="744ec-118">Supprime un sous-dossier du dossier parent.</span><span class="sxs-lookup"><span data-stu-id="744ec-118">Deletes a subfolder from the parent folder.</span></span><br/>                                                                                         |
| [<span data-ttu-id="744ec-119">**DeleteTask**</span><span class="sxs-lookup"><span data-stu-id="744ec-119">**DeleteTask**</span></span>](taskfolder-deletetask.md)                         | <span data-ttu-id="744ec-120">Supprime une tâche du dossier.</span><span class="sxs-lookup"><span data-stu-id="744ec-120">Deletes a task from the folder.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="744ec-121">**GetFolder ITaskService**</span><span class="sxs-lookup"><span data-stu-id="744ec-121">**GetFolder**</span></span>](taskfolder-getfolder.md)                           | <span data-ttu-id="744ec-122">Obtient un dossier qui contient des tâches à un emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="744ec-122">Gets a folder that contains tasks at a specified location.</span></span><br/>                                                                          |
| [<span data-ttu-id="744ec-123">**GetFolders**</span><span class="sxs-lookup"><span data-stu-id="744ec-123">**GetFolders**</span></span>](taskfolder-getfolders.md)                         | <span data-ttu-id="744ec-124">Obtient tous les sous-dossiers du dossier.</span><span class="sxs-lookup"><span data-stu-id="744ec-124">Gets all the subfolders in the folder.</span></span><br/>                                                                                              |
| [<span data-ttu-id="744ec-125">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="744ec-125">**GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)   | <span data-ttu-id="744ec-126">Obtient le descripteur de sécurité pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="744ec-126">Gets the security descriptor for the folder.</span></span><br/>                                                                                        |
| [<span data-ttu-id="744ec-127">**GetTask**</span><span class="sxs-lookup"><span data-stu-id="744ec-127">**GetTask**</span></span>](taskfolder-gettask.md)                               | <span data-ttu-id="744ec-128">Obtient une tâche à un emplacement spécifié dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="744ec-128">Gets a task at a specified location in a folder.</span></span><br/>                                                                                    |
| [<span data-ttu-id="744ec-129">**GetTasks**</span><span class="sxs-lookup"><span data-stu-id="744ec-129">**GetTasks**</span></span>](taskfolder-gettasks.md)                             | <span data-ttu-id="744ec-130">Obtient toutes les tâches dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="744ec-130">Gets all the tasks in the folder.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="744ec-131">**RegisterTask**</span><span class="sxs-lookup"><span data-stu-id="744ec-131">**RegisterTask**</span></span>](taskfolder-registertask.md)                     | <span data-ttu-id="744ec-132">Inscrit (crée) une nouvelle tâche dans le dossier à l’aide de XML pour définir la tâche.</span><span class="sxs-lookup"><span data-stu-id="744ec-132">Registers (creates) a new task in the folder using XML to define the task.</span></span><br/>                                                          |
| [<span data-ttu-id="744ec-133">**RegisterTaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="744ec-133">**RegisterTaskDefinition**</span></span>](taskfolder-registertaskdefinition.md) | <span data-ttu-id="744ec-134">Inscrit (crée) une tâche à un emplacement spécifié à l’aide de l’interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) pour définir une tâche.</span><span class="sxs-lookup"><span data-stu-id="744ec-134">Registers (creates) a task in a specified location using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define a task.</span></span><br/> |
| [<span data-ttu-id="744ec-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="744ec-135">**SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)   | <span data-ttu-id="744ec-136">Définit le descripteur de sécurité pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="744ec-136">Sets the security descriptor for the folder.</span></span><br/>                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="744ec-137">Propriétés</span><span class="sxs-lookup"><span data-stu-id="744ec-137">Properties</span></span>

<span data-ttu-id="744ec-138">L’objet **TaskFolder** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="744ec-138">The **TaskFolder** object has these properties.</span></span>



| <span data-ttu-id="744ec-139">Propriété</span><span class="sxs-lookup"><span data-stu-id="744ec-139">Property</span></span>                                   | <span data-ttu-id="744ec-140">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="744ec-140">Access type</span></span>          | <span data-ttu-id="744ec-141">Description</span><span class="sxs-lookup"><span data-stu-id="744ec-141">Description</span></span>                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="744ec-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="744ec-142">**Name**</span></span>](taskfolder-name.md)<br/> | <span data-ttu-id="744ec-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="744ec-143">Read-only</span></span><br/> | <span data-ttu-id="744ec-144">Obtient le nom utilisé pour identifier le dossier qui contient une tâche.</span><span class="sxs-lookup"><span data-stu-id="744ec-144">Gets the name that is used to identify the folder that contains a task.</span></span><br/> |
| [<span data-ttu-id="744ec-145">**D**</span><span class="sxs-lookup"><span data-stu-id="744ec-145">**Path**</span></span>](taskfolder-path.md)<br/> | <span data-ttu-id="744ec-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="744ec-146">Read-only</span></span><br/> | <span data-ttu-id="744ec-147">Obtient le chemin d’accès à l’emplacement où le dossier est stocké.</span><span class="sxs-lookup"><span data-stu-id="744ec-147">Gets the path to where the folder is stored.</span></span><br/>                            |



 

## <a name="examples"></a><span data-ttu-id="744ec-148">Exemples</span><span class="sxs-lookup"><span data-stu-id="744ec-148">Examples</span></span>

<span data-ttu-id="744ec-149">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md), [exemple de déclencheur d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemple de déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (script)](registration-trigger-example--scripting-.md), exemple de déclencheur [hebdomadaire](weekly-trigger-example--scripting-.md)(script), exemple de [déclencheur de connexion (](logon-trigger-example--scripting-.md)script), exemple de [déclencheur de démarrage (script)](boot-trigger-example--scripting-.md)ou [affichage des noms de tâches et des États (script)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="744ec-149">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="744ec-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="744ec-150">Requirements</span></span>



| <span data-ttu-id="744ec-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="744ec-151">Requirement</span></span> | <span data-ttu-id="744ec-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="744ec-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="744ec-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="744ec-153">Minimum supported client</span></span><br/> | <span data-ttu-id="744ec-154">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="744ec-154">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="744ec-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="744ec-155">Minimum supported server</span></span><br/> | <span data-ttu-id="744ec-156">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="744ec-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="744ec-157">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="744ec-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="744ec-158"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="744ec-158"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="744ec-159">DLL</span><span class="sxs-lookup"><span data-stu-id="744ec-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="744ec-160"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="744ec-160"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="744ec-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="744ec-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744ec-162">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="744ec-162">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="744ec-163">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="744ec-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





