---
title: Objet RepetitionPattern
description: Objet de script qui définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- déclencheur Planificateur de tâches, objet de modèle de répétition
- modèle de répétition Planificateur de tâches, objet
- Objet RepetitionPattern Planificateur de tâches
- Planificateur de tâches d’objets RepetitionPattern, Description
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464814"
---
# <a name="repetitionpattern-object"></a><span data-ttu-id="26137-107">Objet RepetitionPattern</span><span class="sxs-lookup"><span data-stu-id="26137-107">RepetitionPattern object</span></span>

<span data-ttu-id="26137-108">Objet de script qui définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="26137-108">Scripting object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="members"></a><span data-ttu-id="26137-109">Membres</span><span class="sxs-lookup"><span data-stu-id="26137-109">Members</span></span>

<span data-ttu-id="26137-110">L’objet **RepetitionPattern** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26137-110">The **RepetitionPattern** object has these types of members:</span></span>

-   [<span data-ttu-id="26137-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26137-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26137-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26137-112">Properties</span></span>

<span data-ttu-id="26137-113">L’objet **RepetitionPattern** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="26137-113">The **RepetitionPattern** object has these properties.</span></span>



| <span data-ttu-id="26137-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="26137-114">Property</span></span>                                                                    | <span data-ttu-id="26137-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="26137-115">Access type</span></span>           | <span data-ttu-id="26137-116">Description</span><span class="sxs-lookup"><span data-stu-id="26137-116">Description</span></span>                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26137-117">**Duration**</span><span class="sxs-lookup"><span data-stu-id="26137-117">**Duration**</span></span>](repetitionpattern-duration.md)<br/>                   | <span data-ttu-id="26137-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="26137-118">Read/write</span></span><br/> | <span data-ttu-id="26137-119">Obtient ou définit la durée de répétition du modèle.</span><span class="sxs-lookup"><span data-stu-id="26137-119">Gets or sets how long the pattern is repeated.</span></span><br/>                                                                                          |
| [<span data-ttu-id="26137-120">**Défini**</span><span class="sxs-lookup"><span data-stu-id="26137-120">**Interval**</span></span>](repetitionpattern-interval.md)<br/>                   | <span data-ttu-id="26137-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="26137-121">Read/write</span></span><br/> | <span data-ttu-id="26137-122">Obtient ou définit la durée entre chaque redémarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="26137-122">Gets or sets the amount of time between each restart of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="26137-123">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="26137-123">**StopAtDurationEnd**</span></span>](repetitionpattern-stopatdurationend.md)<br/> | <span data-ttu-id="26137-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="26137-124">Read/write</span></span><br/> | <span data-ttu-id="26137-125">Obtient ou définit une valeur booléenne qui indique si une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.</span><span class="sxs-lookup"><span data-stu-id="26137-125">Gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="26137-126">Notes</span><span class="sxs-lookup"><span data-stu-id="26137-126">Remarks</span></span>

<span data-ttu-id="26137-127">Si vous spécifiez une durée de répétition pour une tâche, vous devez également spécifier l’intervalle de répétition.</span><span class="sxs-lookup"><span data-stu-id="26137-127">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="26137-128">Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est lancée cinq fois.</span><span class="sxs-lookup"><span data-stu-id="26137-128">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="26137-129">Les cinq répétitions peuvent être définies par le modèle suivant.</span><span class="sxs-lookup"><span data-stu-id="26137-129">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="26137-130">Une tâche commence au début de la première minute.</span><span class="sxs-lookup"><span data-stu-id="26137-130">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="26137-131">La tâche suivante démarre à la fin de la première minute.</span><span class="sxs-lookup"><span data-stu-id="26137-131">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="26137-132">La tâche suivante démarre à la fin de la seconde minute.</span><span class="sxs-lookup"><span data-stu-id="26137-132">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="26137-133">La tâche suivante démarre à la fin de la troisième minute.</span><span class="sxs-lookup"><span data-stu-id="26137-133">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="26137-134">La tâche suivante démarre à la fin de la quatrième minute.</span><span class="sxs-lookup"><span data-stu-id="26137-134">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="26137-135">**Windows Server 2003, Windows XP et windows 2000 :** Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est lancée quatre fois.</span><span class="sxs-lookup"><span data-stu-id="26137-135">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="26137-136">Lors de la lecture ou de l’écriture de données XML pour une tâche, le modèle de répétition est spécifié à l’aide de l’élément de [**répétition**](taskschedulerschema-repetition-triggerbasetype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="26137-136">When reading or writing XML for a task, the repetition pattern is specified using the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="26137-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="26137-137">Examples</span></span>

<span data-ttu-id="26137-138">Pour plus d’informations et pour obtenir un exemple de code pour cette propriété, consultez [exemple de déclencheur quotidien (script)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="26137-138">For more information and example code for this property, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26137-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26137-139">Requirements</span></span>



| <span data-ttu-id="26137-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26137-140">Requirement</span></span> | <span data-ttu-id="26137-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="26137-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26137-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26137-142">Minimum supported client</span></span><br/> | <span data-ttu-id="26137-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26137-143">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="26137-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26137-144">Minimum supported server</span></span><br/> | <span data-ttu-id="26137-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26137-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26137-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="26137-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="26137-147"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26137-147"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26137-148">DLL</span><span class="sxs-lookup"><span data-stu-id="26137-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26137-149"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26137-149"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26137-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26137-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26137-151">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="26137-151">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="26137-152">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="26137-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





