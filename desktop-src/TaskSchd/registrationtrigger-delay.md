---
title: RegistrationTrigger. Delay, propriété
description: Pour les scripts, obtient ou définit la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Planificateur de tâches de propriétés Delay
- Planificateur de tâches de propriété Delay, objet RegistrationTrigger
- Planificateur de tâches objet RegistrationTrigger, propriété Delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509125"
---
# <a name="registrationtriggerdelay-property"></a><span data-ttu-id="057f2-106">RegistrationTrigger. Delay, propriété</span><span class="sxs-lookup"><span data-stu-id="057f2-106">RegistrationTrigger.Delay property</span></span>

<span data-ttu-id="057f2-107">Pour les scripts, obtient ou définit la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="057f2-107">For scripting, gets or sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="057f2-108">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="057f2-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="057f2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="057f2-109">Syntax</span></span>


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="057f2-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="057f2-110">Property value</span></span>

<span data-ttu-id="057f2-111">Intervalle de temps entre le moment où le système est inscrit et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="057f2-111">The amount of time between when the system is registered and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="057f2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="057f2-112">Remarks</span></span>

<span data-ttu-id="057f2-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, le délai de démarrage est spécifié à l’aide de l’élément [**delay**](taskschedulerschema-delay-registrationtriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="057f2-113">When reading or writing XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="057f2-114">Si une tâche avec un déclencheur d’inscription différé est inscrite et que l’ordinateur sur lequel la tâche est inscrite est arrêté ou redémarré pendant le délai, avant l’exécution de la tâche, la tâche ne s’exécutera pas et le délai sera perdu.</span><span class="sxs-lookup"><span data-stu-id="057f2-114">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="057f2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="057f2-115">Requirements</span></span>



| <span data-ttu-id="057f2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="057f2-116">Requirement</span></span> | <span data-ttu-id="057f2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="057f2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="057f2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="057f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="057f2-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="057f2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="057f2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="057f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="057f2-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="057f2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="057f2-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="057f2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="057f2-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="057f2-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="057f2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="057f2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="057f2-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="057f2-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="057f2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="057f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057f2-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="057f2-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





