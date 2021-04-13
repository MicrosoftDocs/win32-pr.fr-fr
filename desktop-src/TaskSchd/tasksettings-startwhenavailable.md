---
title: TaskSettings. StartWhenAvailable, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la Planificateur de tâches peut démarrer la tâche à tout moment une fois que l’heure planifiée est passée.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Planificateur de tâches de la propriété StartWhenAvailable
- Planificateur de tâches de la propriété StartWhenAvailable, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466406"
---
# <a name="tasksettingsstartwhenavailable-property"></a><span data-ttu-id="26b80-106">TaskSettings. StartWhenAvailable, propriété</span><span class="sxs-lookup"><span data-stu-id="26b80-106">TaskSettings.StartWhenAvailable property</span></span>

<span data-ttu-id="26b80-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que la Planificateur de tâches peut démarrer la tâche à tout moment une fois que l’heure planifiée est passée.</span><span class="sxs-lookup"><span data-stu-id="26b80-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

<span data-ttu-id="26b80-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="26b80-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b80-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26b80-109">Syntax</span></span>


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="26b80-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="26b80-110">Property value</span></span>

<span data-ttu-id="26b80-111">Si la valeur est true, la propriété indique que la Planificateur de tâches peut démarrer la tâche à tout moment une fois que l’heure planifiée est passée.</span><span class="sxs-lookup"><span data-stu-id="26b80-111">If True, the property indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span> <span data-ttu-id="26b80-112">La valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="26b80-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b80-113">Notes</span><span class="sxs-lookup"><span data-stu-id="26b80-113">Remarks</span></span>

<span data-ttu-id="26b80-114">Cette propriété s’applique uniquement aux tâches basées sur le temps avec une limite de fin ou des tâches basées sur le temps qui sont configurées pour se répéter de manière infinie.</span><span class="sxs-lookup"><span data-stu-id="26b80-114">This property applies only to time-based tasks with an end boundary or time-based tasks that are set to repeat infinitely.</span></span>

<span data-ttu-id="26b80-115">Les tâches qui sont démarrées après l’heure planifiée sont passées (en raison de la propriété [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) définie sur true) sont mises en file d’attente dans la file d’attente de tâches du service Planificateur de tâches et elles sont démarrées après un certain délai.</span><span class="sxs-lookup"><span data-stu-id="26b80-115">Tasks that are started after the scheduled time has passed (because of the [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) property being set to True) are queued in the Task Scheduler service's queue of tasks and they are started after a delay.</span></span> <span data-ttu-id="26b80-116">Le délai par défaut est de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="26b80-116">The default delay is 10 minutes.</span></span>

<span data-ttu-id="26b80-117">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="26b80-117">When reading or writing XML for a task, this setting is specified in the [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b80-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26b80-118">Requirements</span></span>



| <span data-ttu-id="26b80-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26b80-119">Requirement</span></span> | <span data-ttu-id="26b80-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="26b80-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26b80-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26b80-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26b80-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26b80-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="26b80-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26b80-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26b80-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26b80-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26b80-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="26b80-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="26b80-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26b80-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26b80-127">DLL</span><span class="sxs-lookup"><span data-stu-id="26b80-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26b80-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26b80-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b80-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26b80-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b80-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="26b80-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





