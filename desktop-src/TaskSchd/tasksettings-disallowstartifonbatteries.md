---
title: TaskSettings. DisallowStartIfOnBatteries, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Planificateur de tâches de la propriété DisallowStartIfOnBatteries
- Planificateur de tâches de la propriété DisallowStartIfOnBatteries, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105346"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a><span data-ttu-id="373e4-106">TaskSettings. DisallowStartIfOnBatteries, propriété</span><span class="sxs-lookup"><span data-stu-id="373e4-106">TaskSettings.DisallowStartIfOnBatteries property</span></span>

<span data-ttu-id="373e4-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.</span><span class="sxs-lookup"><span data-stu-id="373e4-107">For scripting, gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span>

<span data-ttu-id="373e4-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="373e4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="373e4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="373e4-109">Syntax</span></span>


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="373e4-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="373e4-110">Property value</span></span>

<span data-ttu-id="373e4-111">Valeur booléenne qui indique que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.</span><span class="sxs-lookup"><span data-stu-id="373e4-111">A Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="373e4-112">Si la valeur est true, la tâche n’est pas démarrée si l’ordinateur fonctionne sur batterie.</span><span class="sxs-lookup"><span data-stu-id="373e4-112">If True, the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="373e4-113">Si la valeur est false, la tâche est démarrée si l’ordinateur fonctionne sur batterie.</span><span class="sxs-lookup"><span data-stu-id="373e4-113">If False, the task will be started if the computer is running on batteries.</span></span> <span data-ttu-id="373e4-114">La valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="373e4-114">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="373e4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="373e4-115">Remarks</span></span>

<span data-ttu-id="373e4-116">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="373e4-116">When reading or writing XML for a task, this setting is specified in the [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="373e4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="373e4-117">Requirements</span></span>



| <span data-ttu-id="373e4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="373e4-118">Requirement</span></span> | <span data-ttu-id="373e4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="373e4-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="373e4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="373e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="373e4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="373e4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="373e4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="373e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="373e4-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="373e4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="373e4-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="373e4-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="373e4-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="373e4-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="373e4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="373e4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="373e4-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="373e4-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="373e4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="373e4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="373e4-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="373e4-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





