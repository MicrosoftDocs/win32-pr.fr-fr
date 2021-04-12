---
title: TaskSettings. DeleteExpiredTaskAfter, propriété
description: Pour les scripts, obtient ou définit la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Planificateur de tâches de la propriété DeleteExpiredTaskAfter
- Planificateur de tâches de la propriété DeleteExpiredTaskAfter, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464802"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a><span data-ttu-id="3b57e-106">TaskSettings. DeleteExpiredTaskAfter, propriété</span><span class="sxs-lookup"><span data-stu-id="3b57e-106">TaskSettings.DeleteExpiredTaskAfter property</span></span>

<span data-ttu-id="3b57e-107">Pour les scripts, obtient ou définit la durée d’attente de la Planificateur de tâches avant la suppression de la tâche après son expiration.</span><span class="sxs-lookup"><span data-stu-id="3b57e-107">For scripting, gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="3b57e-108">Si aucune valeur n’est spécifiée pour cette propriété, le service Planificateur de tâches ne supprimera pas la tâche.</span><span class="sxs-lookup"><span data-stu-id="3b57e-108">If no value is specified for this property, then the Task Scheduler service will not delete the task.</span></span>

<span data-ttu-id="3b57e-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3b57e-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b57e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b57e-110">Syntax</span></span>


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a><span data-ttu-id="3b57e-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3b57e-111">Property value</span></span>

<span data-ttu-id="3b57e-112">Chaîne qui obtient ou définit la durée d’attente de la Planificateur de tâches avant de supprimer la tâche après son expiration.</span><span class="sxs-lookup"><span data-stu-id="3b57e-112">A string that gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="3b57e-113">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="3b57e-113">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b57e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3b57e-114">Remarks</span></span>

<span data-ttu-id="3b57e-115">Une tâche expire une fois que la limite de fin a été dépassée pour tous les déclencheurs associés à la tâche.</span><span class="sxs-lookup"><span data-stu-id="3b57e-115">A task expires after the end boundary has been exceeded for all triggers associated with the task.</span></span> <span data-ttu-id="3b57e-116">La limite de fin d’un déclencheur est spécifiée par la propriété [EndBoundary](trigger-endboundary.md) héritée par tous les objets déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="3b57e-116">The end boundary for a trigger is specified by the [EndBoundary](trigger-endboundary.md) property inherited by all trigger objects.</span></span>

<span data-ttu-id="3b57e-117">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="3b57e-117">When reading or writing XML for a task, this setting is specified in the [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b57e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b57e-118">Requirements</span></span>



| <span data-ttu-id="3b57e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b57e-119">Requirement</span></span> | <span data-ttu-id="3b57e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b57e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b57e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b57e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b57e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b57e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3b57e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b57e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b57e-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b57e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b57e-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3b57e-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b57e-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3b57e-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3b57e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3b57e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b57e-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b57e-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b57e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b57e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b57e-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="3b57e-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





