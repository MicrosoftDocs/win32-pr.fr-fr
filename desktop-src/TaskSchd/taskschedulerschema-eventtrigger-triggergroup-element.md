---
title: Élément EventTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- déclencheur d’événement Planificateur de tâches, élément
- EventTrigger, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466283"
---
# <a name="eventtrigger-triggergroup-element"></a><span data-ttu-id="44a23-105">Élément EventTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="44a23-105">EventTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="44a23-106">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="44a23-106">Specifies a trigger that starts a task when a system event occurs.</span></span>

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

<span data-ttu-id="44a23-107">L’élément **EventTrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="44a23-107">The **EventTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="44a23-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="44a23-108">Parent element</span></span>



| <span data-ttu-id="44a23-109">Élément</span><span class="sxs-lookup"><span data-stu-id="44a23-109">Element</span></span>                                                           | <span data-ttu-id="44a23-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="44a23-110">Derived from</span></span>                                                         | <span data-ttu-id="44a23-111">Description</span><span class="sxs-lookup"><span data-stu-id="44a23-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="44a23-112">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="44a23-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="44a23-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="44a23-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="44a23-114">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="44a23-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="44a23-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="44a23-115">Child elements</span></span>



| <span data-ttu-id="44a23-116">Élément</span><span class="sxs-lookup"><span data-stu-id="44a23-116">Element</span></span>                                                                                              | <span data-ttu-id="44a23-117">Type</span><span class="sxs-lookup"><span data-stu-id="44a23-117">Type</span></span>                                                                     | <span data-ttu-id="44a23-118">Description</span><span class="sxs-lookup"><span data-stu-id="44a23-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44a23-119">**Délai (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="44a23-119">**Delay (eventTriggerType)**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="44a23-120">duration</span><span class="sxs-lookup"><span data-stu-id="44a23-120">duration</span></span>                                                                 | <span data-ttu-id="44a23-121">Spécifie la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="44a23-121">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                |
| [<span data-ttu-id="44a23-122">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="44a23-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)             | <span data-ttu-id="44a23-123">boolean</span><span class="sxs-lookup"><span data-stu-id="44a23-123">boolean</span></span>                                                                  | <span data-ttu-id="44a23-124">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="44a23-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="44a23-125">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="44a23-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)     | <span data-ttu-id="44a23-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="44a23-126">dateTime</span></span>                                                                 | <span data-ttu-id="44a23-127">Spécifie la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="44a23-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="44a23-128">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="44a23-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="44a23-129">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="44a23-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)       | [<span data-ttu-id="44a23-130">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="44a23-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="44a23-131">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="44a23-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="44a23-132">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="44a23-132">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md) | <span data-ttu-id="44a23-133">dateTime</span><span class="sxs-lookup"><span data-stu-id="44a23-133">dateTime</span></span>                                                                 | <span data-ttu-id="44a23-134">Spécifie la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="44a23-134">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="44a23-135">**Abonnement (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="44a23-135">**Subscription (eventTriggerType)**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | <span data-ttu-id="44a23-136">string</span><span class="sxs-lookup"><span data-stu-id="44a23-136">string</span></span>                                                                   | <span data-ttu-id="44a23-137">Spécifie la requête XPath qui identifie l’événement qui déclenche le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="44a23-137">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                             |



## <a name="attributes"></a><span data-ttu-id="44a23-138">Attributs</span><span class="sxs-lookup"><span data-stu-id="44a23-138">Attributes</span></span>



| <span data-ttu-id="44a23-139">Nom</span><span class="sxs-lookup"><span data-stu-id="44a23-139">Name</span></span> | <span data-ttu-id="44a23-140">Type</span><span class="sxs-lookup"><span data-stu-id="44a23-140">Type</span></span> | <span data-ttu-id="44a23-141">Description</span><span class="sxs-lookup"><span data-stu-id="44a23-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="44a23-142">Id</span><span class="sxs-lookup"><span data-stu-id="44a23-142">Id</span></span>   | <span data-ttu-id="44a23-143">id</span><span class="sxs-lookup"><span data-stu-id="44a23-143">ID</span></span>   | <span data-ttu-id="44a23-144">Identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="44a23-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="44a23-145">Notes</span><span class="sxs-lookup"><span data-stu-id="44a23-145">Remarks</span></span>

<span data-ttu-id="44a23-146">Vous pouvez créer au maximum 500 tâches avec des abonnements aux événements.</span><span class="sxs-lookup"><span data-stu-id="44a23-146">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="44a23-147">Un abonnement aux événements qui interroge un grand nombre d’événements peut être utilisé pour déclencher une tâche qui utilise la même action en réponse aux événements journalisés.</span><span class="sxs-lookup"><span data-stu-id="44a23-147">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="44a23-148">Pour le développement de scripts, un déclencheur d’événement est défini par l’objet [**EventTrigger**](eventtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="44a23-148">For script development, an event trigger is defined by the [**EventTrigger**](eventtrigger.md) object.</span></span>

<span data-ttu-id="44a23-149">Pour le développement C++, un déclencheur d’événement est défini par l’interface [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .</span><span class="sxs-lookup"><span data-stu-id="44a23-149">For C++ development, an event trigger is defined by the [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="44a23-150">Exemples</span><span class="sxs-lookup"><span data-stu-id="44a23-150">Examples</span></span>

<span data-ttu-id="44a23-151">Pour obtenir un exemple complet du code XML d’une tâche qui utilise un déclencheur d’événement, consultez [exemple de déclencheur d’événements (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44a23-151">For a complete example of the XML for a task that uses an event trigger, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="44a23-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44a23-152">Requirements</span></span>



| <span data-ttu-id="44a23-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44a23-153">Requirement</span></span> | <span data-ttu-id="44a23-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="44a23-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44a23-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44a23-155">Minimum supported client</span></span><br/> | <span data-ttu-id="44a23-156">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44a23-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44a23-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44a23-157">Minimum supported server</span></span><br/> | <span data-ttu-id="44a23-158">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44a23-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44a23-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44a23-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a23-160">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="44a23-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

