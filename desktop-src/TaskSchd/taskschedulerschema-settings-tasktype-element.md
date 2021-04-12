---
title: Élément Settings (taskType)
description: Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Paramètres, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384356"
---
# <a name="settings-tasktype-element"></a><span data-ttu-id="0d432-104">Élément Settings (taskType)</span><span class="sxs-lookup"><span data-stu-id="0d432-104">Settings (taskType) Element</span></span>

<span data-ttu-id="0d432-105">Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="0d432-105">Specifies the settings that the Task Scheduler uses to perform the task.</span></span>

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="0d432-106">L’élément **Settings** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0d432-106">The **Settings** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0d432-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="0d432-107">Parent element</span></span>



| <span data-ttu-id="0d432-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0d432-108">Element</span></span>                                          | <span data-ttu-id="0d432-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="0d432-109">Derived from</span></span>                                                 | <span data-ttu-id="0d432-110">Description</span><span class="sxs-lookup"><span data-stu-id="0d432-110">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="0d432-111">**Tâche**</span><span class="sxs-lookup"><span data-stu-id="0d432-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="0d432-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="0d432-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="0d432-113">Spécifie la tâche qui est effectuée par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="0d432-113">Specifies the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="0d432-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0d432-114">Child elements</span></span>



| <span data-ttu-id="0d432-115">Élément</span><span class="sxs-lookup"><span data-stu-id="0d432-115">Element</span></span>                                                                                                          | <span data-ttu-id="0d432-116">Type</span><span class="sxs-lookup"><span data-stu-id="0d432-116">Type</span></span>                                                                                              | <span data-ttu-id="0d432-117">Description</span><span class="sxs-lookup"><span data-stu-id="0d432-117">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d432-118">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="0d432-118">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | <span data-ttu-id="0d432-119">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-119">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-120">Spécifie que la tâche peut être terminée à l’aide de TerminateProcess.</span><span class="sxs-lookup"><span data-stu-id="0d432-120">Specifies that the task may be terminated using TerminateProcess.</span></span><br/>                                         |
| [<span data-ttu-id="0d432-121">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="0d432-121">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | <span data-ttu-id="0d432-122">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-122">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-123">Spécifie que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="0d432-123">Specifies that the task can be started using either the Run command or the Context menu.</span></span><br/>                  |
| [<span data-ttu-id="0d432-124">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="0d432-124">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | <span data-ttu-id="0d432-125">duration</span><span class="sxs-lookup"><span data-stu-id="0d432-125">duration</span></span>                                                                                          | <span data-ttu-id="0d432-126">Spécifie la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.</span><span class="sxs-lookup"><span data-stu-id="0d432-126">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span><br/> |
| [<span data-ttu-id="0d432-127">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="0d432-127">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | <span data-ttu-id="0d432-128">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-128">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-129">Spécifie que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.</span><span class="sxs-lookup"><span data-stu-id="0d432-129">Specifies that the task will not be started if the computer is running on batteries.</span></span><br/>                      |
| [<span data-ttu-id="0d432-130">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="0d432-130">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                              | <span data-ttu-id="0d432-131">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-131">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-132">Spécifie que la tâche est activée.</span><span class="sxs-lookup"><span data-stu-id="0d432-132">Specifies that the task is enabled.</span></span> <span data-ttu-id="0d432-133">La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="0d432-133">The task can be performed only when this setting is True.</span></span><br/>             |
| [<span data-ttu-id="0d432-134">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="0d432-134">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | <span data-ttu-id="0d432-135">duration</span><span class="sxs-lookup"><span data-stu-id="0d432-135">duration</span></span>                                                                                          | <span data-ttu-id="0d432-136">Durée d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0d432-136">Amount of time allowed to complete the task.</span></span><br/>                                                              |
| [<span data-ttu-id="0d432-137">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="0d432-137">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                | <span data-ttu-id="0d432-138">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-138">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-139">Spécifie que la tâche ne sera pas visible dans l’interface utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0d432-139">Specifies that the task will not be visible in the UI by default.</span></span><br/>                                         |
| [<span data-ttu-id="0d432-140">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="0d432-140">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [<span data-ttu-id="0d432-141">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="0d432-141">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="0d432-142">Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="0d432-142">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                    |
| [<span data-ttu-id="0d432-143">**MaintenanceSettings**</span><span class="sxs-lookup"><span data-stu-id="0d432-143">**MaintenanceSettings**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [<span data-ttu-id="0d432-144">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="0d432-144">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md)        | <span data-ttu-id="0d432-145">Spécifie comment l’Planificateur de tâches effectue des tâches pendant la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="0d432-145">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span><br/>                             |
| [<span data-ttu-id="0d432-146">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="0d432-146">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [<span data-ttu-id="0d432-147">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="0d432-147">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="0d432-148">Spécifie la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0d432-148">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span><br/>       |
| [<span data-ttu-id="0d432-149">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="0d432-149">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                            | [<span data-ttu-id="0d432-150">**priorityType**</span><span class="sxs-lookup"><span data-stu-id="0d432-150">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="0d432-151">Spécifie le niveau de priorité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0d432-151">Specifies the priority level for the task.</span></span><br/>                                                                |
| [<span data-ttu-id="0d432-152">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="0d432-152">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [<span data-ttu-id="0d432-153">**restartType**</span><span class="sxs-lookup"><span data-stu-id="0d432-153">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="0d432-154">Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="0d432-154">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/>      |
| [<span data-ttu-id="0d432-155">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="0d432-155">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | <span data-ttu-id="0d432-156">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-156">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-157">Spécifie que la tâche est exécutée uniquement lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="0d432-157">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                |
| [<span data-ttu-id="0d432-158">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="0d432-158">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | <span data-ttu-id="0d432-159">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-159">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-160">Spécifie que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.</span><span class="sxs-lookup"><span data-stu-id="0d432-160">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                     |
| [<span data-ttu-id="0d432-161">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="0d432-161">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | <span data-ttu-id="0d432-162">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-162">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-163">Spécifie que les Planificateur de tâches peuvent démarrer la tâche à tout moment une fois l’heure planifiée passée.</span><span class="sxs-lookup"><span data-stu-id="0d432-163">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>     |
| [<span data-ttu-id="0d432-164">**StopIfGoingOnBatteries (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="0d432-164">**StopIfGoingOnBatteries (settingsType)**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | <span data-ttu-id="0d432-165">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-165">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-166">Spécifie que la tâche sera arrêtée si l’ordinateur va sur des batteries.</span><span class="sxs-lookup"><span data-stu-id="0d432-166">Specifies that the task will be stopped if the computer is going onto batteries.</span></span><br/>                          |
| [<span data-ttu-id="0d432-167">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="0d432-167">**Volatile**</span></span>](taskschedulerschema-volatile-element.md)                                                         | <span data-ttu-id="0d432-168">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-168">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-169">Spécifie si la tâche est automatiquement désactivée par Planificateur de tâches au démarrage de Windows.</span><span class="sxs-lookup"><span data-stu-id="0d432-169">Specifies if the task is automatically disabled by Task Scheduler at Windows startup.</span></span><br/>                     |
| [<span data-ttu-id="0d432-170">**WakeToRun (settingsType)**</span><span class="sxs-lookup"><span data-stu-id="0d432-170">**WakeToRun (settingsType)**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                           | <span data-ttu-id="0d432-171">boolean</span><span class="sxs-lookup"><span data-stu-id="0d432-171">boolean</span></span>                                                                                           | <span data-ttu-id="0d432-172">Spécifie que Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="0d432-172">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span><br/>                     |



## <a name="remarks"></a><span data-ttu-id="0d432-173">Notes</span><span class="sxs-lookup"><span data-stu-id="0d432-173">Remarks</span></span>

<span data-ttu-id="0d432-174">Vous pouvez sélectionner un ou plusieurs des éléments enfants référencés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="0d432-174">You can select one or more of the child elements referenced above.</span></span>

<span data-ttu-id="0d432-175">Pour le développement C++, les informations d’inscription d’une tâche sont spécifiées à l’aide de la [**propriété Settings de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span><span class="sxs-lookup"><span data-stu-id="0d432-175">For C++ development, the registration information of a task is specified using the [**Settings property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).</span></span>

<span data-ttu-id="0d432-176">Pour le développement de scripts, les informations d’inscription d’une tâche sont spécifiées à l’aide de la propriété [**TaskDefinition. Settings**](taskdefinition-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="0d432-176">For scripting development, the registration information of a task is specified using the [**TaskDefinition.Settings**](taskdefinition-settings.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="0d432-177">Exemples</span><span class="sxs-lookup"><span data-stu-id="0d432-177">Examples</span></span>

<span data-ttu-id="0d432-178">L’exemple de code XML suivant définit un élément Settings qui permet un arrêt forcé de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0d432-178">The following XML code example defines a settings element that allows a hard termination of the task.</span></span>


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



<span data-ttu-id="0d432-179">Pour plus d’informations et pour obtenir un exemple complet du code XML permettant de définir des paramètres de tâche, consultez [exemple de déclenchement de temps (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="0d432-179">For more information and a complete example of the XML for setting task settings, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d432-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d432-180">Requirements</span></span>



| <span data-ttu-id="0d432-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d432-181">Requirement</span></span> | <span data-ttu-id="0d432-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d432-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d432-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d432-183">Minimum supported client</span></span><br/> | <span data-ttu-id="0d432-184">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d432-184">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d432-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d432-185">Minimum supported server</span></span><br/> | <span data-ttu-id="0d432-186">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d432-186">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d432-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d432-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d432-188">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0d432-188">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0d432-189">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0d432-189">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





