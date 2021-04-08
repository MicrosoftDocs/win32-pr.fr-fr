---
title: IdleSettings. StopOnIdleEnd, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met fin à la tâche si la condition d’inactivité se termine avant la fin de la tâche.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Planificateur de tâches de la propriété StopOnIdleEnd
- Planificateur de tâches de la propriété StopOnIdleEnd, objet IdleSettings
- Planificateur de tâches objet IdleSettings, propriété StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843265"
---
# <a name="idlesettingsstoponidleend-property"></a><span data-ttu-id="dc759-106">IdleSettings. StopOnIdleEnd, propriété</span><span class="sxs-lookup"><span data-stu-id="dc759-106">IdleSettings.StopOnIdleEnd property</span></span>

<span data-ttu-id="dc759-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met fin à la tâche si la condition d’inactivité se termine avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="dc759-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc759-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc759-108">Syntax</span></span>


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="dc759-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dc759-109">Property value</span></span>

<span data-ttu-id="dc759-110">Valeur booléenne qui indique que la Planificateur de tâches met fin à la tâche si la condition d’inactivité se termine avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="dc759-110">A Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc759-111">Notes</span><span class="sxs-lookup"><span data-stu-id="dc759-111">Remarks</span></span>

<span data-ttu-id="dc759-112">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="dc759-112">When reading or writing XML for a task, this setting is specified in the [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc759-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc759-113">Requirements</span></span>



| <span data-ttu-id="dc759-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc759-114">Requirement</span></span> | <span data-ttu-id="dc759-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc759-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc759-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc759-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dc759-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc759-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dc759-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc759-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dc759-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc759-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc759-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dc759-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc759-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc759-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc759-122">DLL</span><span class="sxs-lookup"><span data-stu-id="dc759-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc759-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc759-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc759-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc759-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc759-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="dc759-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="dc759-126">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="dc759-126">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





