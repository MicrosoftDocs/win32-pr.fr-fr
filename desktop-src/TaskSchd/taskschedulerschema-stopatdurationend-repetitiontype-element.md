---
title: Élément StopAtDurationEnd (repetitionType)
description: Spécifie qu’une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Élément StopAtDurationEnd Planificateur de tâches
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538614"
---
# <a name="stopatdurationend-repetitiontype-element"></a><span data-ttu-id="f5a41-104">Élément StopAtDurationEnd (repetitionType)</span><span class="sxs-lookup"><span data-stu-id="f5a41-104">StopAtDurationEnd (repetitionType) Element</span></span>

<span data-ttu-id="f5a41-105">Spécifie qu’une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.</span><span class="sxs-lookup"><span data-stu-id="f5a41-105">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span> <span data-ttu-id="f5a41-106">Cela s’applique uniquement si des répétitions sont définies.</span><span class="sxs-lookup"><span data-stu-id="f5a41-106">This is applicable only if repetitions are set.</span></span>

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

<span data-ttu-id="f5a41-107">L’élément **StopAtDurationEnd** est défini par le type complexe [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f5a41-107">The **StopAtDurationEnd** element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f5a41-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f5a41-108">Parent element</span></span>

| <span data-ttu-id="f5a41-109">Élément</span><span class="sxs-lookup"><span data-stu-id="f5a41-109">Element</span></span> | <span data-ttu-id="f5a41-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f5a41-110">Derived from</span></span> | <span data-ttu-id="f5a41-111">Description</span><span class="sxs-lookup"><span data-stu-id="f5a41-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="f5a41-112">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="f5a41-112">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="f5a41-113">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="f5a41-113">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="f5a41-114">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f5a41-114">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="f5a41-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f5a41-115">Remarks</span></span>

<span data-ttu-id="f5a41-116">Pour le développement de script, ce paramètre est spécifié à l’aide de la propriété [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) .</span><span class="sxs-lookup"><span data-stu-id="f5a41-116">For scripting development, this setting is specified using the [**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) property.</span></span>

<span data-ttu-id="f5a41-117">Pour le développement C++, ce paramètre est spécifié à l’aide de la propriété [**IRepetitionPattern :: StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .</span><span class="sxs-lookup"><span data-stu-id="f5a41-117">For C++ development, this setting is specified using the [**IRepetitionPattern::StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a41-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5a41-118">Requirements</span></span>

| <span data-ttu-id="f5a41-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5a41-119">Requirement</span></span> | <span data-ttu-id="f5a41-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5a41-120">Value</span></span> |
|-|-|
| <span data-ttu-id="f5a41-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5a41-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a41-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5a41-122">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f5a41-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5a41-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a41-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5a41-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="f5a41-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5a41-125">See also</span></span>

[<span data-ttu-id="f5a41-126">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f5a41-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="f5a41-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f5a41-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
