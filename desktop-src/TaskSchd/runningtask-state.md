---
title: RunningTask. State, propriété
description: Pour les scripts, obtient un identificateur pour l’état de la tâche en cours d’exécution.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Planificateur de tâches de propriété d’État
- Propriété State Planificateur de tâches, objet RunningTask
- Objet RunningTask Planificateur de tâches, propriété State
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740853"
---
# <a name="runningtaskstate-property"></a><span data-ttu-id="d2f74-106">RunningTask. State, propriété</span><span class="sxs-lookup"><span data-stu-id="d2f74-106">RunningTask.State property</span></span>

<span data-ttu-id="d2f74-107">Pour les scripts, obtient un identificateur pour l’état de la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2f74-107">For scripting, gets an identifier for the state of the running task.</span></span>

<span data-ttu-id="d2f74-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d2f74-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f74-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2f74-109">Syntax</span></span>


```VB
RunningTask.State As String
```



## <a name="property-value"></a><span data-ttu-id="d2f74-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d2f74-110">Property value</span></span>

<span data-ttu-id="d2f74-111">Identificateur de l’état de la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2f74-111">An identifier for the state of the running task.</span></span>



| <span data-ttu-id="d2f74-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f74-112">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="d2f74-113">Signification</span><span class="sxs-lookup"><span data-stu-id="d2f74-113">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="d2f74-114"><dt>**Tâche \_ ÉTAT \_ inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2f74-114"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="d2f74-115">L’état de la tâche est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d2f74-115">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="d2f74-116"><dt>**Tâche \_ ÉTAT \_ désactivé**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d2f74-116"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="d2f74-117">La tâche est inscrite, mais elle est désactivée et aucune instance de la tâche n’est mise en file d’attente ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2f74-117">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="d2f74-118">La tâche ne peut pas être exécutée tant qu’elle n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="d2f74-118">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="d2f74-119"><dt>**Tâche \_ État en \_ file d’attente**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2f74-119"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="d2f74-120">Les instances de la tâche sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="d2f74-120">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="d2f74-121"><dt>**Tâche \_ ÉTAT \_ prêt**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2f74-121"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="d2f74-122">La tâche est prête à être exécutée, mais aucune instance n’est en file d’attente ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2f74-122">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="d2f74-123"><dt>**Tâche \_ ÉTAT \_ en cours d’exécution**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d2f74-123"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="d2f74-124">Une ou plusieurs instances de la tâche sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2f74-124">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="d2f74-125">Notes</span><span class="sxs-lookup"><span data-stu-id="d2f74-125">Remarks</span></span>

<span data-ttu-id="d2f74-126">La méthode [**RunningTask. Refresh**](runningtask-refresh.md) est appelée avant que la valeur de la propriété ne soit retournée.</span><span class="sxs-lookup"><span data-stu-id="d2f74-126">The [**RunningTask.Refresh**](runningtask-refresh.md) method is called before the property value is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f74-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2f74-127">Requirements</span></span>



| <span data-ttu-id="d2f74-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2f74-128">Requirement</span></span> | <span data-ttu-id="d2f74-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2f74-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f74-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2f74-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d2f74-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2f74-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d2f74-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2f74-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d2f74-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2f74-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2f74-134">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d2f74-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2f74-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2f74-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2f74-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d2f74-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2f74-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2f74-137"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





