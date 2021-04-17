---
title: Objet TaskService
description: Pour les scripts, fournit l’accès au service Planificateur de tâches pour la gestion des tâches inscrites.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Objet TaskService Planificateur de tâches
- Planificateur de tâches d’objets TaskService, Description
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466411"
---
# <a name="taskservice-object"></a><span data-ttu-id="04073-105">Objet TaskService</span><span class="sxs-lookup"><span data-stu-id="04073-105">TaskService object</span></span>

<span data-ttu-id="04073-106">Pour les scripts, fournit l’accès au service Planificateur de tâches pour la gestion des tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="04073-106">For scripting, provides access to the Task Scheduler service for managing registered tasks.</span></span>

<span data-ttu-id="04073-107">La méthode [**TaskService. Connect**](taskservice-connect.md) doit être appelée avant d’appeler l’une des autres méthodes **TaskService** .</span><span class="sxs-lookup"><span data-stu-id="04073-107">The [**TaskService.Connect**](taskservice-connect.md) method should be called before calling any of the other **TaskService** methods.</span></span>

## <a name="members"></a><span data-ttu-id="04073-108">Membres</span><span class="sxs-lookup"><span data-stu-id="04073-108">Members</span></span>

<span data-ttu-id="04073-109">L’objet **TaskService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="04073-109">The **TaskService** object has these types of members:</span></span>

-   [<span data-ttu-id="04073-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="04073-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="04073-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04073-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04073-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="04073-112">Methods</span></span>

<span data-ttu-id="04073-113">L’objet **TaskService** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="04073-113">The **TaskService** object has these methods.</span></span>



| <span data-ttu-id="04073-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="04073-114">Method</span></span>                                                 | <span data-ttu-id="04073-115">Description</span><span class="sxs-lookup"><span data-stu-id="04073-115">Description</span></span>                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04073-116">**Connecter**</span><span class="sxs-lookup"><span data-stu-id="04073-116">**Connect**</span></span>](taskservice-connect.md)                 | <span data-ttu-id="04073-117">Établit une connexion à un ordinateur distant et associe tous les appels suivants à cette interface avec une session à distance.</span><span class="sxs-lookup"><span data-stu-id="04073-117">Connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="04073-118">**GetFolder ITaskService**</span><span class="sxs-lookup"><span data-stu-id="04073-118">**GetFolder**</span></span>](taskservice-getfolder.md)             | <span data-ttu-id="04073-119">Obtient le chemin d’accès à un dossier de tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="04073-119">Gets the path to a folder of registered tasks.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="04073-120">**GetRunningTasks**</span><span class="sxs-lookup"><span data-stu-id="04073-120">**GetRunningTasks**</span></span>](taskservice-getrunningtasks.md) | <span data-ttu-id="04073-121">Obtient une collection de tâches en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="04073-121">Gets a collection of running tasks.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="04073-122">**NewTask**</span><span class="sxs-lookup"><span data-stu-id="04073-122">**NewTask**</span></span>](taskservice-newtask.md)                 | <span data-ttu-id="04073-123">Retourne un objet de définition de tâche vide à remplir avec des paramètres et des propriétés, puis inscrit à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="04073-123">Returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="04073-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04073-124">Properties</span></span>

<span data-ttu-id="04073-125">L’objet **TaskService** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="04073-125">The **TaskService** object has these properties.</span></span>



| <span data-ttu-id="04073-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="04073-126">Property</span></span>                                                          | <span data-ttu-id="04073-127">Description</span><span class="sxs-lookup"><span data-stu-id="04073-127">Description</span></span>                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04073-128">**Connecté**</span><span class="sxs-lookup"><span data-stu-id="04073-128">**Connected**</span></span>](taskservice-connected.md)<br/>             | <span data-ttu-id="04073-129">Obtient une valeur booléenne qui indique si vous êtes connecté au service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="04073-129">Gets a Boolean value that indicates if you are connected to the Task Scheduler service.</span></span><br/>                          |
| [<span data-ttu-id="04073-130">**ConnectedDomain**</span><span class="sxs-lookup"><span data-stu-id="04073-130">**ConnectedDomain**</span></span>](taskservice-connecteddomain.md)<br/> | <span data-ttu-id="04073-131">Obtient le nom du domaine auquel l’ordinateur [**TargetServer**](taskservice-targetserver.md) est connecté.</span><span class="sxs-lookup"><span data-stu-id="04073-131">Gets the name of the domain to which the [**TargetServer**](taskservice-targetserver.md) computer is connected.</span></span><br/> |
| [<span data-ttu-id="04073-132">**ConnectedUser**</span><span class="sxs-lookup"><span data-stu-id="04073-132">**ConnectedUser**</span></span>](taskservice-connecteduser.md)<br/>     | <span data-ttu-id="04073-133">Obtient le nom de l’utilisateur connecté au service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="04073-133">Gets the name of the user that is connected to the Task Scheduler service.</span></span><br/>                                       |
| <span data-ttu-id="04073-134">HighestVersion</span><span class="sxs-lookup"><span data-stu-id="04073-134">HighestVersion</span></span><br/>                                         | <span data-ttu-id="04073-135">Obtient la version la plus récente de Planificateur de tâches qu’un ordinateur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="04073-135">Gets the highest version of Task Scheduler that a computer supports.</span></span><br/>                                             |
| [<span data-ttu-id="04073-136">**TargetServer**</span><span class="sxs-lookup"><span data-stu-id="04073-136">**TargetServer**</span></span>](taskservice-targetserver.md)<br/>       | <span data-ttu-id="04073-137">Obtient le nom de l’ordinateur qui exécute le service Planificateur de tâches auquel l’utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="04073-137">Gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span><br/>          |



 

## <a name="examples"></a><span data-ttu-id="04073-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="04073-138">Examples</span></span>

<span data-ttu-id="04073-139">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md), [exemple de déclencheur d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemple de déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (script)](registration-trigger-example--scripting-.md), exemple de déclencheur [hebdomadaire](weekly-trigger-example--scripting-.md)(script), exemple de [déclencheur de connexion (](logon-trigger-example--scripting-.md)script), exemple de [déclencheur de démarrage (script)](boot-trigger-example--scripting-.md)ou [affichage des noms de tâches et des États (script)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="04073-139">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04073-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04073-140">Requirements</span></span>



| <span data-ttu-id="04073-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04073-141">Requirement</span></span> | <span data-ttu-id="04073-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="04073-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04073-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04073-143">Minimum supported client</span></span><br/> | <span data-ttu-id="04073-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04073-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="04073-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04073-145">Minimum supported server</span></span><br/> | <span data-ttu-id="04073-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04073-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04073-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="04073-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="04073-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="04073-148"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="04073-149">DLL</span><span class="sxs-lookup"><span data-stu-id="04073-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04073-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04073-150"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04073-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04073-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04073-152">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="04073-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





