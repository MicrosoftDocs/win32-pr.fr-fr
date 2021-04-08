---
title: Méthode TaskService. GetRunningTasks
description: Pour les scripts, obtient une collection de tâches en cours d’exécution.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Planificateur de tâches de la méthode GetRunningTasks
- Méthode GetRunningTasks Planificateur de tâches, objet TaskService
- Planificateur de tâches objet TaskService, méthode GetRunningTasks
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743740"
---
# <a name="taskservicegetrunningtasks-method"></a><span data-ttu-id="14238-106">Méthode TaskService. GetRunningTasks</span><span class="sxs-lookup"><span data-stu-id="14238-106">TaskService.GetRunningTasks method</span></span>

<span data-ttu-id="14238-107">Pour les scripts, obtient une collection de tâches en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="14238-107">For scripting, gets a collection of running tasks.</span></span>

> [!Note]  
> <span data-ttu-id="14238-108">**TaskService. GetRunningTasks** retourne uniquement une collection de tâches en cours d’exécution qui s’exécutent au-dessous ou au-dessous du contexte de sécurité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14238-108">**TaskService.GetRunningTasks** will only return a collection of running tasks that are running at or below a user's security context.</span></span> <span data-ttu-id="14238-109">Par exemple, pour les membres du groupe administrateurs, **GetRunningTasks** retourne une collection de toutes les tâches en cours d’exécution, mais pour les membres du groupe utilisateurs, **GetRunningTasks** renvoie uniquement une collection de tâches qui s’exécutent dans le contexte de sécurité du groupe utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="14238-109">For example, for members of the Administrators group, **GetRunningTasks** will return a collection of all running tasks, but for members of the Users group, **GetRunningTasks** will only return a collection of tasks that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="14238-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14238-110">Syntax</span></span>


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="14238-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14238-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14238-112">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14238-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14238-113">Transmettez 1 pour retourner toutes les tâches en cours d’exécution, y compris les tâches masquées.</span><span class="sxs-lookup"><span data-stu-id="14238-113">Pass in 1 to return all running tasks, including hidden tasks.</span></span> <span data-ttu-id="14238-114">Transmettez 0 pour retourner une collection de tâches en cours d’exécution qui ne sont pas des tâches masquées.</span><span class="sxs-lookup"><span data-stu-id="14238-114">Pass in 0 to return a collection of running tasks that are not hidden tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14238-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14238-115">Return value</span></span>

<span data-ttu-id="14238-116">Objet [**RunningTaskCollection**](runningtaskcollection.md) qui contient les tâches en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="14238-116">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains the currently running tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="14238-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14238-117">Requirements</span></span>



| <span data-ttu-id="14238-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14238-118">Requirement</span></span> | <span data-ttu-id="14238-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="14238-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14238-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14238-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14238-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14238-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="14238-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14238-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14238-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14238-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14238-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="14238-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="14238-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="14238-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="14238-126">DLL</span><span class="sxs-lookup"><span data-stu-id="14238-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14238-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14238-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14238-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14238-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14238-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="14238-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





