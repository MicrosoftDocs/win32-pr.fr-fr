---
title: Structures de déclencheur pour Planificateur de tâches 1,0
description: Planificateur de tâches 1,0 utilise plusieurs structures pour définir les critères d’un déclencheur.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029342"
---
# <a name="trigger-structures-for-task-scheduler-10"></a><span data-ttu-id="faf16-103">Structures de déclencheur pour Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="faf16-103">Trigger Structures for Task Scheduler 1.0</span></span>

<span data-ttu-id="faf16-104">Planificateur de tâches 1,0 utilise plusieurs structures pour définir les critères d’un déclencheur.</span><span class="sxs-lookup"><span data-stu-id="faf16-104">Task Scheduler 1.0 uses several structures to define the criteria of a trigger.</span></span>

> [!Note]  
> <span data-ttu-id="faf16-105">Pour plus d’informations sur les déclencheurs Planificateur de tâches 2,0, consultez [interfaces de déclencheur](trigger-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="faf16-105">For more information about Task Scheduler 2.0 triggers, see [Trigger Interfaces](trigger-interfaces.md).</span></span>

 

## <a name="task-scheduler-10-structures"></a><span data-ttu-id="faf16-106">Structures Planificateur de tâches 1,0</span><span class="sxs-lookup"><span data-stu-id="faf16-106">Task Scheduler 1.0 Structures</span></span>

<span data-ttu-id="faf16-107">L’illustration suivante montre la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="faf16-107">The following illustration shows the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="faf16-108">Il a trois membres requis (**wBeginYear**, **wBeginMonth** et **wBeginDay**) qui doivent être définis lors de la création d’un nouveau déclencheur.</span><span class="sxs-lookup"><span data-stu-id="faf16-108">It has three required members (**wBeginYear**, **wBeginMonth**, and **wBeginDay**) that must be set when creating a new trigger.</span></span> <span data-ttu-id="faf16-109">(Pour accéder à la page de référence de cette structure, cliquez sur le nom de la structure dans l’illustration.)</span><span class="sxs-lookup"><span data-stu-id="faf16-109">(To jump to the reference page for this structure, click the structure name in the illustration.)</span></span>

![structure de déclencheur de tâche](images/tsktri1.png)

<span data-ttu-id="faf16-111">Sachez que le membre **TriggerType** utilise l’énumération de [**\_ \_ type de déclencheur de tâche**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) et que le membre de **type** utilise une structure d' **\_ \_ Union de déclencheur de tâche** .</span><span class="sxs-lookup"><span data-stu-id="faf16-111">Be aware that the **TriggerType** member uses the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the **Type** member uses a **TASK\_TRIGGER\_UNION** structure.</span></span> <span data-ttu-id="faf16-112">L’énumération des types de **\_ \_ déclencheurs de tâches** permet de spécifier le type de déclencheur (types de déclencheurs basés sur les événements et les temps).</span><span class="sxs-lookup"><span data-stu-id="faf16-112">The **TASK\_TRIGGER\_TYPE** enumeration is used to specify the type of trigger (event and time-based trigger types).</span></span> <span data-ttu-id="faf16-113">La structure d' [**\_ \_ Union de type de déclencheur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) est utilisée pour combiner les structures [**quotidienne**](/windows/desktop/api/Mstask/ns-mstask-daily), [**hebdomadaire**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (jour du mois) et [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (jour de la semaine) utilisées pour spécifier quand un déclencheur basé sur l’heure sera activé.</span><span class="sxs-lookup"><span data-stu-id="faf16-113">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used to combine the [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (day of month), and [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (day of week) structures that are used to specify when a time-based trigger will fire.</span></span>

<span data-ttu-id="faf16-114">Si **TriggerType** spécifie un déclencheur basé sur une heure ou un déclencheur basé sur les événements, le membre de **type** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="faf16-114">If **TriggerType** specifies a one-time time-based trigger or an event-based trigger, the **Type** member is ignored.</span></span> <span data-ttu-id="faf16-115">La structure d' [**\_ \_ Union de type de déclencheur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) est utilisée uniquement si le membre **TriggerType** spécifie un déclencheur basé sur le temps quotidien, hebdomadaire, quotidien ou mensuel.</span><span class="sxs-lookup"><span data-stu-id="faf16-115">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used only if the **TriggerType** member specifies a daily, weekly, day-of-month, or monthly day-of-week time-based trigger.</span></span>

<span data-ttu-id="faf16-116">En outre, le paramètre du membre de **type** indique quel membre de la structure d' [**\_ \_ Union de type de déclencheur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="faf16-116">In addition, the setting of the **Type** member indicates which member of the [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used.</span></span> <span data-ttu-id="faf16-117">L’illustration suivante montre la relation entre les valeurs de l’énumération de [**\_ \_ type de déclencheur de tâche**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) et les membres de la structure de la **structure de \_ type \_ de déclencheur** .</span><span class="sxs-lookup"><span data-stu-id="faf16-117">The following illustration shows the relationship between the values of the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the members of the **TRIGGER\_TYPE\_STRUCTURE** structure.</span></span> <span data-ttu-id="faf16-118">(Pour accéder aux pages de référence de ces structures, cliquez sur le nom de la structure dans l’illustration.)</span><span class="sxs-lookup"><span data-stu-id="faf16-118">(To jump to the reference pages for these structures click the structure name in the illustration.)</span></span>

![relation entre les valeurs d’énumération de type de déclencheur de tâche et les membres de la structure de structure de type de déclencheur](images/tsktri3.png)

## <a name="related-topics"></a><span data-ttu-id="faf16-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="faf16-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faf16-121">Déclencheurs de tâche</span><span class="sxs-lookup"><span data-stu-id="faf16-121">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="faf16-122">Types de déclencheurs</span><span class="sxs-lookup"><span data-stu-id="faf16-122">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="faf16-123">Interfaces de déclencheur</span><span class="sxs-lookup"><span data-stu-id="faf16-123">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> </dl>

 

 




