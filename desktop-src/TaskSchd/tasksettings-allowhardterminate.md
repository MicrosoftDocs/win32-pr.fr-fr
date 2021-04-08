---
title: TaskSettings. AllowHardTerminate, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche peut être terminée par le service Planificateur de tâches à l’aide de TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Planificateur de tâches de la propriété AllowHardTerminate
- Planificateur de tâches de la propriété AllowHardTerminate, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété AllowHardTerminate
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742413"
---
# <a name="tasksettingsallowhardterminate-property"></a><span data-ttu-id="86250-106">TaskSettings. AllowHardTerminate, propriété</span><span class="sxs-lookup"><span data-stu-id="86250-106">TaskSettings.AllowHardTerminate property</span></span>

<span data-ttu-id="86250-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche peut être terminée par le service Planificateur de tâches à l’aide de [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="86250-107">For scripting, gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="86250-108">Le service tente de fermer la tâche en cours d’exécution en envoyant la notification [**WM \_ Close**](../winmsg/wm-close.md) et, si la tâche ne répond pas, la tâche ne se termine que si cette propriété a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="86250-108">The service will try to close the running task by sending the [**WM\_CLOSE**](../winmsg/wm-close.md) notification, and if the task does not respond, the task will be terminated only if this property is set to true.</span></span>

<span data-ttu-id="86250-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="86250-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="86250-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86250-110">Syntax</span></span>


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="86250-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="86250-111">Property value</span></span>

<span data-ttu-id="86250-112">Si la valeur est true, la tâche peut être arrêtée à l’aide de [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="86250-112">If True, the task can be terminated by using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="86250-113">Si la valeur est false, la tâche ne peut pas être arrêtée à l’aide de **TerminateProcess**.</span><span class="sxs-lookup"><span data-stu-id="86250-113">If False, the task cannot be terminated by using **TerminateProcess**.</span></span>

## <a name="remarks"></a><span data-ttu-id="86250-114">Notes</span><span class="sxs-lookup"><span data-stu-id="86250-114">Remarks</span></span>

<span data-ttu-id="86250-115">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="86250-115">When reading or writing XML for a task, this setting is specified in the [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="86250-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86250-116">Requirements</span></span>



| <span data-ttu-id="86250-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86250-117">Requirement</span></span> | <span data-ttu-id="86250-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="86250-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86250-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86250-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86250-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86250-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="86250-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86250-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86250-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86250-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86250-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="86250-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="86250-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86250-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86250-125">DLL</span><span class="sxs-lookup"><span data-stu-id="86250-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86250-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86250-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86250-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86250-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86250-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="86250-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

