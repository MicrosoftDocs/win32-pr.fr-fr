---
title: RegisteredTask. NextRunTime, propriété
description: Pour les scripts, obtient l’heure à laquelle la tâche inscrite est planifiée pour s’exécuter.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Planificateur de tâches de la propriété NextRunTime
- Planificateur de tâches de la propriété NextRunTime, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, propriété NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742780"
---
# <a name="registeredtasknextruntime-property"></a><span data-ttu-id="f7036-106">RegisteredTask. NextRunTime, propriété</span><span class="sxs-lookup"><span data-stu-id="f7036-106">RegisteredTask.NextRunTime property</span></span>

<span data-ttu-id="f7036-107">Pour les scripts, obtient l’heure à laquelle la tâche inscrite est planifiée pour s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="f7036-107">For scripting, gets the time when the registered task is next scheduled to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7036-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7036-108">Syntax</span></span>


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a><span data-ttu-id="f7036-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f7036-109">Property value</span></span>

<span data-ttu-id="f7036-110">Heure de la prochaine planification de l’exécution de la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="f7036-110">The time when the registered task is next scheduled to run.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7036-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f7036-111">Remarks</span></span>

<span data-ttu-id="f7036-112">Si la tâche inscrite contient des déclencheurs qui sont désactivés individuellement, ces déclencheurs affectent toujours la prochaine exécution planifiée retournée même si elles sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="f7036-112">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7036-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7036-113">Requirements</span></span>



| <span data-ttu-id="f7036-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7036-114">Requirement</span></span> | <span data-ttu-id="f7036-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7036-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7036-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7036-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f7036-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7036-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f7036-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7036-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f7036-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7036-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7036-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f7036-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7036-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f7036-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f7036-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f7036-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7036-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7036-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7036-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7036-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7036-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f7036-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f7036-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="f7036-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





