---
title: IdleSettings. WaitTimeout, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Planificateur de tâches de la propriété WaitTimeout
- Planificateur de tâches de la propriété WaitTimeout, objet IdleSettings
- Planificateur de tâches objet IdleSettings, propriété WaitTimeout
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032962"
---
# <a name="idlesettingswaittimeout-property"></a><span data-ttu-id="e5fdd-106">IdleSettings. WaitTimeout, propriété</span><span class="sxs-lookup"><span data-stu-id="e5fdd-106">IdleSettings.WaitTimeout property</span></span>

<span data-ttu-id="e5fdd-107">Pour les scripts, obtient ou définit une valeur qui indique la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-107">For scripting, gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="e5fdd-108">Si aucune valeur n’est spécifiée pour cette propriété, le service Planificateur de tâches attend indéfiniment qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-108">If no value is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5fdd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5fdd-109">Syntax</span></span>


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a><span data-ttu-id="e5fdd-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e5fdd-110">Property value</span></span>

<span data-ttu-id="e5fdd-111">Valeur qui indique la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-111">A value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="e5fdd-112">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="e5fdd-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e5fdd-113">La durée minimale autorisée est de 1 minute.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-113">The minimum time allowed is 1 minute.</span></span> <span data-ttu-id="e5fdd-114">Si cette valeur est **null**, le délai prend la valeur par défaut de 1 heure.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-114">If this value is **NULL**, then the delay will be set to the default of 1 hour.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5fdd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e5fdd-115">Remarks</span></span>

<span data-ttu-id="e5fdd-116">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-116">When reading or writing XML for a task, this setting is specified in the [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="e5fdd-117">Si une tâche est déclenchée par un déclencheur inactif, la propriété **IdleSettings. WaitTimeout** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="e5fdd-117">If a task is triggered by an idle trigger, then the **IdleSettings.WaitTimeout** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5fdd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5fdd-118">Requirements</span></span>



| <span data-ttu-id="e5fdd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5fdd-119">Requirement</span></span> | <span data-ttu-id="e5fdd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5fdd-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5fdd-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5fdd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e5fdd-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5fdd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e5fdd-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5fdd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e5fdd-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5fdd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5fdd-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e5fdd-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e5fdd-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e5fdd-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e5fdd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e5fdd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5fdd-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5fdd-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5fdd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5fdd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5fdd-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e5fdd-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e5fdd-131">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="e5fdd-131">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





