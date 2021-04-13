---
title: Élément ExecutionTimeLimit (triggerBaseType)
description: Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- Élément ExecutionTimeLimit Planificateur de tâches
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466286"
---
# <a name="executiontimelimit-triggerbasetype-element"></a><span data-ttu-id="b72b2-104">Élément ExecutionTimeLimit (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="b72b2-104">ExecutionTimeLimit (triggerBaseType) Element</span></span>

<span data-ttu-id="b72b2-105">Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.</span><span class="sxs-lookup"><span data-stu-id="b72b2-105">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="b72b2-106">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="b72b2-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="b72b2-107">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="b72b2-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

<span data-ttu-id="b72b2-108">L’élément **ExecutionTimeLimit** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b72b2-108">The **ExecutionTimeLimit** element is defined by the [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b72b2-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b72b2-109">Parent element</span></span>



| <span data-ttu-id="b72b2-110">Élément</span><span class="sxs-lookup"><span data-stu-id="b72b2-110">Element</span></span>                                                                                     | <span data-ttu-id="b72b2-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="b72b2-111">Derived from</span></span>                                                                               | <span data-ttu-id="b72b2-112">Description</span><span class="sxs-lookup"><span data-stu-id="b72b2-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b72b2-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="b72b2-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="b72b2-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b72b2-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="b72b2-115">Spécifie un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="b72b2-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="b72b2-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="b72b2-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="b72b2-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b72b2-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="b72b2-118">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="b72b2-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="b72b2-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="b72b2-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="b72b2-120">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b72b2-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="b72b2-121">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="b72b2-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="b72b2-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="b72b2-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="b72b2-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b72b2-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="b72b2-124">Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="b72b2-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="b72b2-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="b72b2-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="b72b2-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b72b2-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="b72b2-127">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="b72b2-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="b72b2-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="b72b2-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="b72b2-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b72b2-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="b72b2-130">Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="b72b2-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="b72b2-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="b72b2-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="b72b2-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="b72b2-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="b72b2-133">Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="b72b2-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="b72b2-134">Notes</span><span class="sxs-lookup"><span data-stu-id="b72b2-134">Remarks</span></span>

<span data-ttu-id="b72b2-135">Pour le développement de scripts, la limite de durée d’exécution est spécifiée à l’aide de la propriété [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) qui est héritée par tous les objets déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="b72b2-135">For scripting development, the execution time limit is specified using the [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="b72b2-136">Pour le développement C++, le délai d’exécution est spécifié à l’aide de la propriété [**ITrigger :: ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) qui est héritée par les interfaces de déclencheur All.</span><span class="sxs-lookup"><span data-stu-id="b72b2-136">For C++ development, the execution time limit is specified using the [**ITrigger::ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="b72b2-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b72b2-137">Requirements</span></span>



| <span data-ttu-id="b72b2-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b72b2-138">Requirement</span></span> | <span data-ttu-id="b72b2-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="b72b2-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b72b2-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b72b2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b72b2-141">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b72b2-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b72b2-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b72b2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b72b2-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b72b2-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b72b2-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b72b2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72b2-145">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b72b2-145">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b72b2-146">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b72b2-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





