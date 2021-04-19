---
title: Élément RegistrationTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Planificateur de tâches de déclencheur d’inscription, élément XML
- Élément RegistrationTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511783"
---
# <a name="registrationtrigger-triggergroup-element"></a><span data-ttu-id="1fa06-105">Élément RegistrationTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="1fa06-105">RegistrationTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="1fa06-106">Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="1fa06-106">Specifies a trigger that starts a task when the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

<span data-ttu-id="1fa06-107">L’élément **RegistrationTrigger** est défini par le type complexe [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1fa06-107">The **RegistrationTrigger** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1fa06-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1fa06-108">Parent element</span></span>



| <span data-ttu-id="1fa06-109">Élément</span><span class="sxs-lookup"><span data-stu-id="1fa06-109">Element</span></span>                                                           | <span data-ttu-id="1fa06-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="1fa06-110">Derived from</span></span>                                                         | <span data-ttu-id="1fa06-111">Description</span><span class="sxs-lookup"><span data-stu-id="1fa06-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="1fa06-112">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="1fa06-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="1fa06-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="1fa06-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="1fa06-114">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="1fa06-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="1fa06-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1fa06-115">Child elements</span></span>



| <span data-ttu-id="1fa06-116">Élément</span><span class="sxs-lookup"><span data-stu-id="1fa06-116">Element</span></span>                                                                                                        | <span data-ttu-id="1fa06-117">Type</span><span class="sxs-lookup"><span data-stu-id="1fa06-117">Type</span></span>                                                                     | <span data-ttu-id="1fa06-118">Description</span><span class="sxs-lookup"><span data-stu-id="1fa06-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fa06-119">**Délai (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-119">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                   | <span data-ttu-id="1fa06-120">duration</span><span class="sxs-lookup"><span data-stu-id="1fa06-120">duration</span></span>                                                                 | <span data-ttu-id="1fa06-121">Spécifie la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="1fa06-121">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/>                          |
| [<span data-ttu-id="1fa06-122">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="1fa06-123">boolean</span><span class="sxs-lookup"><span data-stu-id="1fa06-123">boolean</span></span>                                                                  | <span data-ttu-id="1fa06-124">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="1fa06-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="1fa06-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="1fa06-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="1fa06-126">dateTime</span></span>                                                                 | <span data-ttu-id="1fa06-127">Spécifie la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="1fa06-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="1fa06-128">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="1fa06-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="1fa06-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="1fa06-130">duration</span><span class="sxs-lookup"><span data-stu-id="1fa06-130">duration</span></span>                                                                 | <span data-ttu-id="1fa06-131">Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="1fa06-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="1fa06-132">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="1fa06-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="1fa06-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="1fa06-134">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1fa06-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="1fa06-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="1fa06-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="1fa06-136">dateTime</span></span>                                                                 | <span data-ttu-id="1fa06-137">Spécifie la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="1fa06-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="1fa06-138">Attributs</span><span class="sxs-lookup"><span data-stu-id="1fa06-138">Attributes</span></span>



| <span data-ttu-id="1fa06-139">Nom</span><span class="sxs-lookup"><span data-stu-id="1fa06-139">Name</span></span> | <span data-ttu-id="1fa06-140">Type</span><span class="sxs-lookup"><span data-stu-id="1fa06-140">Type</span></span> | <span data-ttu-id="1fa06-141">Description</span><span class="sxs-lookup"><span data-stu-id="1fa06-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="1fa06-142">Id</span><span class="sxs-lookup"><span data-stu-id="1fa06-142">Id</span></span>   | <span data-ttu-id="1fa06-143">id</span><span class="sxs-lookup"><span data-stu-id="1fa06-143">ID</span></span>   | <span data-ttu-id="1fa06-144">Identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="1fa06-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1fa06-145">Notes</span><span class="sxs-lookup"><span data-stu-id="1fa06-145">Remarks</span></span>

<span data-ttu-id="1fa06-146">Pour le développement de scripts, un déclencheur d’inscription est spécifié à l’aide de l’objet [**RegistrationTrigger**](registrationtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="1fa06-146">For scripting development, a registration trigger is specified using the [**RegistrationTrigger**](registrationtrigger.md) object.</span></span>

<span data-ttu-id="1fa06-147">Pour le développement C++, un déclencheur d’inscription est spécifié à l’aide de l’interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .</span><span class="sxs-lookup"><span data-stu-id="1fa06-147">For C++ development, a registration trigger is specified using the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface.</span></span>

<span data-ttu-id="1fa06-148">Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) et [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1fa06-148">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="1fa06-149">Ces éléments doivent être ajoutés dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1fa06-149">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="1fa06-150">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-150">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="1fa06-151">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-151">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="1fa06-152">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-152">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="1fa06-153">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-153">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="1fa06-154">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-154">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="1fa06-155">**Délai (registrationTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="1fa06-155">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a><span data-ttu-id="1fa06-156">Exemples</span><span class="sxs-lookup"><span data-stu-id="1fa06-156">Examples</span></span>

<span data-ttu-id="1fa06-157">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur de démarrage, consultez [exemple de déclencheur d’inscription (XML)](registration-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="1fa06-157">For a complete example of the XML for a task that specifies a boot trigger, see [Registration Trigger Example (XML)](registration-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa06-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fa06-158">Requirements</span></span>



| <span data-ttu-id="1fa06-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fa06-159">Requirement</span></span> | <span data-ttu-id="1fa06-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa06-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1fa06-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fa06-161">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa06-162">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fa06-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1fa06-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fa06-163">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa06-164">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fa06-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fa06-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fa06-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa06-166">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1fa06-166">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1fa06-167">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1fa06-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





