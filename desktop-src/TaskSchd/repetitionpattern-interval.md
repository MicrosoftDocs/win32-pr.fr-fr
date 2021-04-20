---
title: RepetitionPattern. Interval, propriété
description: Pour les scripts, obtient ou définit la durée entre chaque redémarrage de la tâche.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Planificateur de tâches de la propriété Interval
- Planificateur de tâches de la propriété Interval, objet RepetitionPattern
- Objet RepetitionPattern Planificateur de tâches, propriété Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734174"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="d5a5f-106">RepetitionPattern. Interval, propriété</span><span class="sxs-lookup"><span data-stu-id="d5a5f-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="d5a5f-107">Pour les scripts, obtient ou définit la durée entre chaque redémarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a5f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5a5f-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="d5a5f-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d5a5f-109">Property value</span></span>

<span data-ttu-id="d5a5f-110">Intervalle de temps entre chaque redémarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="d5a5f-111">Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, « PT5M » est de 5 minutes, « PT1H » est 1 heure et « PT20M » est 20 minutes).</span><span class="sxs-lookup"><span data-stu-id="d5a5f-111">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="d5a5f-112">La durée maximale autorisée est de 31 jours, et la durée minimale autorisée est de 1 minute.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5a5f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="d5a5f-113">Remarks</span></span>

<span data-ttu-id="d5a5f-114">Si vous spécifiez une durée de répétition pour une tâche, vous devez également spécifier l’intervalle de répétition.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="d5a5f-115">Lors de la lecture ou de l’écriture de données XML pour une tâche, l’intervalle de répétition est spécifié dans l’élément [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="d5a5f-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a5f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5a5f-116">Requirements</span></span>



| <span data-ttu-id="d5a5f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5a5f-117">Requirement</span></span> | <span data-ttu-id="d5a5f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5a5f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a5f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5a5f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a5f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5a5f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d5a5f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5a5f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a5f-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5a5f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5a5f-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d5a5f-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d5a5f-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d5a5f-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d5a5f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d5a5f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5a5f-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5a5f-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5a5f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5a5f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a5f-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d5a5f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





