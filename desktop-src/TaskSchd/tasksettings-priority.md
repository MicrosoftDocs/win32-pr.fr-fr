---
title: TaskSettings. Priority (propriété)
description: Pour les scripts, obtient ou définit le niveau de priorité de la tâche.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Planificateur de tâches de la propriété Priority
- Propriété Priority Planificateur de tâches, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941763"
---
# <a name="tasksettingspriority-property"></a><span data-ttu-id="6d1fa-106">TaskSettings. Priority (propriété)</span><span class="sxs-lookup"><span data-stu-id="6d1fa-106">TaskSettings.Priority property</span></span>

<span data-ttu-id="6d1fa-107">Pour les scripts, obtient ou définit le niveau de priorité de la tâche.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-107">For scripting, gets or sets the priority level of the task.</span></span>

<span data-ttu-id="6d1fa-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d1fa-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d1fa-109">Syntax</span></span>


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a><span data-ttu-id="6d1fa-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6d1fa-110">Property value</span></span>

<span data-ttu-id="6d1fa-111">Niveau de priorité (0-10) de la tâche.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-111">The priority level (0-10) of the task.</span></span> <span data-ttu-id="6d1fa-112">La valeur par défaut est 7.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-112">The default is 7.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d1fa-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6d1fa-113">Remarks</span></span>

<span data-ttu-id="6d1fa-114">Le niveau de priorité 0 est la priorité la plus élevée et le niveau de priorité 10 est la priorité la plus basse.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-114">Priority level 0 is the highest priority, and priority level 10 is the lowest priority.</span></span> <span data-ttu-id="6d1fa-115">La valeur par défaut est 7.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-115">The default value is 7.</span></span> <span data-ttu-id="6d1fa-116">Les niveaux de priorité 7 et 8 sont utilisés pour les tâches en arrière-plan, et les niveaux de priorité 4, 5 et 6 sont utilisés pour les tâches interactives.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-116">Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.</span></span>

<span data-ttu-id="6d1fa-117">L’action de la tâche est démarrée dans un processus avec une priorité basée sur une valeur de classe de priorité.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-117">The task's action is started in a process with a priority that is based on a Priority Class value.</span></span> <span data-ttu-id="6d1fa-118">Une valeur de niveau de priorité (priorité de thread) est utilisée pour les actions de la tâche du gestionnaire COM, de la boîte de message et de l’e-mail.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-118">A Priority Level value (thread priority) is used for COM handler, message box, and email task actions.</span></span> <span data-ttu-id="6d1fa-119">Pour plus d’informations sur la classe de priorité et les valeurs de niveau de priorité, consultez [planification des priorités](/windows/desktop/ProcThread/scheduling-priorities).</span><span class="sxs-lookup"><span data-stu-id="6d1fa-119">For more information about the Priority Class and Priority Level values, see [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities).</span></span> <span data-ttu-id="6d1fa-120">Le tableau suivant répertorie les valeurs possibles pour le paramètre *Priority* et les valeurs de classe de priorité et de niveau de priorité correspondantes.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-120">The following table lists the possible values for the *priority* parameter, and the corresponding Priority Class and Priority Level values.</span></span>



