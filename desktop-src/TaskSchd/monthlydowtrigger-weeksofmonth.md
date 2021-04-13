---
title: MonthlyDOWTrigger. WeeksOfMonth, propriété
description: Pour les scripts, obtient ou définit les semaines du mois pendant lequel la tâche s’exécute.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Planificateur de tâches de la propriété WeeksOfMonth
- Planificateur de tâches de la propriété WeeksOfMonth, objet MonthlyDOWTrigger
- Planificateur de tâches objet MonthlyDOWTrigger, propriété WeeksOfMonth
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464702"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a><span data-ttu-id="c6ca1-106">MonthlyDOWTrigger. WeeksOfMonth, propriété</span><span class="sxs-lookup"><span data-stu-id="c6ca1-106">MonthlyDOWTrigger.WeeksOfMonth property</span></span>

<span data-ttu-id="c6ca1-107">Pour les scripts, obtient ou définit les semaines du mois pendant lequel la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="c6ca1-107">For scripting, gets or sets the weeks of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ca1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6ca1-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a><span data-ttu-id="c6ca1-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c6ca1-109">Property value</span></span>

<span data-ttu-id="c6ca1-110">Un masque de bits qui indique les jours de la semaine pendant lesquels la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="c6ca1-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6ca1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c6ca1-111">Remarks</span></span>

<span data-ttu-id="c6ca1-112">Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c6ca1-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="c6ca1-113">Semaine</span><span class="sxs-lookup"><span data-stu-id="c6ca1-113">Week</span></span>                     | <span data-ttu-id="c6ca1-114">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="c6ca1-114">Hex Value</span></span> | <span data-ttu-id="c6ca1-115">Valeur décimale</span><span class="sxs-lookup"><span data-stu-id="c6ca1-115">Decimal Value</span></span> |
|--------------------------|-----------|---------------|
| <span data-ttu-id="c6ca1-116">Première semaine du mois</span><span class="sxs-lookup"><span data-stu-id="c6ca1-116">First week of the month</span></span>  | <span data-ttu-id="c6ca1-117">0X01</span><span class="sxs-lookup"><span data-stu-id="c6ca1-117">0X01</span></span>      | <span data-ttu-id="c6ca1-118">1</span><span class="sxs-lookup"><span data-stu-id="c6ca1-118">1</span></span>             |
| <span data-ttu-id="c6ca1-119">Deuxième semaine du mois</span><span class="sxs-lookup"><span data-stu-id="c6ca1-119">Second week of the month</span></span> | <span data-ttu-id="c6ca1-120">0x02</span><span class="sxs-lookup"><span data-stu-id="c6ca1-120">0x02</span></span>      | <span data-ttu-id="c6ca1-121">2</span><span class="sxs-lookup"><span data-stu-id="c6ca1-121">2</span></span>             |
| <span data-ttu-id="c6ca1-122">Troisième semaine du mois</span><span class="sxs-lookup"><span data-stu-id="c6ca1-122">Third week of the month</span></span>  | <span data-ttu-id="c6ca1-123">0X04</span><span class="sxs-lookup"><span data-stu-id="c6ca1-123">0X04</span></span>      | <span data-ttu-id="c6ca1-124">4</span><span class="sxs-lookup"><span data-stu-id="c6ca1-124">4</span></span>             |
| <span data-ttu-id="c6ca1-125">Quatrième semaine du mois</span><span class="sxs-lookup"><span data-stu-id="c6ca1-125">Fourth week of the month</span></span> | <span data-ttu-id="c6ca1-126">0X08</span><span class="sxs-lookup"><span data-stu-id="c6ca1-126">0X08</span></span>      | <span data-ttu-id="c6ca1-127">8</span><span class="sxs-lookup"><span data-stu-id="c6ca1-127">8</span></span>             |



 

<span data-ttu-id="c6ca1-128">Lors de la lecture ou de l’écriture de données XML pour une tâche, les jours de la semaine d’un calendrier de jour de semaine mensuel sont spécifiés par l’élément [**weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c6ca1-128">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ca1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6ca1-129">Requirements</span></span>



| <span data-ttu-id="c6ca1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6ca1-130">Requirement</span></span> | <span data-ttu-id="c6ca1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6ca1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ca1-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6ca1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ca1-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6ca1-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c6ca1-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6ca1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ca1-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6ca1-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6ca1-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c6ca1-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6ca1-137"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c6ca1-137"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c6ca1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c6ca1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6ca1-139"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6ca1-139"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ca1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6ca1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ca1-141">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="c6ca1-141">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="c6ca1-142">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c6ca1-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





