---
title: Propriété Trigger. StartBoundary
description: Pour les scripts, obtient ou définit la date et l’heure d’activation du déclencheur.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Planificateur de tâches de la propriété StartBoundary
- Propriété StartBoundary Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet de déclencheur, propriété StartBoundary
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740796"
---
# <a name="triggerstartboundary-property"></a><span data-ttu-id="15291-106">Propriété Trigger. StartBoundary</span><span class="sxs-lookup"><span data-stu-id="15291-106">Trigger.StartBoundary property</span></span>

<span data-ttu-id="15291-107">Pour les scripts, obtient ou définit la date et l’heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="15291-107">For scripting, gets or sets the date and time when the trigger is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="15291-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15291-108">Syntax</span></span>


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="15291-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="15291-109">Property value</span></span>

<span data-ttu-id="15291-110">Date et heure d’activation du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="15291-110">The date and time when the trigger is activated.</span></span> <span data-ttu-id="15291-111">La date et l’heure doivent être au format suivant : AAAA-MM-JJThh : MM : SS (+-) HH : MM.</span><span class="sxs-lookup"><span data-stu-id="15291-111">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="15291-112">Par exemple, la date du 11 octobre 2005 à 1:21:17 dans le fuseau horaire Pacifique serait écrite sous la forme 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="15291-112">For example the date October 11th, 2005 at 1:21:17 in the Pacific Time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="15291-113">La section (+-) HH : MM du format décrit le fuseau horaire comme un certain nombre d’heures avant ou après le temps universel coordonné (heure de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="15291-113">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="15291-114">Notes</span><span class="sxs-lookup"><span data-stu-id="15291-114">Remarks</span></span>

<span data-ttu-id="15291-115">Lors de la lecture ou de l’écriture de données XML pour une tâche, la limite de démarrage du déclencheur est spécifiée dans l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="15291-115">When reading or writing XML for a task, the trigger start boundary is specified in the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="15291-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15291-116">Requirements</span></span>



| <span data-ttu-id="15291-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15291-117">Requirement</span></span> | <span data-ttu-id="15291-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="15291-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15291-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15291-119">Minimum supported client</span></span><br/> | <span data-ttu-id="15291-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15291-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="15291-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15291-121">Minimum supported server</span></span><br/> | <span data-ttu-id="15291-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15291-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15291-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="15291-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="15291-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15291-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15291-125">DLL</span><span class="sxs-lookup"><span data-stu-id="15291-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15291-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15291-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15291-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15291-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15291-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="15291-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





