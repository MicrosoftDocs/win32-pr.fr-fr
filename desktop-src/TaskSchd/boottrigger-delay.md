---
title: BootTrigger. Delay, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la durée entre le démarrage du système et le démarrage de la tâche.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Planificateur de tâches de propriétés Delay
- Planificateur de tâches de propriété Delay, objet BootTrigger
- Planificateur de tâches objet BootTrigger, propriété Delay
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104668"
---
# <a name="boottriggerdelay-property"></a><span data-ttu-id="a7509-106">BootTrigger. Delay, propriété</span><span class="sxs-lookup"><span data-stu-id="a7509-106">BootTrigger.Delay property</span></span>

<span data-ttu-id="a7509-107">Pour les scripts, obtient ou définit une valeur qui indique la durée entre le démarrage du système et le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a7509-107">For scripting, gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7509-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7509-108">Syntax</span></span>


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="a7509-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a7509-109">Property value</span></span>

<span data-ttu-id="a7509-110">Valeur qui indique la durée entre le démarrage du système et le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="a7509-110">A value that indicates the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="a7509-111">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="a7509-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7509-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a7509-112">Remarks</span></span>

<span data-ttu-id="a7509-113">Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, le délai de démarrage est spécifié à l’aide de l’élément [**delay**](taskschedulerschema-delay-boottriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="a7509-113">When reading or writing your own XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7509-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7509-114">Requirements</span></span>



| <span data-ttu-id="a7509-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7509-115">Requirement</span></span> | <span data-ttu-id="a7509-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7509-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7509-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7509-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a7509-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7509-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a7509-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7509-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a7509-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7509-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7509-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a7509-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7509-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a7509-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a7509-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a7509-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7509-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7509-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7509-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7509-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7509-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a7509-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="a7509-127">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="a7509-127">**BootTrigger**</span></span>](boottrigger.md)
</dt> </dl>

 

 





