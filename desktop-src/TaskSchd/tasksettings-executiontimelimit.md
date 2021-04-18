---
title: TaskSettings.Exepropriété cutionTimeLimit
description: Pour les scripts, obtient ou définit la durée autorisée pour terminer la tâche.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Planificateur de tâches de la propriété ExecutionTimeLimit
- Planificateur de tâches de la propriété ExecutionTimeLimit, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété ExecutionTimeLimit
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509343"
---
# <a name="tasksettingsexecutiontimelimit-property"></a><span data-ttu-id="23303-106">TaskSettings.Exepropriété cutionTimeLimit</span><span class="sxs-lookup"><span data-stu-id="23303-106">TaskSettings.ExecutionTimeLimit property</span></span>

<span data-ttu-id="23303-107">Pour les scripts, obtient ou définit la durée autorisée pour terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="23303-107">For scripting, gets or sets the amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="23303-108">Par défaut, une tâche sera arrêtée 72 heures après son démarrage.</span><span class="sxs-lookup"><span data-stu-id="23303-108">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="23303-109">Vous pouvez modifier ce paramètre en modifiant ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="23303-109">You can change this by changing this setting.</span></span>

<span data-ttu-id="23303-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="23303-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="23303-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23303-111">Syntax</span></span>


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="23303-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="23303-112">Property value</span></span>

<span data-ttu-id="23303-113">Durée autorisée pour terminer la tâche.</span><span class="sxs-lookup"><span data-stu-id="23303-113">The amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="23303-114">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="23303-114">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="23303-115">La valeur PT0S permet à la tâche de s’exécuter indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="23303-115">A value of PT0S will enable the task to run indefinitely.</span></span> <span data-ttu-id="23303-116">Lorsque ce paramètre a la valeur Nothing, la limite de durée d’exécution est infinie.</span><span class="sxs-lookup"><span data-stu-id="23303-116">When this parameter is set to Nothing, the execution time limit is infinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="23303-117">Notes</span><span class="sxs-lookup"><span data-stu-id="23303-117">Remarks</span></span>

<span data-ttu-id="23303-118">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="23303-118">When reading or writing XML for a task, this setting is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="23303-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23303-119">Requirements</span></span>



| <span data-ttu-id="23303-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23303-120">Requirement</span></span> | <span data-ttu-id="23303-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="23303-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23303-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23303-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23303-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23303-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="23303-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23303-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23303-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23303-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23303-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="23303-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="23303-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23303-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23303-128">DLL</span><span class="sxs-lookup"><span data-stu-id="23303-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23303-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23303-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23303-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23303-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23303-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="23303-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





