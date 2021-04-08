---
title: Élément d’août (monthsType)
description: Spécifie que la tâche s’exécute en août.
ms.assetid: cd7e528c-d482-4bb4-a31f-fccdb19a441b
keywords:
- Planificateur de tâches de l’élément d’août
topic_type:
- apiref
api_name:
- August
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4978ebd8f22da6e157461791c4c2000fce9db6ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843857"
---
# <a name="august-monthstype-element"></a><span data-ttu-id="5c00b-104">Élément d’août (monthsType)</span><span class="sxs-lookup"><span data-stu-id="5c00b-104">August (monthsType) Element</span></span>

<span data-ttu-id="5c00b-105">Spécifie que la tâche s’exécute en août.</span><span class="sxs-lookup"><span data-stu-id="5c00b-105">Specifies that the task runs in August.</span></span>

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="5c00b-106">L’élément d' **août** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5c00b-106">The **August** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5c00b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="5c00b-107">Parent element</span></span>



| <span data-ttu-id="5c00b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="5c00b-108">Element</span></span>                                                                                                          | <span data-ttu-id="5c00b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="5c00b-109">Derived from</span></span>                                                     | <span data-ttu-id="5c00b-110">Description</span><span class="sxs-lookup"><span data-stu-id="5c00b-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c00b-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="5c00b-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="5c00b-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="5c00b-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="5c00b-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="5c00b-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="5c00b-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="5c00b-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="5c00b-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="5c00b-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="5c00b-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="5c00b-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="5c00b-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="5c00b-117">Examples</span></span>

<span data-ttu-id="5c00b-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche en août.</span><span class="sxs-lookup"><span data-stu-id="5c00b-118">The following XML defines a months calendar that runs the task in August.</span></span>


```XML
<Months>
    <August/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="5c00b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c00b-119">Requirements</span></span>



| <span data-ttu-id="5c00b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c00b-120">Requirement</span></span> | <span data-ttu-id="5c00b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c00b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c00b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c00b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5c00b-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c00b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c00b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c00b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5c00b-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c00b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c00b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c00b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c00b-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5c00b-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5c00b-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5c00b-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





