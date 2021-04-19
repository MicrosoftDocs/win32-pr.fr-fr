---
title: EventTrigger. Delay, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Planificateur de tâches de propriétés Delay
- Planificateur de tâches de propriété Delay, objet EventTrigger
- Objet EventTrigger Planificateur de tâches, propriété Delay
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509927"
---
# <a name="eventtriggerdelay-property"></a><span data-ttu-id="c0c82-106">EventTrigger. Delay, propriété</span><span class="sxs-lookup"><span data-stu-id="c0c82-106">EventTrigger.Delay property</span></span>

<span data-ttu-id="c0c82-107">Pour les scripts, obtient ou définit une valeur qui indique la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="c0c82-107">For scripting, gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="c0c82-108">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="c0c82-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c82-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0c82-109">Syntax</span></span>


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="c0c82-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c0c82-110">Property value</span></span>

<span data-ttu-id="c0c82-111">Valeur qui indique la durée écoulée entre le moment où l’événement se produit et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="c0c82-111">A value that indicates the amount of time between when the event occurs and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0c82-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c0c82-112">Remarks</span></span>

<span data-ttu-id="c0c82-113">Lors de la lecture ou de l’écriture de votre propre code XML pour une tâche, le délai d’événement est spécifié à l’aide de l’élément [**delay**](taskschedulerschema-delay-eventtriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="c0c82-113">When reading or writing your own XML for a task, the event delay is specified using the [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0c82-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0c82-114">Requirements</span></span>



| <span data-ttu-id="c0c82-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0c82-115">Requirement</span></span> | <span data-ttu-id="c0c82-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0c82-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c82-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0c82-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0c82-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0c82-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c0c82-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0c82-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0c82-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0c82-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0c82-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c0c82-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0c82-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0c82-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0c82-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c0c82-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0c82-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0c82-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0c82-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0c82-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0c82-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c0c82-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c0c82-127">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0c82-127">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

 





