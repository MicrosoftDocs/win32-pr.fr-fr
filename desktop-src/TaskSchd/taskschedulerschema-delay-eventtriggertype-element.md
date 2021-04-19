---
title: Élément Delay (eventTriggerType)
description: Spécifie la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Retarder l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517333"
---
# <a name="delay-eventtriggertype-element"></a><span data-ttu-id="c7aed-104">Élément Delay (eventTriggerType)</span><span class="sxs-lookup"><span data-stu-id="c7aed-104">Delay (eventTriggerType) Element</span></span>

<span data-ttu-id="c7aed-105">Spécifie la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.</span><span class="sxs-lookup"><span data-stu-id="c7aed-105">Specifies the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="c7aed-106">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="c7aed-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="c7aed-107">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="c7aed-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="c7aed-108">L’élément **delay** est défini par le type complexe [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c7aed-108">The **Delay** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c7aed-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c7aed-109">Parent element</span></span>



| <span data-ttu-id="c7aed-110">Élément</span><span class="sxs-lookup"><span data-stu-id="c7aed-110">Element</span></span>                                                                       | <span data-ttu-id="c7aed-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c7aed-111">Derived from</span></span>                                                                 | <span data-ttu-id="c7aed-112">Description</span><span class="sxs-lookup"><span data-stu-id="c7aed-112">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="c7aed-113">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="c7aed-113">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="c7aed-114">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="c7aed-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="c7aed-115">Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.</span><span class="sxs-lookup"><span data-stu-id="c7aed-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c7aed-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c7aed-116">Remarks</span></span>

<span data-ttu-id="c7aed-117">Pour le développement de scripts, le délai de déclenchement des événements est spécifié par la propriété [**EventTrigger. Delay**](eventtrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="c7aed-117">For script development, the event trigger delay is specified by the [**EventTrigger.Delay**](eventtrigger-delay.md) property.</span></span>

<span data-ttu-id="c7aed-118">Pour le développement C++, le délai de déclenchement des événements est spécifié par la propriété [**IEventTrigger ::D Nouv**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="c7aed-118">For C++ development, the event trigger delay is specified by the [**IEventTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7aed-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7aed-119">Requirements</span></span>



| <span data-ttu-id="c7aed-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7aed-120">Requirement</span></span> | <span data-ttu-id="c7aed-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7aed-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c7aed-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7aed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7aed-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7aed-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c7aed-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7aed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7aed-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7aed-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7aed-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7aed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7aed-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c7aed-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c7aed-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c7aed-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





