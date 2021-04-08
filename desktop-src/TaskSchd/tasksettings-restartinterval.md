---
title: TaskSettings. RestartInterval, propriété
description: Pour les scripts, obtient ou définit une valeur qui spécifie la durée pendant laquelle l’Planificateur de tâches tente de redémarrer la tâche.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Planificateur de tâches de la propriété RestartInterval
- Planificateur de tâches de la propriété RestartInterval, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740421"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="4347f-106">TaskSettings. RestartInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="4347f-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="4347f-107">Pour les scripts, obtient ou définit une valeur qui spécifie la durée pendant laquelle l’Planificateur de tâches tente de redémarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="4347f-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="4347f-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4347f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4347f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4347f-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="4347f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4347f-110">Property value</span></span>

<span data-ttu-id="4347f-111">Valeur qui spécifie la durée pendant laquelle l’Planificateur de tâches tente de redémarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="4347f-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="4347f-112">Si cette propriété est définie, la propriété [**RestartCount**](tasksettings-restartcount.md) doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="4347f-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="4347f-113">Le format de cette chaîne est P <days> DT <hours> H <minutes> M <seconds> S (par exemple, « PT5M » est de 5 minutes, « PT1H » est 1 heure et « PT20M » est de 20 minutes).</span><span class="sxs-lookup"><span data-stu-id="4347f-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="4347f-114">La durée maximale autorisée est de 31 jours, et la durée minimale autorisée est de 1 minute.</span><span class="sxs-lookup"><span data-stu-id="4347f-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="4347f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4347f-115">Remarks</span></span>

<span data-ttu-id="4347f-116">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Interval**](taskschedulerschema-interval-restarttype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="4347f-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4347f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4347f-117">Requirements</span></span>



| <span data-ttu-id="4347f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4347f-118">Requirement</span></span> | <span data-ttu-id="4347f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4347f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4347f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4347f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4347f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4347f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4347f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4347f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4347f-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4347f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4347f-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4347f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4347f-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4347f-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4347f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4347f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4347f-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4347f-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4347f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4347f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4347f-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4347f-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





