---
title: TaskSettings. StopIfGoingOnBatteries, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche sera arrêtée si l’ordinateur est sur batteries.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Planificateur de tâches de la propriété StopIfGoingOnBatteries
- Planificateur de tâches de la propriété StopIfGoingOnBatteries, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466399"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a><span data-ttu-id="1d088-106">TaskSettings. StopIfGoingOnBatteries, propriété</span><span class="sxs-lookup"><span data-stu-id="1d088-106">TaskSettings.StopIfGoingOnBatteries property</span></span>

<span data-ttu-id="1d088-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche sera arrêtée si l’ordinateur est sur batteries.</span><span class="sxs-lookup"><span data-stu-id="1d088-107">For scripting, gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span>

<span data-ttu-id="1d088-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1d088-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d088-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d088-109">Syntax</span></span>


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="1d088-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1d088-110">Property value</span></span>

<span data-ttu-id="1d088-111">Valeur booléenne qui indique que la tâche sera arrêtée si l’ordinateur passe sur batteries.</span><span class="sxs-lookup"><span data-stu-id="1d088-111">A Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="1d088-112">Si la valeur est true, la propriété indique que la tâche sera arrêtée si l’ordinateur passe sur batteries.</span><span class="sxs-lookup"><span data-stu-id="1d088-112">If True, the property indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="1d088-113">Si la valeur est false, la propriété indique que la tâche ne sera pas arrêtée si l’ordinateur passe sur batteries.</span><span class="sxs-lookup"><span data-stu-id="1d088-113">If False, the property indicates that the task will not be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="1d088-114">La valeur par défaut est True.</span><span class="sxs-lookup"><span data-stu-id="1d088-114">The default is True.</span></span> <span data-ttu-id="1d088-115">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1d088-115">See Remarks for more details.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d088-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1d088-116">Remarks</span></span>

<span data-ttu-id="1d088-117">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="1d088-117">When reading or writing XML for a task, this setting is specified in the [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d088-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d088-118">Requirements</span></span>



| <span data-ttu-id="1d088-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d088-119">Requirement</span></span> | <span data-ttu-id="1d088-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d088-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d088-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d088-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1d088-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d088-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1d088-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d088-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1d088-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d088-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1d088-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1d088-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d088-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1d088-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1d088-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1d088-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d088-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d088-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d088-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d088-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d088-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1d088-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





