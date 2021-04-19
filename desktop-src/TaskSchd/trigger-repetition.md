---
title: Déclencheur. rerépétition, propriété
description: Pour les scripts, obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Planificateur de tâches de la propriété de répétition
- Propriété de répétition Planificateur de tâches, objet déclencheur
- Planificateur de tâches de l’objet de déclencheur, propriété à répétition
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513589"
---
# <a name="triggerrepetition-property"></a><span data-ttu-id="4624c-106">Déclencheur. rerépétition, propriété</span><span class="sxs-lookup"><span data-stu-id="4624c-106">Trigger.Repetition property</span></span>

<span data-ttu-id="4624c-107">Pour les scripts, obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="4624c-107">For scripting, gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="4624c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4624c-108">Syntax</span></span>


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a><span data-ttu-id="4624c-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4624c-109">Property value</span></span>

<span data-ttu-id="4624c-110">Objet [**RepetitionPattern**](repetitionpattern.md) qui définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="4624c-110">A [**RepetitionPattern**](repetitionpattern.md) object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="4624c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4624c-111">Remarks</span></span>

<span data-ttu-id="4624c-112">Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, le modèle de répétition d’un déclencheur est spécifié dans l’élément de [**répétition**](taskschedulerschema-repetition-triggerbasetype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="4624c-112">When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4624c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4624c-113">Requirements</span></span>



| <span data-ttu-id="4624c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4624c-114">Requirement</span></span> | <span data-ttu-id="4624c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4624c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4624c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4624c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4624c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4624c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4624c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4624c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4624c-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4624c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4624c-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4624c-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="4624c-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4624c-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4624c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4624c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4624c-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4624c-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4624c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4624c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4624c-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4624c-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4624c-126">**RepetitionPattern**</span><span class="sxs-lookup"><span data-stu-id="4624c-126">**RepetitionPattern**</span></span>](repetitionpattern.md)
</dt> </dl>

 

 





