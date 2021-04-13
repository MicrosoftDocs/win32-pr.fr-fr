---
title: Élément TimeTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Élément TimeTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466271"
---
# <a name="timetrigger-triggergroup-element"></a><span data-ttu-id="b4bca-104">Élément TimeTrigger (triggerGroup)</span><span class="sxs-lookup"><span data-stu-id="b4bca-104">TimeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="b4bca-105">Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="b4bca-105">Specifies a trigger that starts a task when the trigger is activated.</span></span>

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

<span data-ttu-id="b4bca-106">L’élément **timetrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="b4bca-106">The **TimeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="b4bca-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b4bca-107">Parent element</span></span>



| <span data-ttu-id="b4bca-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b4bca-108">Element</span></span>                                                           | <span data-ttu-id="b4bca-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="b4bca-109">Derived from</span></span>                                                         | <span data-ttu-id="b4bca-110">Description</span><span class="sxs-lookup"><span data-stu-id="b4bca-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="b4bca-111">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="b4bca-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="b4bca-112">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="b4bca-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="b4bca-113">Spécifie les déclencheurs qui démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="b4bca-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="b4bca-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b4bca-114">Child elements</span></span>



| <span data-ttu-id="b4bca-115">Élément</span><span class="sxs-lookup"><span data-stu-id="b4bca-115">Element</span></span>                                                                                                        | <span data-ttu-id="b4bca-116">Type</span><span class="sxs-lookup"><span data-stu-id="b4bca-116">Type</span></span>                                                                     | <span data-ttu-id="b4bca-117">Description</span><span class="sxs-lookup"><span data-stu-id="b4bca-117">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4bca-118">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-118">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="b4bca-119">boolean</span><span class="sxs-lookup"><span data-stu-id="b4bca-119">boolean</span></span>                                                                  | <span data-ttu-id="b4bca-120">Spécifie que le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="b4bca-120">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="b4bca-121">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-121">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="b4bca-122">dateTime</span><span class="sxs-lookup"><span data-stu-id="b4bca-122">dateTime</span></span>                                                                 | <span data-ttu-id="b4bca-123">Spécifie la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="b4bca-123">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="b4bca-124">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b4bca-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="b4bca-125">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-125">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="b4bca-126">duration</span><span class="sxs-lookup"><span data-stu-id="b4bca-126">duration</span></span>                                                                 | <span data-ttu-id="b4bca-127">Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="b4bca-127">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="b4bca-128">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-128">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="b4bca-129">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="b4bca-129">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="b4bca-130">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="b4bca-130">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="b4bca-131">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-131">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="b4bca-132">dateTime</span><span class="sxs-lookup"><span data-stu-id="b4bca-132">dateTime</span></span>                                                                 | <span data-ttu-id="b4bca-133">Spécifie la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="b4bca-133">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="b4bca-134">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b4bca-134">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="b4bca-135">Attributs</span><span class="sxs-lookup"><span data-stu-id="b4bca-135">Attributes</span></span>



| <span data-ttu-id="b4bca-136">Nom</span><span class="sxs-lookup"><span data-stu-id="b4bca-136">Name</span></span> | <span data-ttu-id="b4bca-137">Type</span><span class="sxs-lookup"><span data-stu-id="b4bca-137">Type</span></span>       | <span data-ttu-id="b4bca-138">Description</span><span class="sxs-lookup"><span data-stu-id="b4bca-138">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="b4bca-139">Id</span><span class="sxs-lookup"><span data-stu-id="b4bca-139">Id</span></span>   | <span data-ttu-id="b4bca-140">**string**</span><span class="sxs-lookup"><span data-stu-id="b4bca-140">**string**</span></span> | <span data-ttu-id="b4bca-141">Identificateur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="b4bca-141">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b4bca-142">Notes</span><span class="sxs-lookup"><span data-stu-id="b4bca-142">Remarks</span></span>

<span data-ttu-id="b4bca-143">L’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) est un élément requis pour les déclencheurs de temps et de calendrier (**timetrigger** et [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="b4bca-143">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers (**TimeTrigger** and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="b4bca-144">Pour le développement de scripts, un déclencheur Time est spécifié à l’aide de l’objet [**timetrigger**](timetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="b4bca-144">For scripting development, a time trigger is specified using the [**TimeTrigger**](timetrigger.md) object.</span></span>

<span data-ttu-id="b4bca-145">Pour le développement C++, un déclencheur Time est spécifié à l’aide de l’interface [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) .</span><span class="sxs-lookup"><span data-stu-id="b4bca-145">For C++ development, a time trigger is specified using the [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) interface.</span></span>

<span data-ttu-id="b4bca-146">Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b4bca-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="b4bca-147">Ces éléments doivent être ajoutés dans l’ordre indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b4bca-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="b4bca-148">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="b4bca-149">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="b4bca-150">**Activé (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="b4bca-151">**Répétition (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="b4bca-152">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="b4bca-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="b4bca-153">Exemples</span><span class="sxs-lookup"><span data-stu-id="b4bca-153">Examples</span></span>

<span data-ttu-id="b4bca-154">Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur d’heure, consultez [exemple de déclencheur temporel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="b4bca-154">For a complete example of the XML for a task that specifies a time trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4bca-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4bca-155">Requirements</span></span>



| <span data-ttu-id="b4bca-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4bca-156">Requirement</span></span> | <span data-ttu-id="b4bca-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4bca-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4bca-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4bca-158">Minimum supported client</span></span><br/> | <span data-ttu-id="b4bca-159">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4bca-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b4bca-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4bca-160">Minimum supported server</span></span><br/> | <span data-ttu-id="b4bca-161">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4bca-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4bca-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4bca-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4bca-163">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b4bca-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





