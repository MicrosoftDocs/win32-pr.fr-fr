---
title: Élément de septembre (monthsType)
description: Spécifie que la tâche s’exécute en septembre.
ms.assetid: b1ad2221-ca22-4808-bf20-ecf3cbb930f2
keywords:
- Planificateur de tâches de l’élément de septembre
topic_type:
- apiref
api_name:
- September
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd7e18ba9ae1cc7653589710fb9529281e84ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942730"
---
# <a name="september-monthstype-element"></a><span data-ttu-id="be6e1-104">Élément de septembre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="be6e1-104">September (monthsType) Element</span></span>

<span data-ttu-id="be6e1-105">Spécifie que la tâche s’exécute en septembre.</span><span class="sxs-lookup"><span data-stu-id="be6e1-105">Specifies that the task runs in September.</span></span>

``` syntax
<xs:element name="September">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="be6e1-106">L’élément **septembre** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="be6e1-106">The **September** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="be6e1-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="be6e1-107">Parent element</span></span>



| <span data-ttu-id="be6e1-108">Élément</span><span class="sxs-lookup"><span data-stu-id="be6e1-108">Element</span></span>                                                                                                          | <span data-ttu-id="be6e1-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="be6e1-109">Derived from</span></span>                                                     | <span data-ttu-id="be6e1-110">Description</span><span class="sxs-lookup"><span data-stu-id="be6e1-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be6e1-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="be6e1-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="be6e1-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="be6e1-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="be6e1-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="be6e1-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="be6e1-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="be6e1-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="be6e1-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="be6e1-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="be6e1-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="be6e1-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="be6e1-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="be6e1-117">Examples</span></span>

<span data-ttu-id="be6e1-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche en septembre.</span><span class="sxs-lookup"><span data-stu-id="be6e1-118">The following XML defines a months calendar that runs the task in September.</span></span>


```XML
<Months>
    <September/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="be6e1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be6e1-119">Requirements</span></span>



| <span data-ttu-id="be6e1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be6e1-120">Requirement</span></span> | <span data-ttu-id="be6e1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="be6e1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="be6e1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be6e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="be6e1-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be6e1-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="be6e1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be6e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="be6e1-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be6e1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be6e1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be6e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6e1-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="be6e1-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="be6e1-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="be6e1-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





