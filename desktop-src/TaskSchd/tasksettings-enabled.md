---
title: TaskSettings. Enabled, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche est activée. La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Planificateur de tâches de la propriété Enabled
- Propriété Enabled Planificateur de tâches, objet TaskSettings
- Objet TaskSettings Planificateur de tâches, propriété Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384907"
---
# <a name="tasksettingsenabled-property"></a><span data-ttu-id="4e117-107">TaskSettings. Enabled, propriété</span><span class="sxs-lookup"><span data-stu-id="4e117-107">TaskSettings.Enabled property</span></span>

<span data-ttu-id="4e117-108">Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche est activée.</span><span class="sxs-lookup"><span data-stu-id="4e117-108">For scripting, gets or sets a Boolean value that indicates that the task is enabled.</span></span> <span data-ttu-id="4e117-109">La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="4e117-109">The task can be performed only when this setting is True.</span></span>

<span data-ttu-id="4e117-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4e117-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e117-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e117-111">Syntax</span></span>


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="4e117-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4e117-112">Property value</span></span>

<span data-ttu-id="4e117-113">Si la valeur est true, la tâche est activée.</span><span class="sxs-lookup"><span data-stu-id="4e117-113">If True, the task is enabled.</span></span> <span data-ttu-id="4e117-114">Si la valeur est false, la tâche n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="4e117-114">If False, the task is not enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e117-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4e117-115">Remarks</span></span>

<span data-ttu-id="4e117-116">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="4e117-116">When reading or writing XML for a task, this setting is specified in the [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e117-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e117-117">Requirements</span></span>



| <span data-ttu-id="4e117-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e117-118">Requirement</span></span> | <span data-ttu-id="4e117-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e117-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e117-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e117-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e117-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e117-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4e117-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e117-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e117-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e117-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e117-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4e117-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e117-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4e117-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4e117-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4e117-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e117-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e117-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e117-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e117-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e117-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4e117-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





