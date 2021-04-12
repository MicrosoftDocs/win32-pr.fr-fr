---
title: Méthode RegisteredTask. GetInstances
description: Pour les scripts, retourne toutes les instances en cours d’exécution de la tâche inscrite.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Planificateur de tâches de la méthode GetInstances
- Méthode GetInstances Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode GetInstances
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105244"
---
# <a name="registeredtaskgetinstances-method"></a><span data-ttu-id="0e5c4-106">Méthode RegisteredTask. GetInstances</span><span class="sxs-lookup"><span data-stu-id="0e5c4-106">RegisteredTask.GetInstances method</span></span>

<span data-ttu-id="0e5c4-107">Pour les scripts, retourne toutes les instances en cours d’exécution de la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-107">For scripting, returns all currently running instances of the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="0e5c4-108">**RegisteredTask. GetInstances** retourne uniquement les instances de la tâche inscrite en cours d’exécution qui s’exécutent au-dessous ou au-dessous du contexte de sécurité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-108">**RegisteredTask.GetInstances** will only return instances of the currently running registered task that are running at or below a user's security context.</span></span> <span data-ttu-id="0e5c4-109">Par exemple, pour les membres du groupe administrateurs, **GetInstances** retourne toutes les instances de la tâche inscrite en cours d’exécution, mais pour les membres du groupe utilisateurs, **GetInstances** renvoie uniquement les instances de la tâche inscrite en cours d’exécution qui s’exécutent dans le contexte de sécurité du groupe utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-109">For example, for members of the Administrators group, **GetInstances** will return all instances of the currently running registered task, but for members of the Users group, **GetInstances** will only return instances of the currently running registered task that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0e5c4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e5c4-110">Syntax</span></span>


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a><span data-ttu-id="0e5c4-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e5c4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e5c4-112">*flags*</span><span class="sxs-lookup"><span data-stu-id="0e5c4-112">*flags*</span></span> 
</dt> <dd>

<span data-ttu-id="0e5c4-113">Ce paramètre est réservé pour une utilisation ultérieure et doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-113">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="0e5c4-114">*runningTasks* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0e5c4-114">*runningTasks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e5c4-115">Objet [**RunningTaskCollection**](runningtaskcollection.md) qui contient toutes les instances en cours d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-115">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains all currently running instances of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e5c4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e5c4-116">Return value</span></span>

<span data-ttu-id="0e5c4-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0e5c4-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e5c4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e5c4-118">Requirements</span></span>



| <span data-ttu-id="0e5c4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e5c4-119">Requirement</span></span> | <span data-ttu-id="0e5c4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e5c4-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e5c4-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e5c4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e5c4-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e5c4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e5c4-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e5c4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e5c4-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e5c4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e5c4-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0e5c4-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e5c4-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e5c4-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e5c4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0e5c4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e5c4-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e5c4-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e5c4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e5c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e5c4-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0e5c4-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0e5c4-131">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="0e5c4-131">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





