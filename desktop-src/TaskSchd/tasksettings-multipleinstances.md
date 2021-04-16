---
title: TaskSettings. MultipleInstances, propriété
description: Pour les scripts, obtient ou définit la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Planificateur de tâches de la propriété MultipleInstances
- Planificateur de tâches de la propriété MultipleInstances, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété MultipleInstances
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508369"
---
# <a name="tasksettingsmultipleinstances-property"></a><span data-ttu-id="30d35-106">TaskSettings. MultipleInstances, propriété</span><span class="sxs-lookup"><span data-stu-id="30d35-106">TaskSettings.MultipleInstances property</span></span>

<span data-ttu-id="30d35-107">Pour les scripts, obtient ou définit la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.</span><span class="sxs-lookup"><span data-stu-id="30d35-107">For scripting, gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

<span data-ttu-id="30d35-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="30d35-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d35-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30d35-109">Syntax</span></span>


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a><span data-ttu-id="30d35-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="30d35-110">Property value</span></span>

<span data-ttu-id="30d35-111">[**Tâche \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) Constantes de stratégie d’instances.</span><span class="sxs-lookup"><span data-stu-id="30d35-111">[**TASK\_INSTANCES\_POLICY**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) constants.</span></span>



| <span data-ttu-id="30d35-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="30d35-112">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="30d35-113">Signification</span><span class="sxs-lookup"><span data-stu-id="30d35-113">Meaning</span></span>                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <span data-ttu-id="30d35-114"><dt>**Tâche \_ INSTANCES \_ parallèles**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30d35-114"><dt>**TASK\_INSTANCES\_PARALLEL**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="30d35-115">Démarre une nouvelle instance lorsqu’une instance existante de la tâche est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="30d35-115">Starts a new instance while an existing instance of the task is running.</span></span><br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <span data-ttu-id="30d35-116"><dt>**Tâche \_ INSTANCES, \_ file d’attente**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="30d35-116"><dt>**TASK\_INSTANCES\_QUEUE**</dt> <dt>1</dt></span></span> </dl>                          | <span data-ttu-id="30d35-117">Démarre une nouvelle instance de la tâche une fois que toutes les autres instances de la tâche sont terminées.</span><span class="sxs-lookup"><span data-stu-id="30d35-117">Starts a new instance of the task after all other instances of the task are complete.</span></span><br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <span data-ttu-id="30d35-118"><dt>**Tâche \_ Les INSTANCES \_ ignorent les \_ nouvelles**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="30d35-118"><dt>**TASK\_INSTANCES\_IGNORE\_NEW**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="30d35-119">Ne démarre pas une nouvelle instance si une instance existante de la tâche est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="30d35-119">Does not start a new instance if an existing instance of the task is running.</span></span><br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <span data-ttu-id="30d35-120"><dt>**Tâche \_ Arrêter les INSTANCES \_ \_ existantes**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="30d35-120"><dt>**TASK\_INSTANCES\_STOP\_EXISTING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="30d35-121">Arrête une instance existante de la tâche avant de démarrer une nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="30d35-121">Stops an existing instance of the task before it starts new instance.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="30d35-122">Notes</span><span class="sxs-lookup"><span data-stu-id="30d35-122">Remarks</span></span>

<span data-ttu-id="30d35-123">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="30d35-123">When reading or writing XML for a task, this setting is specified in the [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="30d35-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30d35-124">Requirements</span></span>



| <span data-ttu-id="30d35-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30d35-125">Requirement</span></span> | <span data-ttu-id="30d35-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="30d35-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30d35-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30d35-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30d35-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30d35-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="30d35-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30d35-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30d35-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30d35-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30d35-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="30d35-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="30d35-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30d35-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30d35-133">DLL</span><span class="sxs-lookup"><span data-stu-id="30d35-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30d35-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30d35-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30d35-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30d35-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30d35-136">**\_stratégie d’instances de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="30d35-136">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[<span data-ttu-id="30d35-137">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="30d35-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





