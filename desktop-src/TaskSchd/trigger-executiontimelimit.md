---
title: Trigger.Exepropriété cutionTimeLimit
description: Pour les scripts, obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Planificateur de tâches de la propriété ExecutionTimeLimit
- Propriété ExecutionTimeLimit Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet de déclencheur, propriété ExecutionTimeLimit
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941887"
---
# <a name="triggerexecutiontimelimit-property"></a><span data-ttu-id="cfbd2-106">Trigger.Exepropriété cutionTimeLimit</span><span class="sxs-lookup"><span data-stu-id="cfbd2-106">Trigger.ExecutionTimeLimit property</span></span>

<span data-ttu-id="cfbd2-107">Pour les scripts, obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="cfbd2-107">For scripting, gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfbd2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfbd2-108">Syntax</span></span>


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="cfbd2-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cfbd2-109">Property value</span></span>

<span data-ttu-id="cfbd2-110">Durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="cfbd2-110">The maximum amount of time that the task launched by the trigger is allowed to run.</span></span> <span data-ttu-id="cfbd2-111">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="cfbd2-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbd2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="cfbd2-112">Remarks</span></span>

<span data-ttu-id="cfbd2-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, la limite de temps d’exécution est spécifiée dans l’élément [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="cfbd2-113">When reading or writing XML for a task, the execution time limit is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbd2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfbd2-114">Requirements</span></span>



| <span data-ttu-id="cfbd2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfbd2-115">Requirement</span></span> | <span data-ttu-id="cfbd2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfbd2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbd2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfbd2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbd2-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfbd2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cfbd2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfbd2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbd2-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfbd2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cfbd2-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cfbd2-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="cfbd2-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cfbd2-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cfbd2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cfbd2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfbd2-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfbd2-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbd2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfbd2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbd2-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="cfbd2-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





