---
title: IdleSettings. IdleDuration, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche soit exécutée.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Planificateur de tâches de la propriété IdleDuration
- Planificateur de tâches de la propriété IdleDuration, objet IdleSettings
- Planificateur de tâches objet IdleSettings, propriété IdleDuration
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742453"
---
# <a name="idlesettingsidleduration-property"></a><span data-ttu-id="6e1e2-106">IdleSettings. IdleDuration, propriété</span><span class="sxs-lookup"><span data-stu-id="6e1e2-106">IdleSettings.IdleDuration property</span></span>

<span data-ttu-id="6e1e2-107">Pour les scripts, obtient ou définit une valeur qui indique la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche soit exécutée.</span><span class="sxs-lookup"><span data-stu-id="6e1e2-107">For scripting, gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e1e2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e1e2-108">Syntax</span></span>


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a><span data-ttu-id="6e1e2-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6e1e2-109">Property value</span></span>

<span data-ttu-id="6e1e2-110">Valeur qui indique la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche ne soit exécutée.</span><span class="sxs-lookup"><span data-stu-id="6e1e2-110">A value that indicates the amount of time that the computer must be in an idle state before the task is run).</span></span> <span data-ttu-id="6e1e2-111">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="6e1e2-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="6e1e2-112">La valeur minimale est d’une minute.</span><span class="sxs-lookup"><span data-stu-id="6e1e2-112">The minimum value is one minute.</span></span> <span data-ttu-id="6e1e2-113">Si cette valeur est **null**, le délai est défini sur la valeur par défaut de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="6e1e2-113">If this value is **NULL**, then the delay will be set to the default of 10 minutes.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e1e2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6e1e2-114">Remarks</span></span>

<span data-ttu-id="6e1e2-115">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="6e1e2-115">When reading or writing XML for a task, this setting is specified in the [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1e2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e1e2-116">Requirements</span></span>



| <span data-ttu-id="6e1e2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e1e2-117">Requirement</span></span> | <span data-ttu-id="6e1e2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e1e2-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1e2-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e1e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1e2-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e1e2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6e1e2-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e1e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1e2-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e1e2-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e1e2-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6e1e2-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e1e2-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6e1e2-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6e1e2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6e1e2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e1e2-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e1e2-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e1e2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e1e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1e2-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="6e1e2-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="6e1e2-129">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="6e1e2-129">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





