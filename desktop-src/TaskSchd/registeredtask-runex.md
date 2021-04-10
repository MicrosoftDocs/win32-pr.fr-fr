---
title: Méthode RegisteredTask. RunEx
description: Pour les scripts, exécute la tâche inscrite immédiatement à l’aide d’indicateurs spécifiés et d’un identificateur de session.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Planificateur de tâches de la méthode RunEx
- Méthode RunEx Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode RunEx
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104662"
---
# <a name="registeredtaskrunex-method"></a><span data-ttu-id="7647a-106">Méthode RegisteredTask. RunEx</span><span class="sxs-lookup"><span data-stu-id="7647a-106">RegisteredTask.RunEx method</span></span>

<span data-ttu-id="7647a-107">Pour les scripts, exécute la tâche inscrite immédiatement à l’aide d’indicateurs spécifiés et d’un identificateur de session.</span><span class="sxs-lookup"><span data-stu-id="7647a-107">For scripting, runs the registered task immediately using specified flags and a session identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="7647a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7647a-108">Syntax</span></span>


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="7647a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7647a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7647a-110">*paramètres* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7647a-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7647a-111">Paramètres utilisés comme valeurs dans les actions de tâche.</span><span class="sxs-lookup"><span data-stu-id="7647a-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="7647a-112">Pour ne pas spécifier de valeurs de paramètre pour les actions de tâche, attribuez la valeur **Nothing** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="7647a-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="7647a-113">Dans le cas contraire, vous pouvez spécifier une valeur de chaîne unique ou un tableau de valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7647a-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="7647a-114">Les valeurs de chaîne que vous spécifiez sont associées à des noms et stockées en tant que paires nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="7647a-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="7647a-115">Si vous spécifiez une valeur de chaîne unique, arg0 sera le nom affecté à la valeur.</span><span class="sxs-lookup"><span data-stu-id="7647a-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="7647a-116">La valeur peut être utilisée dans l’action de tâche où la variable $ (arg0) est utilisée dans les propriétés de l’action.</span><span class="sxs-lookup"><span data-stu-id="7647a-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="7647a-117">Si vous transmettez des valeurs telles que « 0 », « 100 » et « 250 » en tant que tableau de valeurs de chaîne, « 0 » remplace les variables $ (arg0), « 100 » remplace les variables $ (Arg1) et « 250 » remplace les variables $ (Arg2) utilisées dans les propriétés d’action.</span><span class="sxs-lookup"><span data-stu-id="7647a-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="7647a-118">Vous pouvez spécifier au maximum 32 valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7647a-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="7647a-119">Pour plus d’informations et pour obtenir la liste des propriétés d’action qui peuvent utiliser les variables $ (arg0), $ (Arg1),..., $ (Arg32) dans leurs valeurs, consultez [actions de tâche](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="7647a-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="7647a-120">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7647a-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7647a-121">Constante [d' \_ exécution \_ de tâche indicateurs](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) qui définit le mode d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7647a-121">A [TASK\_RUN\_FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) constant that defines how the task is run.</span></span>

</dd> <dt>

<span data-ttu-id="7647a-122">*SessionID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7647a-122">*sessionID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7647a-123">Session Terminal Server dans laquelle vous souhaitez lancer la tâche.</span><span class="sxs-lookup"><span data-stu-id="7647a-123">The terminal server session in which you want to launch the task.</span></span>

<span data-ttu-id="7647a-124">Si l’exécution de la tâche \_ \_ utiliser une \_ \_ constante d’ID de session (0x4) n’est pas passée dans le paramètre *Flags* , la valeur spécifiée dans ce paramètre est ignorée.</span><span class="sxs-lookup"><span data-stu-id="7647a-124">If the TASK\_RUN\_USE\_SESSION\_ID constant (0x4) is not passed into the *flags* parameter, then the value specified in this parameter is ignored.</span></span> <span data-ttu-id="7647a-125">Si la \_ constante exécuter la tâche \_ utiliser \_ \_ l’ID de session est passée dans le paramètre *Flags* et que la valeur SessionID est inférieure ou égale à 0, une erreur d’argument non valide est retournée.</span><span class="sxs-lookup"><span data-stu-id="7647a-125">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is less than or equal to 0, then an invalid argument error will be returned.</span></span>

<span data-ttu-id="7647a-126">Si la tâche \_ exécuter la tâche \_ utiliser l’ID de \_ session \_ est passée dans le paramètre *Flags* et que la valeur SessionID est un ID de session valide supérieur à 0 et si aucune valeur n’est spécifiée pour le paramètre *User* , le service Planificateur de tâches tente de lancer la tâche de manière interactive en tant qu’utilisateur connecté à la session spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7647a-126">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if no value is specified for the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is logged on to the specified session.</span></span>

<span data-ttu-id="7647a-127">Si la tâche \_ exécuter la tâche \_ utiliser l’ID de \_ session \_ est passée dans le paramètre *Flags* et que la valeur SessionID est un ID de session valide supérieur à 0 et si un utilisateur est spécifié dans le paramètre *User* , le service Planificateur de tâches essaiera de lancer la tâche de manière interactive en tant qu’utilisateur spécifié dans le paramètre *User* .</span><span class="sxs-lookup"><span data-stu-id="7647a-127">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if a user is specified in the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7647a-128">*runningTask* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7647a-128">*runningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7647a-129">Objet [**RunningTask**](runningtask.md) qui définit la nouvelle instance de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7647a-129">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7647a-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7647a-130">Return value</span></span>

<span data-ttu-id="7647a-131">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7647a-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7647a-132">Notes</span><span class="sxs-lookup"><span data-stu-id="7647a-132">Remarks</span></span>

<span data-ttu-id="7647a-133">Cette méthode retournera sans erreur, mais la tâche ne s’exécutera pas si la propriété [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) est définie sur false pour la tâche inscrite.</span><span class="sxs-lookup"><span data-stu-id="7647a-133">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="7647a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7647a-134">Requirements</span></span>



| <span data-ttu-id="7647a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7647a-135">Requirement</span></span> | <span data-ttu-id="7647a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7647a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7647a-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7647a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7647a-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7647a-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7647a-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7647a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7647a-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7647a-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7647a-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7647a-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="7647a-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7647a-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7647a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7647a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7647a-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7647a-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7647a-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7647a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7647a-146">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7647a-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="7647a-147">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="7647a-147">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





