---
title: Élément IdleTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- déclencheur Idle, élément XML
- Élément IdleTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032534"
---
# <a name="idletrigger-triggergroup-element"></a><span data-ttu-id="20a21-105">Élément IdleTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="20a21-105">IdleTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="20a21-106">Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="20a21-106">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span> <span data-ttu-id="20a21-107">Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="20a21-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

<span data-ttu-id="20a21-108">L’élément **IdleTrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="20a21-108">The **IdleTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="20a21-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="20a21-109">Parent element</span></span>



| <span data-ttu-id="20a21-110">Élément</span><span class="sxs-lookup"><span data-stu-id="20a21-110">Element</span></span>                                                           | <span data-ttu-id="20a21-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="20a21-111">Derived from</span></span>                                                         | <span data-ttu-id="20a21-112">Description</span><span class="sxs-lookup"><span data-stu-id="20a21-112">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="20a21-113">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="20a21-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="20a21-114">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="20a21-114">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="20a21-115">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="20a21-115">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="20a21-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="20a21-116">Child elements</span></span>



| <span data-ttu-id="20a21-117">Élément</span><span class="sxs-lookup"><span data-stu-id="20a21-117">Element</span></span>                                                                                                        | <span data-ttu-id="20a21-118">Type</span><span class="sxs-lookup"><span data-stu-id="20a21-118">Type</span></span>                                                                     | <span data-ttu-id="20a21-119">Description</span><span class="sxs-lookup"><span data-stu-id="20a21-119">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20a21-120">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-120">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="20a21-121">boolean</span><span class="sxs-lookup"><span data-stu-id="20a21-121">boolean</span></span>                                                                  | <span data-ttu-id="20a21-122">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="20a21-122">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="20a21-123">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-123">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="20a21-124">dateTime</span><span class="sxs-lookup"><span data-stu-id="20a21-124">dateTime</span></span>                                                                 | <span data-ttu-id="20a21-125">Spécifie la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="20a21-125">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="20a21-126">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="20a21-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="20a21-127">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-127">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="20a21-128">duration</span><span class="sxs-lookup"><span data-stu-id="20a21-128">duration</span></span>                                                                 | <span data-ttu-id="20a21-129">Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="20a21-129">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="20a21-130">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-130">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="20a21-131">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="20a21-131">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="20a21-132">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="20a21-132">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="20a21-133">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-133">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="20a21-134">dateTime</span><span class="sxs-lookup"><span data-stu-id="20a21-134">dateTime</span></span>                                                                 | <span data-ttu-id="20a21-135">Spécifie la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="20a21-135">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="20a21-136">Attributs</span><span class="sxs-lookup"><span data-stu-id="20a21-136">Attributes</span></span>



| <span data-ttu-id="20a21-137">Nom</span><span class="sxs-lookup"><span data-stu-id="20a21-137">Name</span></span> | <span data-ttu-id="20a21-138">Type</span><span class="sxs-lookup"><span data-stu-id="20a21-138">Type</span></span>   | <span data-ttu-id="20a21-139">Description</span><span class="sxs-lookup"><span data-stu-id="20a21-139">Description</span></span>                               |
|------|--------|-------------------------------------------|
| <span data-ttu-id="20a21-140">Id</span><span class="sxs-lookup"><span data-stu-id="20a21-140">Id</span></span>   | <span data-ttu-id="20a21-141">string</span><span class="sxs-lookup"><span data-stu-id="20a21-141">string</span></span> | <span data-ttu-id="20a21-142">Identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="20a21-142">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="20a21-143">Notes</span><span class="sxs-lookup"><span data-stu-id="20a21-143">Remarks</span></span>

<span data-ttu-id="20a21-144">Pour le développement de scripts, un déclencheur inactif est spécifié à l’aide de l’objet [**IdleTrigger**](idletrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="20a21-144">For scripting development, an idle trigger is specified using the [**IdleTrigger**](idletrigger.md) object.</span></span>

<span data-ttu-id="20a21-145">Pour le développement C++, un déclencheur inactif est spécifié à l’aide de l’interface [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .</span><span class="sxs-lookup"><span data-stu-id="20a21-145">For C++ development, an idle trigger is specified using the [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interface.</span></span>

<span data-ttu-id="20a21-146">Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="20a21-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="20a21-147">Ces éléments doivent être ajoutés dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="20a21-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="20a21-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="20a21-149">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="20a21-150">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="20a21-151">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="20a21-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="20a21-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="20a21-153">Exemples</span><span class="sxs-lookup"><span data-stu-id="20a21-153">Examples</span></span>

<span data-ttu-id="20a21-154">Le code XML suivant définit un déclencheur inactif.</span><span class="sxs-lookup"><span data-stu-id="20a21-154">The following XML defines an idle trigger.</span></span>


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a><span data-ttu-id="20a21-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20a21-155">Requirements</span></span>



| <span data-ttu-id="20a21-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20a21-156">Requirement</span></span> | <span data-ttu-id="20a21-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="20a21-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="20a21-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a21-158">Minimum supported client</span></span><br/> | <span data-ttu-id="20a21-159">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20a21-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="20a21-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a21-160">Minimum supported server</span></span><br/> | <span data-ttu-id="20a21-161">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20a21-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20a21-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20a21-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a21-163">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="20a21-163">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="20a21-164">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="20a21-164">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

