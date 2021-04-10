---
title: Élément LogonTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- déclencheur LOGON, élément XML
- Élément LogonTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317194"
---
# <a name="logontrigger-triggergroup-element"></a><span data-ttu-id="cce0b-105">Élément LogonTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="cce0b-105">LogonTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="cce0b-106">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="cce0b-106">Specifies a trigger that starts a task when a user logs on.</span></span>

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

<span data-ttu-id="cce0b-107">L’élément **LogonTrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="cce0b-107">The **LogonTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="cce0b-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="cce0b-108">Parent element</span></span>



| <span data-ttu-id="cce0b-109">Élément</span><span class="sxs-lookup"><span data-stu-id="cce0b-109">Element</span></span>                                                           | <span data-ttu-id="cce0b-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="cce0b-110">Derived from</span></span>                                                         | <span data-ttu-id="cce0b-111">Description</span><span class="sxs-lookup"><span data-stu-id="cce0b-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="cce0b-112">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="cce0b-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="cce0b-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="cce0b-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="cce0b-114">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="cce0b-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="cce0b-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cce0b-115">Child elements</span></span>



| <span data-ttu-id="cce0b-116">Élément</span><span class="sxs-lookup"><span data-stu-id="cce0b-116">Element</span></span>                                                                                                        | <span data-ttu-id="cce0b-117">Type</span><span class="sxs-lookup"><span data-stu-id="cce0b-117">Type</span></span>                                                                     | <span data-ttu-id="cce0b-118">Description</span><span class="sxs-lookup"><span data-stu-id="cce0b-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cce0b-119">**Délai (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-119">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)                         | <span data-ttu-id="cce0b-120">duration</span><span class="sxs-lookup"><span data-stu-id="cce0b-120">duration</span></span>                                                                 | <span data-ttu-id="cce0b-121">Intervalle de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="cce0b-121">Amount of time between when the user logs on and when the task is started.</span></span><br/>                                              |
| [<span data-ttu-id="cce0b-122">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="cce0b-123">boolean</span><span class="sxs-lookup"><span data-stu-id="cce0b-123">boolean</span></span>                                                                  | <span data-ttu-id="cce0b-124">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="cce0b-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="cce0b-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="cce0b-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="cce0b-126">dateTime</span></span>                                                                 | <span data-ttu-id="cce0b-127">Spécifie la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cce0b-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="cce0b-128">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="cce0b-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="cce0b-129">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="cce0b-130">duration</span><span class="sxs-lookup"><span data-stu-id="cce0b-130">duration</span></span>                                                                 | <span data-ttu-id="cce0b-131">Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cce0b-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="cce0b-132">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="cce0b-133">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="cce0b-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="cce0b-134">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="cce0b-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="cce0b-135">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="cce0b-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="cce0b-136">dateTime</span></span>                                                                 | <span data-ttu-id="cce0b-137">Spécifie la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cce0b-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="cce0b-138">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-138">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)                       | <span data-ttu-id="cce0b-139">string</span><span class="sxs-lookup"><span data-stu-id="cce0b-139">string</span></span>                                                                   | <span data-ttu-id="cce0b-140">Identificateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cce0b-140">Identifier of the user.</span></span> <span data-ttu-id="cce0b-141">La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cce0b-141">The task is started when this user logs onto the computer.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="cce0b-142">Notes</span><span class="sxs-lookup"><span data-stu-id="cce0b-142">Remarks</span></span>

<span data-ttu-id="cce0b-143">Pour le développement de scripts, un déclencheur LOGON est spécifié à l’aide de l’objet [**LogonTrigger**](logontrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="cce0b-143">For scripting development, a logon trigger is specified using the [**LogonTrigger**](logontrigger.md) object.</span></span>

<span data-ttu-id="cce0b-144">Pour le développement C++, un déclencheur LOGON est spécifié à l’aide de l’interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .</span><span class="sxs-lookup"><span data-stu-id="cce0b-144">For C++ development, a logon trigger is specified using the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface.</span></span>

<span data-ttu-id="cce0b-145">Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) et [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cce0b-145">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="cce0b-146">Ces éléments doivent être ajoutés dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cce0b-146">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="cce0b-147">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-147">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="cce0b-148">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-148">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="cce0b-149">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-149">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="cce0b-150">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-150">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="cce0b-151">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-151">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="cce0b-152">**UserId (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-152">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)
-   [<span data-ttu-id="cce0b-153">**Délai (logonTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="cce0b-153">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a><span data-ttu-id="cce0b-154">Attributs</span><span class="sxs-lookup"><span data-stu-id="cce0b-154">Attributes</span></span>

<span data-ttu-id="cce0b-155">L’attribut indiqué ci-dessous est défini par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cce0b-155">The attribute listed below is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span>

-   <span data-ttu-id="cce0b-156">ID : identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="cce0b-156">Id: Identifier of the trigger.</span></span>

## <a name="examples"></a><span data-ttu-id="cce0b-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="cce0b-157">Examples</span></span>

<span data-ttu-id="cce0b-158">Pour obtenir un exemple complet du code XML d’une tâche qui utilise un déclencheur LOGON, consultez [exemple de déclencheur de connexion (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="cce0b-158">For a complete example of the XML for a task that uses a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cce0b-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cce0b-159">Requirements</span></span>



| <span data-ttu-id="cce0b-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cce0b-160">Requirement</span></span> | <span data-ttu-id="cce0b-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="cce0b-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cce0b-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cce0b-162">Minimum supported client</span></span><br/> | <span data-ttu-id="cce0b-163">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cce0b-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cce0b-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cce0b-164">Minimum supported server</span></span><br/> | <span data-ttu-id="cce0b-165">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cce0b-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cce0b-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cce0b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce0b-167">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="cce0b-167">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





