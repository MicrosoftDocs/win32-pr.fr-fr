---
title: RepetitionPattern. Duration, propriété
description: Pour les scripts, obtient ou définit la durée de répétition du modèle.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Propriété Duration Planificateur de tâches
- Propriété Duration Planificateur de tâches, objet RepetitionPattern
- Planificateur de tâches objet RepetitionPattern, propriété Duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510154"
---
# <a name="repetitionpatternduration-property"></a><span data-ttu-id="77e50-106">RepetitionPattern. Duration, propriété</span><span class="sxs-lookup"><span data-stu-id="77e50-106">RepetitionPattern.Duration property</span></span>

<span data-ttu-id="77e50-107">Pour les scripts, obtient ou définit la durée de répétition du modèle.</span><span class="sxs-lookup"><span data-stu-id="77e50-107">For scripting, gets or sets how long the pattern is repeated.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e50-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77e50-108">Syntax</span></span>


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a><span data-ttu-id="77e50-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="77e50-109">Property value</span></span>

<span data-ttu-id="77e50-110">Durée de répétition du modèle.</span><span class="sxs-lookup"><span data-stu-id="77e50-110">How long the pattern is repeated.</span></span> <span data-ttu-id="77e50-111">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="77e50-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="77e50-112">La durée minimale autorisée est d’une minute.</span><span class="sxs-lookup"><span data-stu-id="77e50-112">The minimum time allowed is one minute.</span></span>

<span data-ttu-id="77e50-113">Si aucune valeur n’est spécifiée pour la durée, le modèle est répété indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="77e50-113">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span>

## <a name="remarks"></a><span data-ttu-id="77e50-114">Notes</span><span class="sxs-lookup"><span data-stu-id="77e50-114">Remarks</span></span>

<span data-ttu-id="77e50-115">Si vous spécifiez une durée de répétition pour une tâche, vous devez également spécifier l’intervalle de répétition.</span><span class="sxs-lookup"><span data-stu-id="77e50-115">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="77e50-116">Lors de la lecture ou de l’écriture de données XML pour une tâche, la durée de répétition est spécifiée dans l’élément [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="77e50-116">When reading or writing XML for a task, the repetition duration is specified in the [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="77e50-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77e50-117">Requirements</span></span>



| <span data-ttu-id="77e50-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77e50-118">Requirement</span></span> | <span data-ttu-id="77e50-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="77e50-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77e50-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77e50-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77e50-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77e50-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="77e50-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77e50-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77e50-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77e50-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77e50-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="77e50-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="77e50-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="77e50-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="77e50-126">DLL</span><span class="sxs-lookup"><span data-stu-id="77e50-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77e50-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77e50-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e50-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77e50-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e50-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="77e50-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





