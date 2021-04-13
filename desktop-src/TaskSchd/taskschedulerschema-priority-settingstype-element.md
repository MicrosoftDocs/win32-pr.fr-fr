---
title: Élément Priority (settingsType)
description: Spécifie le niveau de priorité de la tâche.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Élément Priority Planificateur de tâches
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384099"
---
# <a name="priority-settingstype-element"></a><span data-ttu-id="c66e1-104">Élément Priority (settingsType)</span><span class="sxs-lookup"><span data-stu-id="c66e1-104">Priority (settingsType) Element</span></span>

<span data-ttu-id="c66e1-105">Spécifie le niveau de priorité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="c66e1-105">Specifies the priority level for the task.</span></span>

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

<span data-ttu-id="c66e1-106">L’élément **Priority** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c66e1-106">The **Priority** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c66e1-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c66e1-107">Parent element</span></span>



| <span data-ttu-id="c66e1-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c66e1-108">Element</span></span>                                                           | <span data-ttu-id="c66e1-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c66e1-109">Derived from</span></span>                                                         | <span data-ttu-id="c66e1-110">Description</span><span class="sxs-lookup"><span data-stu-id="c66e1-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c66e1-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="c66e1-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c66e1-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c66e1-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c66e1-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="c66e1-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c66e1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c66e1-114">Remarks</span></span>

