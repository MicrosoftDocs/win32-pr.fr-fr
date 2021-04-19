---
title: Type complexe settingsType
description: Définit les éléments enfants et les informations de séquencement pour l’élément Settings (taskType).
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- Planificateur de tâches de type complexe settingsType
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3c2b3128a35ee0e46c56d19badd431400d4d862
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509116"
---
# <a name="settingstype-complex-type"></a><span data-ttu-id="7353a-104">Type complexe settingsType</span><span class="sxs-lookup"><span data-stu-id="7353a-104">settingsType Complex Type</span></span>

<span data-ttu-id="7353a-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**Settings (TaskType)**](taskschedulerschema-settings-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7353a-105">Defines the child elements and sequencing information for the [**Settings (taskType)**](taskschedulerschema-settings-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7353a-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7353a-106">Child elements</span></span>



| <span data-ttu-id="7353a-107">Élément</span><span class="sxs-lookup"><span data-stu-id="7353a-107">Element</span></span>                                                                                                             | <span data-ttu-id="7353a-108">Type</span><span class="sxs-lookup"><span data-stu-id="7353a-108">Type</span></span>                                                                                              | <span data-ttu-id="7353a-109">Description</span><span class="sxs-lookup"><span data-stu-id="7353a-109">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7353a-110">**AllowHardTerminate**</span><span class="sxs-lookup"><span data-stu-id="7353a-110">**AllowHardTerminate**</span></span>](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | <span data-ttu-id="7353a-111">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-111">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-112">Spécifie si le service de Planificateur de tâches permet l’arrêt forcé de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7353a-112">Specifies if the Task Scheduler service allows hard termination of the task.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="7353a-113">**AllowStartOnDemand**</span><span class="sxs-lookup"><span data-stu-id="7353a-113">**AllowStartOnDemand**</span></span>](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | <span data-ttu-id="7353a-114">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-114">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-115">Spécifie que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7353a-115">Specifies that the task can be started by using either the Run command or the Context menu.</span></span> <br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="7353a-116">**DeleteExpiredTaskAfter**</span><span class="sxs-lookup"><span data-stu-id="7353a-116">**DeleteExpiredTaskAfter**</span></span>](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | <span data-ttu-id="7353a-117">duration</span><span class="sxs-lookup"><span data-stu-id="7353a-117">duration</span></span>                                                                                          | <span data-ttu-id="7353a-118">Spécifie la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.</span><span class="sxs-lookup"><span data-stu-id="7353a-118">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="7353a-119">Si aucune valeur n’est spécifiée pour cet élément, le service Planificateur de tâches ne supprimera pas la tâche.</span><span class="sxs-lookup"><span data-stu-id="7353a-119">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span><br/>                                                                                           |
| [<span data-ttu-id="7353a-120">**DisallowStartIfOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="7353a-120">**DisallowStartIfOnBatteries**</span></span>](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | <span data-ttu-id="7353a-121">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-121">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-122">Spécifie que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.</span><span class="sxs-lookup"><span data-stu-id="7353a-122">Specifies that the task will not be started if the computer is running on battery power.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="7353a-123">**DisallowStartOnRemoteAppSession**</span><span class="sxs-lookup"><span data-stu-id="7353a-123">**DisallowStartOnRemoteAppSession**</span></span>](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | <span data-ttu-id="7353a-124">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-124">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-125">Spécifie que la tâche ne doit pas démarrer si la tâche est déclenchée pour s’exécuter dans une session à distance intégrée à des applications locales (RAIL).</span><span class="sxs-lookup"><span data-stu-id="7353a-125">Specifies that the task should not start if the task is triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="7353a-126">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="7353a-126">**Enabled**</span></span>](taskschedulerschema-enabled-settingstype-element.md)                                                 | <span data-ttu-id="7353a-127">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-127">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-128">Spécifie que la tâche est activée.</span><span class="sxs-lookup"><span data-stu-id="7353a-128">Specifies that the task is enabled.</span></span> <span data-ttu-id="7353a-129">La tâche ne peut être exécutée que lorsque ce paramètre a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="7353a-129">The task can be performed only when this setting is **True**.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="7353a-130">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="7353a-130">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | <span data-ttu-id="7353a-131">duration</span><span class="sxs-lookup"><span data-stu-id="7353a-131">duration</span></span>                                                                                          | <span data-ttu-id="7353a-132">Spécifie la durée d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7353a-132">Specifies the amount of time allowed to complete the task.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="7353a-133">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="7353a-133">**Hidden**</span></span>](taskschedulerschema-hidden-settingstype-element.md)                                                   | <span data-ttu-id="7353a-134">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-134">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-135">Spécifie, par défaut, que la tâche ne sera pas visible dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7353a-135">Specifies, by default, that the task will not be visible in the user interface (UI).</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="7353a-136">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="7353a-136">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [<span data-ttu-id="7353a-137">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="7353a-137">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md)                      | <span data-ttu-id="7353a-138">Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="7353a-138">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="7353a-139">**MultipleInstancesPolicy**</span><span class="sxs-lookup"><span data-stu-id="7353a-139">**MultipleInstancesPolicy**</span></span>](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [<span data-ttu-id="7353a-140">**multipleInstancesPolicyType**</span><span class="sxs-lookup"><span data-stu-id="7353a-140">**multipleInstancesPolicyType**</span></span>](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | <span data-ttu-id="7353a-141">Spécifie la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7353a-141">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span> <br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="7353a-142">**NetworkProfileName**</span><span class="sxs-lookup"><span data-stu-id="7353a-142">**NetworkProfileName**</span></span>](taskschedulerschema-networkprofilename-settingstype-element.md)                           | <span data-ttu-id="7353a-143">string</span><span class="sxs-lookup"><span data-stu-id="7353a-143">string</span></span>                                                                                            | <span data-ttu-id="7353a-144">Spécifie le nom d’un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="7353a-144">Specifies the name of a network profile.</span></span> <span data-ttu-id="7353a-145">Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="7353a-145">The Task Scheduler service verifies the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span> <span data-ttu-id="7353a-146">Le nom est utilisé à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7353a-146">The name is used for display purposes.</span></span><br/>        |
| [<span data-ttu-id="7353a-147">**NetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="7353a-147">**NetworkSettings**</span></span>](taskschedulerschema-networksettings-settingstype-element.md)                                 | [<span data-ttu-id="7353a-148">**networkSettingsType**</span><span class="sxs-lookup"><span data-stu-id="7353a-148">**networkSettingsType**</span></span>](taskschedulerschema-networksettingstype-complextype.md)                | <span data-ttu-id="7353a-149">Spécifie les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.</span><span class="sxs-lookup"><span data-stu-id="7353a-149">Specifies the settings that the Task Scheduler service uses to obtain a network profile.</span></span> <span data-ttu-id="7353a-150">Le service de Planificateur de tâches vérifie la disponibilité de ce réseau lorsque l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="7353a-150">The Task Scheduler service checks the availability of this network when the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element is set to **True**.</span></span><br/> |
| [<span data-ttu-id="7353a-151">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="7353a-151">**Priority**</span></span>](taskschedulerschema-priority-settingstype-element.md)                                               | [<span data-ttu-id="7353a-152">**priorityType**</span><span class="sxs-lookup"><span data-stu-id="7353a-152">**priorityType**</span></span>](taskschedulerschema-prioritytype-simpletype.md)                               | <span data-ttu-id="7353a-153">Spécifie le niveau de priorité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7353a-153">Specifies the priority level for the task.</span></span><br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="7353a-154">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="7353a-154">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [<span data-ttu-id="7353a-155">**restartType**</span><span class="sxs-lookup"><span data-stu-id="7353a-155">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md)                                | <span data-ttu-id="7353a-156">Spécifie que le Planificateur de tâches essaiera de redémarrer la tâche si elle échoue pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="7353a-156">Specifies that the Task Scheduler will attempt to restart the task if it fails for any reason.</span></span> <br/>                                                                                                                                                                                                          |
| [<span data-ttu-id="7353a-157">**RunOnlyIfIdle**</span><span class="sxs-lookup"><span data-stu-id="7353a-157">**RunOnlyIfIdle**</span></span>](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | <span data-ttu-id="7353a-158">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-158">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-159">Spécifie que la tâche est exécutée uniquement lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="7353a-159">Specifies that the task is run only when the computer is in an idle state.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="7353a-160">**RunOnlyIfNetworkAvailable**</span><span class="sxs-lookup"><span data-stu-id="7353a-160">**RunOnlyIfNetworkAvailable**</span></span>](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | <span data-ttu-id="7353a-161">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-161">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-162">Spécifie que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.</span><span class="sxs-lookup"><span data-stu-id="7353a-162">Specifies that the Task Scheduler will run the task only when a network is available.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="7353a-163">**StartWhenAvailable**</span><span class="sxs-lookup"><span data-stu-id="7353a-163">**StartWhenAvailable**</span></span>](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | <span data-ttu-id="7353a-164">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-164">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-165">Spécifie que les Planificateur de tâches peuvent démarrer la tâche à tout moment une fois l’heure planifiée passée.</span><span class="sxs-lookup"><span data-stu-id="7353a-165">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="7353a-166">**StopIfGoingOnBatteries**</span><span class="sxs-lookup"><span data-stu-id="7353a-166">**StopIfGoingOnBatteries**</span></span>](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | <span data-ttu-id="7353a-167">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-167">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-168">Spécifie que la tâche sera arrêtée si l’ordinateur bascule sur la batterie.</span><span class="sxs-lookup"><span data-stu-id="7353a-168">Specifies that the task will be stopped if the computer switches to battery power.</span></span> <br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="7353a-169">**UseUnifiedSchedulingEngine**</span><span class="sxs-lookup"><span data-stu-id="7353a-169">**UseUnifiedSchedulingEngine**</span></span>](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | <span data-ttu-id="7353a-170">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-170">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-171">Spécifie que la tâche est exécutée à l’aide du moteur de planification unifié.</span><span class="sxs-lookup"><span data-stu-id="7353a-171">Specifies that the task is run by using the Unified Scheduling Engine.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="7353a-172">**WakeToRun**</span><span class="sxs-lookup"><span data-stu-id="7353a-172">**WakeToRun**</span></span>](taskschedulerschema-waketorun-settingstype-element.md)                                             | <span data-ttu-id="7353a-173">boolean</span><span class="sxs-lookup"><span data-stu-id="7353a-173">boolean</span></span>                                                                                           | <span data-ttu-id="7353a-174">Spécifie que Planificateur de tâches met en éveil l’ordinateur avant d’exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="7353a-174">Specifies that Task Scheduler will wake the computer before it runs the task.</span></span><br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="7353a-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7353a-175">Requirements</span></span>



| <span data-ttu-id="7353a-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7353a-176">Requirement</span></span> | <span data-ttu-id="7353a-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="7353a-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7353a-178">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7353a-178">Minimum supported client</span></span><br/> | <span data-ttu-id="7353a-179">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7353a-179">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7353a-180">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7353a-180">Minimum supported server</span></span><br/> | <span data-ttu-id="7353a-181">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7353a-181">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7353a-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7353a-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7353a-183">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7353a-183">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="7353a-184">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7353a-184">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





