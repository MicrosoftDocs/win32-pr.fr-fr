---
title: Élément de répétition (triggerBaseType)
description: Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Planificateur de tâches d’élément à répétition
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466015"
---
# <a name="repetition-triggerbasetype-element"></a><span data-ttu-id="60954-104">Élément de répétition (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="60954-104">Repetition (triggerBaseType) Element</span></span>

<span data-ttu-id="60954-105">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="60954-105">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

<span data-ttu-id="60954-106">L’élément à **répétition** est défini par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="60954-106">The **Repetition** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="60954-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="60954-107">Parent element</span></span>



| <span data-ttu-id="60954-108">Élément</span><span class="sxs-lookup"><span data-stu-id="60954-108">Element</span></span>                                                                                     | <span data-ttu-id="60954-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="60954-109">Derived from</span></span>                                                                               | <span data-ttu-id="60954-110">Description</span><span class="sxs-lookup"><span data-stu-id="60954-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60954-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="60954-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="60954-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="60954-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="60954-113">Spécifie un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="60954-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="60954-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="60954-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="60954-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="60954-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="60954-116">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="60954-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="60954-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="60954-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="60954-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="60954-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="60954-119">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="60954-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="60954-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="60954-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="60954-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="60954-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="60954-122">Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="60954-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="60954-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="60954-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="60954-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="60954-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="60954-125">Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="60954-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="60954-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="60954-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="60954-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="60954-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="60954-128">Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="60954-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="60954-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="60954-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="60954-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="60954-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="60954-131">Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="60954-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="child-elements"></a><span data-ttu-id="60954-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="60954-132">Child elements</span></span>



| <span data-ttu-id="60954-133">Élément</span><span class="sxs-lookup"><span data-stu-id="60954-133">Element</span></span>                                                                                   | <span data-ttu-id="60954-134">Type</span><span class="sxs-lookup"><span data-stu-id="60954-134">Type</span></span>     | <span data-ttu-id="60954-135">Description</span><span class="sxs-lookup"><span data-stu-id="60954-135">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60954-136">**Duration**</span><span class="sxs-lookup"><span data-stu-id="60954-136">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   | <span data-ttu-id="60954-137">duration</span><span class="sxs-lookup"><span data-stu-id="60954-137">duration</span></span> | <span data-ttu-id="60954-138">Spécifie la durée de répétition du modèle.</span><span class="sxs-lookup"><span data-stu-id="60954-138">Specifies how long the pattern is repeated.</span></span><br/>                                                              |
| [<span data-ttu-id="60954-139">**Défini**</span><span class="sxs-lookup"><span data-stu-id="60954-139">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   | <span data-ttu-id="60954-140">duration</span><span class="sxs-lookup"><span data-stu-id="60954-140">duration</span></span> | <span data-ttu-id="60954-141">Spécifie la durée entre chaque redémarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="60954-141">Specifies the amount of time between each restart of the task.</span></span><br/>                                           |
| [<span data-ttu-id="60954-142">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="60954-142">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="60954-143">boolean</span><span class="sxs-lookup"><span data-stu-id="60954-143">boolean</span></span>  | <span data-ttu-id="60954-144">Spécifie qu’une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.</span><span class="sxs-lookup"><span data-stu-id="60954-144">Specifies that a running instances of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="60954-145">Notes</span><span class="sxs-lookup"><span data-stu-id="60954-145">Remarks</span></span>

<span data-ttu-id="60954-146">Si vous spécifiez une durée de répétition pour une tâche, vous devez également spécifier l’intervalle de répétition.</span><span class="sxs-lookup"><span data-stu-id="60954-146">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="60954-147">Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est lancée cinq fois.</span><span class="sxs-lookup"><span data-stu-id="60954-147">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="60954-148">Les cinq répétitions peuvent être définies par le modèle suivant.</span><span class="sxs-lookup"><span data-stu-id="60954-148">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="60954-149">Une tâche commence au début de la première minute.</span><span class="sxs-lookup"><span data-stu-id="60954-149">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="60954-150">La tâche suivante démarre à la fin de la première minute.</span><span class="sxs-lookup"><span data-stu-id="60954-150">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="60954-151">La tâche suivante démarre à la fin de la seconde minute.</span><span class="sxs-lookup"><span data-stu-id="60954-151">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="60954-152">La tâche suivante démarre à la fin de la troisième minute.</span><span class="sxs-lookup"><span data-stu-id="60954-152">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="60954-153">La tâche suivante démarre à la fin de la quatrième minute.</span><span class="sxs-lookup"><span data-stu-id="60954-153">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="60954-154">**Windows Server 2003, Windows XP et windows 2000 :** Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est lancée quatre fois.</span><span class="sxs-lookup"><span data-stu-id="60954-154">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="60954-155">**Windows Vista, Windows 7, Windows server 2008, Windows 8 et Windows server 2012 :** En règle générale, la définition de la durée de répétition sur un multiple exact de l’intervalle produit les nombres décrits ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="60954-155">**Windows Vista, Windows 7, Windows Server 2008, Windows 8 and Windows Server 2012:** Usually, setting the repetition duration to an exact multiple of the interval yields the numbers described above.</span></span> <span data-ttu-id="60954-156">Toutefois, dans certaines conditions de charge élevée, il est possible que le délai d’expiration soit écoulé avant que TaskScheduler puisse lancer l’intervalle de tâche final.</span><span class="sxs-lookup"><span data-stu-id="60954-156">However, under certain heavy load conditions, it is possible for the duration to timeout before TaskScheduler can launch the final task interval.</span></span>

<span data-ttu-id="60954-157">Pour le développement de scripts, le modèle de répétition est spécifié à l’aide de la propriété [**déclencheur.**](trigger-repetition.md) reformation qui est héritée par tous les objets déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="60954-157">For scripting development, the repetition pattern is specified using the [**Trigger.Repetition**](trigger-repetition.md) property that is inherited by all the trigger objects.</span></span>

<span data-ttu-id="60954-158">Pour le développement C++, le modèle de répétition est spécifié à l’aide de la propriété [**ITRigger :: rerépétition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) qui est héritée par toutes les interfaces de déclencheur.</span><span class="sxs-lookup"><span data-stu-id="60954-158">For C++ development, the repetition pattern is specified using the [**ITRigger::Repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) property that is inherited by all the trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="60954-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="60954-159">Examples</span></span>

<span data-ttu-id="60954-160">Le code XML suivant définit un élément de déclencheur de démarrage qui spécifie un modèle de répétition pour un déclencheur.</span><span class="sxs-lookup"><span data-stu-id="60954-160">The following XML defines a boot trigger element that specifies a repetition pattern for a trigger.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="60954-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60954-161">Requirements</span></span>



| <span data-ttu-id="60954-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60954-162">Requirement</span></span> | <span data-ttu-id="60954-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="60954-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60954-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60954-164">Minimum supported client</span></span><br/> | <span data-ttu-id="60954-165">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60954-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60954-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60954-166">Minimum supported server</span></span><br/> | <span data-ttu-id="60954-167">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60954-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60954-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60954-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60954-169">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="60954-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="60954-170">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="60954-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





