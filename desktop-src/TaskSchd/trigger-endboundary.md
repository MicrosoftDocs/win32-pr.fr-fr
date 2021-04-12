---
title: Propriété Trigger. EndBoundary
description: Pour les scripts, obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Planificateur de tâches de la propriété EndBoundary
- Propriété EndBoundary Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet de déclencheur, propriété EndBoundary
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032642"
---
# <a name="triggerendboundary-property"></a><span data-ttu-id="9fe76-107">Propriété Trigger. EndBoundary</span><span class="sxs-lookup"><span data-stu-id="9fe76-107">Trigger.EndBoundary property</span></span>

<span data-ttu-id="9fe76-108">Pour les scripts, obtient ou définit la date et l’heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="9fe76-108">For scripting, gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="9fe76-109">Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="9fe76-109">The trigger cannot start the task after it is deactivated.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe76-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fe76-110">Syntax</span></span>


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="9fe76-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9fe76-111">Property value</span></span>

<span data-ttu-id="9fe76-112">Date et heure de désactivation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="9fe76-112">The date and time when the trigger is deactivated.</span></span> <span data-ttu-id="9fe76-113">La date et l’heure doivent être au format suivant : AAAA-MM-JJThh : MM : SS (+-) HH : MM.</span><span class="sxs-lookup"><span data-stu-id="9fe76-113">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="9fe76-114">Par exemple, la date du 11 octobre 2005 à 1:21:17 dans le fuseau horaire Pacifique serait écrite sous la forme 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="9fe76-114">For example the date October 11th, 2005 at 1:21:17 in the Pacific time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="9fe76-115">La section (+-) HH : MM du format décrit le fuseau horaire comme un certain nombre d’heures avant ou après le temps universel coordonné (heure de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="9fe76-115">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="9fe76-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9fe76-116">Remarks</span></span>

<span data-ttu-id="9fe76-117">Lors de la lecture ou de l’écriture de données XML pour une tâche, la propriété Enabled est spécifiée à l’aide de l’élément [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="9fe76-117">When reading or writing XML for a task, the enabled property is specified using the [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe76-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fe76-118">Requirements</span></span>



| <span data-ttu-id="9fe76-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fe76-119">Requirement</span></span> | <span data-ttu-id="9fe76-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fe76-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe76-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fe76-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe76-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fe76-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9fe76-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fe76-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe76-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fe76-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9fe76-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9fe76-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fe76-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9fe76-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9fe76-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9fe76-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fe76-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe76-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fe76-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fe76-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe76-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="9fe76-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





