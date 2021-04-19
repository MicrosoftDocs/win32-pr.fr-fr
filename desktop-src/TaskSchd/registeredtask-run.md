---
title: RegisteredTask. Run, méthode
description: Pour les scripts, exécute la tâche inscrite immédiatement.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Planificateur de tâches de la méthode Run
- Méthode Run Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches de l’objet RegisteredTask, méthode Run
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512598"
---
# <a name="registeredtaskrun-method"></a><span data-ttu-id="72711-106">RegisteredTask. Run, méthode</span><span class="sxs-lookup"><span data-stu-id="72711-106">RegisteredTask.Run method</span></span>

<span data-ttu-id="72711-107">Pour les scripts, exécute la tâche inscrite immédiatement.</span><span class="sxs-lookup"><span data-stu-id="72711-107">For scripting, runs the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="72711-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72711-108">Syntax</span></span>


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="72711-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72711-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72711-110">*paramètres* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="72711-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72711-111">Paramètres utilisés comme valeurs dans les actions de tâche.</span><span class="sxs-lookup"><span data-stu-id="72711-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="72711-112">Pour ne pas spécifier de valeurs de paramètre pour les actions de tâche, attribuez la valeur **Nothing** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="72711-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="72711-113">Dans le cas contraire, vous pouvez spécifier une valeur de chaîne unique ou un tableau de valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="72711-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="72711-114">Les valeurs de chaîne que vous spécifiez sont associées à des noms et stockées en tant que paires nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="72711-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="72711-115">Si vous spécifiez une valeur de chaîne unique, arg0 sera le nom affecté à la valeur.</span><span class="sxs-lookup"><span data-stu-id="72711-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="72711-116">La valeur peut être utilisée dans l’action de tâche où la variable $ (arg0) est utilisée dans les propriétés de l’action.</span><span class="sxs-lookup"><span data-stu-id="72711-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="72711-117">Si vous transmettez des valeurs telles que « 0 », « 100 » et « 250 » en tant que tableau de valeurs de chaîne, « 0 » remplace les variables $ (arg0), « 100 » remplace les variables $ (Arg1) et « 250 » remplace les variables $ (Arg2) utilisées dans les propriétés d’action.</span><span class="sxs-lookup"><span data-stu-id="72711-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="72711-118">Vous pouvez spécifier au maximum 32 valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="72711-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="72711-119">Pour plus d’informations et pour obtenir la liste des propriétés d’action qui peuvent utiliser les variables $ (arg0), $ (Arg1),..., $ (Arg32) dans leurs valeurs, consultez [actions de tâche](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="72711-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="72711-120">*ppRunningTask* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="72711-120">*ppRunningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72711-121">Objet [**RunningTask**](runningtask.md) qui définit la nouvelle instance de la tâche.</span><span class="sxs-lookup"><span data-stu-id="72711-121">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72711-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72711-122">Return value</span></span>

<span data-ttu-id="72711-123">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="72711-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72711-124">Notes</span><span class="sxs-lookup"><span data-stu-id="72711-124">Remarks</span></span>

<span data-ttu-id="72711-125">La fonction **RegisteredTask. Run** est équivalente à la fonction [**RegisteredTask. RunEx**](registeredtask-runex.md) avec le paramètre flags égal à 0 et rien n’est spécifié pour le paramètre User.</span><span class="sxs-lookup"><span data-stu-id="72711-125">The **RegisteredTask.Run** function is equivalent to the [**RegisteredTask.RunEx**](registeredtask-runex.md) function with the flags parameter equal to 0 and nothing specified for the user parameter.</span></span>

<span data-ttu-id="72711-126">Cette méthode retournera sans erreur, mais la tâche ne s’exécutera pas si la propriété [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) est définie sur false pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="72711-126">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="72711-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72711-127">Requirements</span></span>



| <span data-ttu-id="72711-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72711-128">Requirement</span></span> | <span data-ttu-id="72711-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="72711-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72711-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72711-130">Minimum supported client</span></span><br/> | <span data-ttu-id="72711-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72711-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="72711-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72711-132">Minimum supported server</span></span><br/> | <span data-ttu-id="72711-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72711-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72711-134">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="72711-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="72711-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72711-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72711-136">DLL</span><span class="sxs-lookup"><span data-stu-id="72711-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72711-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72711-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72711-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72711-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72711-139">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="72711-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="72711-140">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="72711-140">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





