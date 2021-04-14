---
title: Méthode RegisteredTask. GetRunTimes
description: Pour les scripts, obtient le nombre de fois que la tâche inscrite est planifiée pour s’exécuter pendant une période spécifiée.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Planificateur de tâches de la méthode GetRunTimes
- Méthode GetRunTimes Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode GetRunTimes
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509058"
---
# <a name="registeredtaskgetruntimes-method"></a><span data-ttu-id="2fcdc-106">Méthode RegisteredTask. GetRunTimes</span><span class="sxs-lookup"><span data-stu-id="2fcdc-106">RegisteredTask.GetRunTimes method</span></span>

<span data-ttu-id="2fcdc-107">Pour les scripts, obtient le nombre de fois que la tâche inscrite est planifiée pour s’exécuter pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2fcdc-107">For scripting, gets the times that the registered task is scheduled to run during a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcdc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fcdc-108">Syntax</span></span>


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a><span data-ttu-id="2fcdc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fcdc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fcdc-110">*commencer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fcdc-110">*begin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcdc-111">Heure de début de la requête.</span><span class="sxs-lookup"><span data-stu-id="2fcdc-111">The starting time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="2fcdc-112">*fin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fcdc-112">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcdc-113">Heure de fin de la requête.</span><span class="sxs-lookup"><span data-stu-id="2fcdc-113">The ending time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="2fcdc-114">*nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2fcdc-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcdc-115">Nombre de fois que la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="2fcdc-115">The number of scheduled times the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="2fcdc-116">*rgstTaskTimes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2fcdc-116">*rgstTaskTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fcdc-117">Heures planifiées d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="2fcdc-117">The scheduled times that the task will run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fcdc-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fcdc-118">Return value</span></span>

<span data-ttu-id="2fcdc-119">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2fcdc-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fcdc-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2fcdc-120">Remarks</span></span>

<span data-ttu-id="2fcdc-121">Si la tâche inscrite contient des déclencheurs qui sont désactivés individuellement, ces déclencheurs affectent toujours la prochaine exécution planifiée retournée même si elles sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="2fcdc-121">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fcdc-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fcdc-122">Requirements</span></span>



| <span data-ttu-id="2fcdc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fcdc-123">Requirement</span></span> | <span data-ttu-id="2fcdc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fcdc-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcdc-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fcdc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2fcdc-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fcdc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2fcdc-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fcdc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2fcdc-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fcdc-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2fcdc-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2fcdc-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="2fcdc-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2fcdc-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2fcdc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2fcdc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fcdc-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcdc-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fcdc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fcdc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcdc-134">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="2fcdc-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="2fcdc-135">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="2fcdc-135">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





