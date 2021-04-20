---
title: DailyTrigger. RandomDelay, propriété
description: Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur. | DailyTrigger. RandomDelay, propriété
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Planificateur de tâches de la propriété RandomDelay
- Planificateur de tâches de la propriété RandomDelay, objet DailyTrigger
- Planificateur de tâches objet DailyTrigger, propriété RandomDelay
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303192d578a2681e250784c1e1eb2831c98482cc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734104"
---
# <a name="dailytriggerrandomdelay-property"></a><span data-ttu-id="d0615-107">DailyTrigger. RandomDelay, propriété</span><span class="sxs-lookup"><span data-stu-id="d0615-107">DailyTrigger.RandomDelay property</span></span>

<span data-ttu-id="d0615-108">Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="d0615-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0615-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0615-109">Syntax</span></span>


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="d0615-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d0615-110">Property value</span></span>

<span data-ttu-id="d0615-111">Délai d’ajout aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="d0615-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="d0615-112">Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, P2DT5S est un délai de 2 jours, 5 secondes).</span><span class="sxs-lookup"><span data-stu-id="d0615-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0615-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0615-113">Requirements</span></span>



| <span data-ttu-id="d0615-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0615-114">Requirement</span></span> | <span data-ttu-id="d0615-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0615-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0615-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0615-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d0615-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0615-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d0615-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0615-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d0615-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0615-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0615-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d0615-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0615-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0615-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0615-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d0615-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0615-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0615-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0615-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0615-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0615-125">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="d0615-125">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> <dt>

[<span data-ttu-id="d0615-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d0615-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





