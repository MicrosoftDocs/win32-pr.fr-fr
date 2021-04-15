---
title: TaskSettings. AllowDemandStart, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Planificateur de tâches de la propriété AllowDemandStart
- Planificateur de tâches de la propriété AllowDemandStart, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété AllowDemandStart
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384091"
---
# <a name="tasksettingsallowdemandstart-property"></a><span data-ttu-id="6c8a7-106">TaskSettings. AllowDemandStart, propriété</span><span class="sxs-lookup"><span data-stu-id="6c8a7-106">TaskSettings.AllowDemandStart property</span></span>

<span data-ttu-id="6c8a7-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-107">For scripting, gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.</span></span>

<span data-ttu-id="6c8a7-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8a7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c8a7-109">Syntax</span></span>


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6c8a7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6c8a7-110">Property value</span></span>

<span data-ttu-id="6c8a7-111">Si la valeur est true, la tâche peut être exécutée à l’aide de la commande exécuter ou du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-111">If True, the task can be run by using the Run command or the Context menu.</span></span> <span data-ttu-id="6c8a7-112">Si la valeur est false, la tâche ne peut pas être exécutée à l’aide de la commande exécuter ou du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-112">If False, the task cannot be run using the Run command or the Context menu.</span></span> <span data-ttu-id="6c8a7-113">La valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-113">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8a7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6c8a7-114">Remarks</span></span>

<span data-ttu-id="6c8a7-115">Lorsque cette propriété a la valeur true, la tâche peut être démarrée indépendamment de la date à laquelle les déclencheurs démarrent la tâche.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-115">When this property is set to True, the task can be started independent of when any triggers start the task.</span></span>

<span data-ttu-id="6c8a7-116">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-116">When reading or writing XML for a task, this setting is specified in the [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8a7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c8a7-117">Requirements</span></span>



| <span data-ttu-id="6c8a7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c8a7-118">Requirement</span></span> | <span data-ttu-id="6c8a7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c8a7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8a7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c8a7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8a7-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c8a7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6c8a7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c8a7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8a7-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c8a7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c8a7-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6c8a7-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c8a7-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6c8a7-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6c8a7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6c8a7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c8a7-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c8a7-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8a7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c8a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8a7-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="6c8a7-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