<span data-ttu-id="c66e1-115">Le niveau de priorité 0 est la priorité la plus élevée et le niveau de priorité 10 est la priorité la plus basse.</span><span class="sxs-lookup"><span data-stu-id="c66e1-115">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="c66e1-116">La valeur par défaut est 7.</span><span class="sxs-lookup"><span data-stu-id="c66e1-116">The default value is 7.</span></span> <span data-ttu-id="c66e1-117">Les valeurs minimales et maximales sont définies par le type simple [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="c66e1-117">The minimum and maximum values are set by the [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) simple type.</span></span> <span data-ttu-id="c66e1-118">Les niveaux de priorité 7 et 8 sont utilisés pour les tâches en arrière-plan, et les niveaux de priorité 4, 5 et 6 sont utilisés pour les tâches interactives.</span><span class="sxs-lookup"><span data-stu-id="c66e1-118">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="c66e1-119">L’action de la tâche est démarrée dans un processus avec une priorité basée sur une valeur de classe de priorité.</span><span class="sxs-lookup"><span data-stu-id="c66e1-119">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="c66e1-120">Une valeur de niveau de priorité (priorité de thread) est utilisée pour les actions de la tâche du gestionnaire COM, de la boîte de message et de l’e-mail.</span><span class="sxs-lookup"><span data-stu-id="c66e1-120">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="c66e1-121">Pour plus d’informations sur la classe de priorité et les valeurs de niveau de priorité, consultez [planification des priorités](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="c66e1-121">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="c66e1-122">Le tableau suivant répertorie les valeurs possibles pour l’élément **Priority** , ainsi que la classe de priorité correspondante et les valeurs de niveau de priorité.</span><span class="sxs-lookup"><span data-stu-id="c66e1-122">The following table lists the possible values for the **Priority** element, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="c66e1-123">Priorité de la tâche</span><span class="sxs-lookup"><span data-stu-id="c66e1-123">Task Priority</span></span> | <span data-ttu-id="c66e1-124">Classe de priorité</span><span class="sxs-lookup"><span data-stu-id="c66e1-124">Priority Class</span></span>                 | <span data-ttu-id="c66e1-125">Niveau de priorité</span><span class="sxs-lookup"><span data-stu-id="c66e1-125">Priority Level</span></span>                   |
|---------------|--------------------------------|----------------------------------|
| <span data-ttu-id="c66e1-126">0</span><span class="sxs-lookup"><span data-stu-id="c66e1-126">0</span></span>             | <span data-ttu-id="c66e1-127">\_classe de priorité en temps réel \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-127">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="c66e1-128">temps de priorité des THREADs \_ \_ \_ critique</span><span class="sxs-lookup"><span data-stu-id="c66e1-128">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="c66e1-129">1</span><span class="sxs-lookup"><span data-stu-id="c66e1-129">1</span></span>             | <span data-ttu-id="c66e1-130">\_classe de priorité élevée \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-130">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="c66e1-131">priorité de THREAD la \_ \_ plus élevée</span><span class="sxs-lookup"><span data-stu-id="c66e1-131">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="c66e1-132">2</span><span class="sxs-lookup"><span data-stu-id="c66e1-132">2</span></span>             | <span data-ttu-id="c66e1-133">classe de priorité supérieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-133">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="c66e1-134">priorité de THREAD supérieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="c66e1-134">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="c66e1-135">3</span><span class="sxs-lookup"><span data-stu-id="c66e1-135">3</span></span>             | <span data-ttu-id="c66e1-136">classe de priorité supérieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-136">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="c66e1-137">priorité de THREAD supérieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="c66e1-137">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="c66e1-138">4</span><span class="sxs-lookup"><span data-stu-id="c66e1-138">4</span></span>             | <span data-ttu-id="c66e1-139">\_classe de priorité normale \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-139">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="c66e1-140">priorité de THREAD \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="c66e1-140">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="c66e1-141">5</span><span class="sxs-lookup"><span data-stu-id="c66e1-141">5</span></span>             | <span data-ttu-id="c66e1-142">\_classe de priorité normale \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-142">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="c66e1-143">priorité de THREAD \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="c66e1-143">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="c66e1-144">6</span><span class="sxs-lookup"><span data-stu-id="c66e1-144">6</span></span>             | <span data-ttu-id="c66e1-145">\_classe de priorité normale \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-145">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="c66e1-146">priorité de THREAD \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="c66e1-146">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="c66e1-147">7</span><span class="sxs-lookup"><span data-stu-id="c66e1-147">7</span></span>             | <span data-ttu-id="c66e1-148">classe de priorité inférieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-148">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="c66e1-149">priorité de THREAD inférieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="c66e1-149">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="c66e1-150">8</span><span class="sxs-lookup"><span data-stu-id="c66e1-150">8</span></span>             | <span data-ttu-id="c66e1-151">classe de priorité inférieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-151">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="c66e1-152">priorité de THREAD inférieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="c66e1-152">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="c66e1-153">9</span><span class="sxs-lookup"><span data-stu-id="c66e1-153">9</span></span>             | <span data-ttu-id="c66e1-154">\_classe de priorité Idle \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-154">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="c66e1-155">priorité de THREAD la \_ \_ plus basse</span><span class="sxs-lookup"><span data-stu-id="c66e1-155">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="c66e1-156">10</span><span class="sxs-lookup"><span data-stu-id="c66e1-156">10</span></span>            | <span data-ttu-id="c66e1-157">\_classe de priorité Idle \_</span><span class="sxs-lookup"><span data-stu-id="c66e1-157">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="c66e1-158">priorité de THREAD \_ \_ inactive</span><span class="sxs-lookup"><span data-stu-id="c66e1-158">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="c66e1-159">Pour le développement C++, consultez la [**propriété Priority de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span><span class="sxs-lookup"><span data-stu-id="c66e1-159">For C++ development, see [**Priority Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).</span></span>

<span data-ttu-id="c66e1-160">Pour le développement de scripts, consultez [**TaskSettings. Priority**](tasksettings-priority.md).</span><span class="sxs-lookup"><span data-stu-id="c66e1-160">For script development, see [**TaskSettings.Priority**](tasksettings-priority.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c66e1-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c66e1-161">Requirements</span></span>



| <span data-ttu-id="c66e1-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c66e1-162">Requirement</span></span> | <span data-ttu-id="c66e1-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="c66e1-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c66e1-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c66e1-164">Minimum supported client</span></span><br/> | <span data-ttu-id="c66e1-165">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c66e1-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c66e1-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c66e1-166">Minimum supported server</span></span><br/> | <span data-ttu-id="c66e1-167">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c66e1-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c66e1-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c66e1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c66e1-169">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c66e1-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

