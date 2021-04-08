---
title: TaskSettings. Compatibility, propriété
description: Pour les scripts, obtient ou définit une valeur entière qui indique quelle version de Planificateur de tâches une tâche est compatible.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Planificateur de tâches de propriétés de compatibilité
- Planificateur de tâches de propriété de compatibilité, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété de compatibilité
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740813"
---
# <a name="tasksettingscompatibility-property"></a><span data-ttu-id="67347-106">TaskSettings. Compatibility, propriété</span><span class="sxs-lookup"><span data-stu-id="67347-106">TaskSettings.Compatibility property</span></span>

<span data-ttu-id="67347-107">Pour les scripts, obtient ou définit une valeur entière qui indique quelle version de Planificateur de tâches une tâche est compatible.</span><span class="sxs-lookup"><span data-stu-id="67347-107">For scripting, gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.</span></span>

<span data-ttu-id="67347-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="67347-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="67347-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67347-109">Syntax</span></span>


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a><span data-ttu-id="67347-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="67347-110">Property value</span></span>



| <span data-ttu-id="67347-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="67347-111">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="67347-112">Signification</span><span class="sxs-lookup"><span data-stu-id="67347-112">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <span data-ttu-id="67347-113"><dt>**Tâche \_ COMPATIBILITÉ \_ à**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="67347-113"><dt>**TASK\_COMPATIBILITY\_AT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="67347-114">La tâche est compatible avec la commande AT.</span><span class="sxs-lookup"><span data-stu-id="67347-114">The task is compatible with the AT command.</span></span><br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <span data-ttu-id="67347-115"><dt>**Tâche \_ COMPATIBILITÉ \_ v1**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="67347-115"><dt>**TASK\_COMPATIBILITY\_V1**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="67347-116">La tâche est compatible avec Planificateur de tâches 1,0.</span><span class="sxs-lookup"><span data-stu-id="67347-116">The task is compatible with Task Scheduler 1.0.</span></span><br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <span data-ttu-id="67347-117"><dt>**Tâche \_ COMPATIBILITÉ \_ v2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="67347-117"><dt>**TASK\_COMPATIBILITY\_V2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="67347-118">La tâche est compatible avec Planificateur de tâches 2,0.</span><span class="sxs-lookup"><span data-stu-id="67347-118">The task is compatible with Task Scheduler 2.0.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67347-119">Notes</span><span class="sxs-lookup"><span data-stu-id="67347-119">Remarks</span></span>

<span data-ttu-id="67347-120">La compatibilité des tâches, définie par la propriété de [**compatibilité**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , doit uniquement être définie sur \_ compatibilité \_ des tâches v1 si une tâche doit être accessible ou modifiée à partir d’un ordinateur Windows XP, Windows Server 2003 ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="67347-120">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task needs to be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="67347-121">Dans le cas contraire, il est recommandé d’utiliser la compatibilité Planificateur de tâches 2,0, car la tâche aura davantage de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="67347-121">Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.</span></span>

<span data-ttu-id="67347-122">Les tâches compatibles avec la commande AT ne peuvent avoir qu’un seul déclencheur d’heure.</span><span class="sxs-lookup"><span data-stu-id="67347-122">Tasks compatible with the AT command can only have one time trigger.</span></span>

<span data-ttu-id="67347-123">Les tâches compatibles avec Planificateur de tâches 1,0 peuvent uniquement avoir un déclencheur d’heure, un déclencheur de connexion ou un déclencheur de démarrage, et la tâche ne peut avoir qu’une action exécutable.</span><span class="sxs-lookup"><span data-stu-id="67347-123">Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.</span></span>

<span data-ttu-id="67347-124">Pour plus d’informations sur la compatibilité des tâches, consultez [Nouveautés des planificateur de tâches](what-s-new-in-task-scheduler.md) et des [tâches](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="67347-124">For more information about task compatibility, see [What's New in Task Scheduler](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67347-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67347-125">Requirements</span></span>



| <span data-ttu-id="67347-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67347-126">Requirement</span></span> | <span data-ttu-id="67347-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="67347-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67347-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67347-128">Minimum supported client</span></span><br/> | <span data-ttu-id="67347-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67347-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="67347-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67347-130">Minimum supported server</span></span><br/> | <span data-ttu-id="67347-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67347-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67347-132">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="67347-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="67347-133"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="67347-133"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="67347-134">DLL</span><span class="sxs-lookup"><span data-stu-id="67347-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67347-135"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67347-135"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67347-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67347-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67347-137">**compatibilité des tâches \_**</span><span class="sxs-lookup"><span data-stu-id="67347-137">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[<span data-ttu-id="67347-138">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="67347-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





