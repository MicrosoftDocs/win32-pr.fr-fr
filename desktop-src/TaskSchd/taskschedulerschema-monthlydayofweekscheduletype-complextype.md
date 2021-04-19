---
title: Type complexe monthlyDayOfWeekScheduleType
description: Définit les éléments enfants et les informations de séquencement pour l’élément ScheduleByMonthDayOfWeek.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- Planificateur de tâches de type complexe monthlyDayOfWeekScheduleType
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543057"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a><span data-ttu-id="46aa7-104">Type complexe monthlyDayOfWeekScheduleType</span><span class="sxs-lookup"><span data-stu-id="46aa7-104">monthlyDayOfWeekScheduleType Complex Type</span></span>

<span data-ttu-id="46aa7-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="46aa7-105">Defines the child elements and sequencing information for the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="46aa7-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="46aa7-106">Child elements</span></span>



| <span data-ttu-id="46aa7-107">Élément</span><span class="sxs-lookup"><span data-stu-id="46aa7-107">Element</span></span>                                                                                   | <span data-ttu-id="46aa7-108">Type</span><span class="sxs-lookup"><span data-stu-id="46aa7-108">Type</span></span>                                                                     | <span data-ttu-id="46aa7-109">Description</span><span class="sxs-lookup"><span data-stu-id="46aa7-109">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="46aa7-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="46aa7-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="46aa7-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="46aa7-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="46aa7-112">Spécifie les jours de la semaine pendant lesquels la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="46aa7-112">Specifies the days of the week during which the task runs.</span></span><br/>   |
| [<span data-ttu-id="46aa7-113">**Suivent**</span><span class="sxs-lookup"><span data-stu-id="46aa7-113">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="46aa7-114">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="46aa7-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="46aa7-115">Spécifie les mois de l’année pendant laquelle la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="46aa7-115">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="46aa7-116">**Semaines**</span><span class="sxs-lookup"><span data-stu-id="46aa7-116">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [<span data-ttu-id="46aa7-117">**weeksType**</span><span class="sxs-lookup"><span data-stu-id="46aa7-117">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)           | <span data-ttu-id="46aa7-118">Spécifie les semaines du mois pendant lequel la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="46aa7-118">Specifies the weeks of the month during which the task runs.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="46aa7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46aa7-119">Requirements</span></span>



| <span data-ttu-id="46aa7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46aa7-120">Requirement</span></span> | <span data-ttu-id="46aa7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="46aa7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46aa7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46aa7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="46aa7-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46aa7-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46aa7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46aa7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="46aa7-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46aa7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46aa7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46aa7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46aa7-127">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="46aa7-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="46aa7-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="46aa7-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





