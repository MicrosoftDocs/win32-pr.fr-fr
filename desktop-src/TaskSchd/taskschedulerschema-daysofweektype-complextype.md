---
title: Type complexe daysOfWeekType
description: Définit les éléments enfants et les informations de séquencement pour les éléments DaysOfWeek (weeklyScheduleType) et DaysOfWeek (monthlyDayOfWeekScheduleType).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- Planificateur de tâches de type complexe daysOfWeekType
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317510"
---
# <a name="daysofweektype-complex-type"></a><span data-ttu-id="8774e-104">Type complexe daysOfWeekType</span><span class="sxs-lookup"><span data-stu-id="8774e-104">daysOfWeekType Complex Type</span></span>

<span data-ttu-id="8774e-105">Définit les éléments enfants et les informations de séquencement pour les éléments [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) et [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8774e-105">Defines the child elements and sequencing information for the [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) and [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8774e-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8774e-106">Child elements</span></span>



| <span data-ttu-id="8774e-107">Élément</span><span class="sxs-lookup"><span data-stu-id="8774e-107">Element</span></span>                                                                   | <span data-ttu-id="8774e-108">Type</span><span class="sxs-lookup"><span data-stu-id="8774e-108">Type</span></span> | <span data-ttu-id="8774e-109">Description</span><span class="sxs-lookup"><span data-stu-id="8774e-109">Description</span></span>                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [<span data-ttu-id="8774e-110">**Vendredi**</span><span class="sxs-lookup"><span data-stu-id="8774e-110">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       | <span data-ttu-id="8774e-111">N/A</span><span class="sxs-lookup"><span data-stu-id="8774e-111">N/A</span></span>  | <span data-ttu-id="8774e-112">La tâche est exécutée le vendredi.</span><span class="sxs-lookup"><span data-stu-id="8774e-112">Task runs on Friday.</span></span> <br/>    |
| [<span data-ttu-id="8774e-113">**Monday**</span><span class="sxs-lookup"><span data-stu-id="8774e-113">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       | <span data-ttu-id="8774e-114">N/A</span><span class="sxs-lookup"><span data-stu-id="8774e-114">N/A</span></span>  | <span data-ttu-id="8774e-115">La tâche est exécutée le lundi.</span><span class="sxs-lookup"><span data-stu-id="8774e-115">Task runs on Monday.</span></span><br/>     |
| [<span data-ttu-id="8774e-116">**Samedi**</span><span class="sxs-lookup"><span data-stu-id="8774e-116">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   | <span data-ttu-id="8774e-117">N/A</span><span class="sxs-lookup"><span data-stu-id="8774e-117">N/A</span></span>  | <span data-ttu-id="8774e-118">La tâche est exécutée le samedi.</span><span class="sxs-lookup"><span data-stu-id="8774e-118">Task runs on Saturday.</span></span> <br/>  |
| [<span data-ttu-id="8774e-119">**Dimanche**</span><span class="sxs-lookup"><span data-stu-id="8774e-119">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       | <span data-ttu-id="8774e-120">N/A</span><span class="sxs-lookup"><span data-stu-id="8774e-120">N/A</span></span>  | <span data-ttu-id="8774e-121">La tâche est exécutée le dimanche.</span><span class="sxs-lookup"><span data-stu-id="8774e-121">Task runs on Sunday.</span></span> <br/>    |
| [<span data-ttu-id="8774e-122">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="8774e-122">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   | <span data-ttu-id="8774e-123">N/A</span><span class="sxs-lookup"><span data-stu-id="8774e-123">N/A</span></span>  | <span data-ttu-id="8774e-124">Tâche exécutée le jeudi</span><span class="sxs-lookup"><span data-stu-id="8774e-124">Task runs on Thursday</span></span> <br/>   |
| [<span data-ttu-id="8774e-125">**Mardi**</span><span class="sxs-lookup"><span data-stu-id="8774e-125">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     | <span data-ttu-id="8774e-126">N/A</span><span class="sxs-lookup"><span data-stu-id="8774e-126">N/A</span></span>  | <span data-ttu-id="8774e-127">La tâche est exécutée le mardi.</span><span class="sxs-lookup"><span data-stu-id="8774e-127">Task runs on Tuesday.</span></span> <br/>   |
| [<span data-ttu-id="8774e-128">**Mercredi**</span><span class="sxs-lookup"><span data-stu-id="8774e-128">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) | <span data-ttu-id="8774e-129">N/A</span><span class="sxs-lookup"><span data-stu-id="8774e-129">N/A</span></span>  | <span data-ttu-id="8774e-130">La tâche est exécutée le mercredi.</span><span class="sxs-lookup"><span data-stu-id="8774e-130">Task runs on Wednesday.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="8774e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8774e-131">Requirements</span></span>



| <span data-ttu-id="8774e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8774e-132">Requirement</span></span> | <span data-ttu-id="8774e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8774e-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8774e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8774e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8774e-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8774e-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8774e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8774e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8774e-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8774e-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8774e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8774e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8774e-139">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8774e-139">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8774e-140">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="8774e-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