| <span data-ttu-id="6d1fa-121">*Priorité* de la tâche</span><span class="sxs-lookup"><span data-stu-id="6d1fa-121">Task *priority*</span></span> | <span data-ttu-id="6d1fa-122">Classe de priorité</span><span class="sxs-lookup"><span data-stu-id="6d1fa-122">Priority Class</span></span>                 | <span data-ttu-id="6d1fa-123">Niveau de priorité</span><span class="sxs-lookup"><span data-stu-id="6d1fa-123">Priority Level</span></span>                   |
|-----------------|--------------------------------|----------------------------------|
| <span data-ttu-id="6d1fa-124">0</span><span class="sxs-lookup"><span data-stu-id="6d1fa-124">0</span></span>               | <span data-ttu-id="6d1fa-125">\_classe de priorité en temps réel \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-125">REALTIME\_PRIORITY\_CLASS</span></span>      | <span data-ttu-id="6d1fa-126">temps de priorité des THREADs \_ \_ \_ critique</span><span class="sxs-lookup"><span data-stu-id="6d1fa-126">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span> |
| <span data-ttu-id="6d1fa-127">1</span><span class="sxs-lookup"><span data-stu-id="6d1fa-127">1</span></span>               | <span data-ttu-id="6d1fa-128">\_classe de priorité élevée \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-128">HIGH\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="6d1fa-129">priorité de THREAD la \_ \_ plus élevée</span><span class="sxs-lookup"><span data-stu-id="6d1fa-129">THREAD\_PRIORITY\_HIGHEST</span></span>        |
| <span data-ttu-id="6d1fa-130">2</span><span class="sxs-lookup"><span data-stu-id="6d1fa-130">2</span></span>               | <span data-ttu-id="6d1fa-131">classe de priorité supérieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-131">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="6d1fa-132">priorité de THREAD supérieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="6d1fa-132">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="6d1fa-133">3</span><span class="sxs-lookup"><span data-stu-id="6d1fa-133">3</span></span>               | <span data-ttu-id="6d1fa-134">classe de priorité supérieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-134">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="6d1fa-135">priorité de THREAD supérieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="6d1fa-135">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  |
| <span data-ttu-id="6d1fa-136">4</span><span class="sxs-lookup"><span data-stu-id="6d1fa-136">4</span></span>               | <span data-ttu-id="6d1fa-137">\_classe de priorité normale \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-137">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="6d1fa-138">priorité de THREAD \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="6d1fa-138">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="6d1fa-139">5</span><span class="sxs-lookup"><span data-stu-id="6d1fa-139">5</span></span>               | <span data-ttu-id="6d1fa-140">\_classe de priorité normale \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-140">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="6d1fa-141">priorité de THREAD \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="6d1fa-141">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="6d1fa-142">6</span><span class="sxs-lookup"><span data-stu-id="6d1fa-142">6</span></span>               | <span data-ttu-id="6d1fa-143">\_classe de priorité normale \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-143">NORMAL\_PRIORITY\_CLASS</span></span>        | <span data-ttu-id="6d1fa-144">priorité de THREAD \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="6d1fa-144">THREAD\_PRIORITY\_NORMAL</span></span>         |
| <span data-ttu-id="6d1fa-145">7</span><span class="sxs-lookup"><span data-stu-id="6d1fa-145">7</span></span>               | <span data-ttu-id="6d1fa-146">classe de priorité inférieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-146">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="6d1fa-147">priorité de THREAD inférieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="6d1fa-147">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="6d1fa-148">8</span><span class="sxs-lookup"><span data-stu-id="6d1fa-148">8</span></span>               | <span data-ttu-id="6d1fa-149">classe de priorité inférieure à la \_ normale \_ \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-149">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span> | <span data-ttu-id="6d1fa-150">priorité de THREAD inférieure à la \_ \_ \_ normale</span><span class="sxs-lookup"><span data-stu-id="6d1fa-150">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  |
| <span data-ttu-id="6d1fa-151">9</span><span class="sxs-lookup"><span data-stu-id="6d1fa-151">9</span></span>               | <span data-ttu-id="6d1fa-152">\_classe de priorité Idle \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-152">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="6d1fa-153">priorité de THREAD la \_ \_ plus basse</span><span class="sxs-lookup"><span data-stu-id="6d1fa-153">THREAD\_PRIORITY\_LOWEST</span></span>         |
| <span data-ttu-id="6d1fa-154">10</span><span class="sxs-lookup"><span data-stu-id="6d1fa-154">10</span></span>              | <span data-ttu-id="6d1fa-155">\_classe de priorité Idle \_</span><span class="sxs-lookup"><span data-stu-id="6d1fa-155">IDLE\_PRIORITY\_CLASS</span></span>          | <span data-ttu-id="6d1fa-156">priorité de THREAD \_ \_ inactive</span><span class="sxs-lookup"><span data-stu-id="6d1fa-156">THREAD\_PRIORITY\_IDLE</span></span>           |



 

<span data-ttu-id="6d1fa-157">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="6d1fa-157">When reading or writing XML for a task, this setting is specified in the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d1fa-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d1fa-158">Requirements</span></span>



| <span data-ttu-id="6d1fa-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d1fa-159">Requirement</span></span> | <span data-ttu-id="6d1fa-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d1fa-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d1fa-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d1fa-161">Minimum supported client</span></span><br/> | <span data-ttu-id="6d1fa-162">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d1fa-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6d1fa-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d1fa-163">Minimum supported server</span></span><br/> | <span data-ttu-id="6d1fa-164">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d1fa-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d1fa-165">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6d1fa-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d1fa-166"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6d1fa-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6d1fa-167">DLL</span><span class="sxs-lookup"><span data-stu-id="6d1fa-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d1fa-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d1fa-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d1fa-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d1fa-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d1fa-170">**TaskSettings**</span><span class="sxs-lookup"><span data-stu-id="6d1fa-170">**TaskSettings**</span></span>](tasksettings.md)
</dt> </dl>

 

