---
title: Type complexe monthsType
description: Définit les éléments enfants et les informations de séquencement pour les éléments months (monthlyDayOfWeekScheduleType) et months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- Planificateur de tâches de type complexe monthsType
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740437"
---
# <a name="monthstype-complex-type"></a><span data-ttu-id="b3fe2-104">Type complexe monthsType</span><span class="sxs-lookup"><span data-stu-id="b3fe2-104">monthsType Complex Type</span></span>

<span data-ttu-id="b3fe2-105">Définit les éléments enfants et les informations de séquencement pour les éléments [**months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) et [**months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b3fe2-105">Defines the child elements and sequencing information for the [**Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) and [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md) elements.</span></span>

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b3fe2-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b3fe2-106">Child elements</span></span>



| <span data-ttu-id="b3fe2-107">Élément</span><span class="sxs-lookup"><span data-stu-id="b3fe2-107">Element</span></span>                                                               | <span data-ttu-id="b3fe2-108">Type</span><span class="sxs-lookup"><span data-stu-id="b3fe2-108">Type</span></span> | <span data-ttu-id="b3fe2-109">Description</span><span class="sxs-lookup"><span data-stu-id="b3fe2-109">Description</span></span>                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [<span data-ttu-id="b3fe2-110">**Avril**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-110">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         | <span data-ttu-id="b3fe2-111">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-111">N/A</span></span>  | <span data-ttu-id="b3fe2-112">Spécifie que la tâche s’exécute en avril.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-112">Specifies that the task runs in April.</span></span> <br/>     |
| [<span data-ttu-id="b3fe2-113">**Août**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-113">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       | <span data-ttu-id="b3fe2-114">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-114">N/A</span></span>  | <span data-ttu-id="b3fe2-115">Spécifie que la tâche s’exécute en août.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-115">Specifies that the task runs in August.</span></span> <br/>    |
| [<span data-ttu-id="b3fe2-116">**Décembre**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-116">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   | <span data-ttu-id="b3fe2-117">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-117">N/A</span></span>  | <span data-ttu-id="b3fe2-118">Spécifie que la tâche s’exécute en décembre.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-118">Specifies that the task runs in December.</span></span> <br/>  |
| [<span data-ttu-id="b3fe2-119">**February**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-119">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   | <span data-ttu-id="b3fe2-120">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-120">N/A</span></span>  | <span data-ttu-id="b3fe2-121">Spécifie que la tâche s’exécute en février.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-121">Specifies that the task runs in February.</span></span> <br/>  |
| [<span data-ttu-id="b3fe2-122">**Janvier**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-122">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     | <span data-ttu-id="b3fe2-123">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-123">N/A</span></span>  | <span data-ttu-id="b3fe2-124">Spécifie que la tâche s’exécute en janvier.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-124">Specifies that the task runs in January.</span></span> <br/>   |
| [<span data-ttu-id="b3fe2-125">**Juillet**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-125">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           | <span data-ttu-id="b3fe2-126">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-126">N/A</span></span>  | <span data-ttu-id="b3fe2-127">Spécifie que la tâche s’exécute en juillet.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-127">Specifies that the task runs in July.</span></span> <br/>      |
| [<span data-ttu-id="b3fe2-128">**June**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-128">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           | <span data-ttu-id="b3fe2-129">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-129">N/A</span></span>  | <span data-ttu-id="b3fe2-130">Spécifie que la tâche s’exécute en juin.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-130">Specifies that the task runs in June.</span></span> <br/>      |
| [<span data-ttu-id="b3fe2-131">**Mars**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-131">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         | <span data-ttu-id="b3fe2-132">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-132">N/A</span></span>  | <span data-ttu-id="b3fe2-133">Spécifie que la tâche s’exécute en mars.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-133">Specifies that the task runs in March.</span></span> <br/>     |
| [<span data-ttu-id="b3fe2-134">**Mai**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             | <span data-ttu-id="b3fe2-135">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-135">N/A</span></span>  | <span data-ttu-id="b3fe2-136">Spécifie que la tâche s’exécute en mai.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-136">Specifies that the task runs in May.</span></span> <br/>       |
| [<span data-ttu-id="b3fe2-137">**Novembre**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-137">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   | <span data-ttu-id="b3fe2-138">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-138">N/A</span></span>  | <span data-ttu-id="b3fe2-139">Spécifie que la tâche s’exécute en novembre.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-139">Specifies that the task runs in November.</span></span> <br/>  |
| [<span data-ttu-id="b3fe2-140">**Octobre**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-140">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     | <span data-ttu-id="b3fe2-141">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-141">N/A</span></span>  | <span data-ttu-id="b3fe2-142">Spécifie que la tâche s’exécute en octobre.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-142">Specifies that the task runs in October.</span></span> <br/>   |
| [<span data-ttu-id="b3fe2-143">**Septembre**</span><span class="sxs-lookup"><span data-stu-id="b3fe2-143">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) | <span data-ttu-id="b3fe2-144">N/A</span><span class="sxs-lookup"><span data-stu-id="b3fe2-144">N/A</span></span>  | <span data-ttu-id="b3fe2-145">Spécifie que la tâche s’exécute en septembre.</span><span class="sxs-lookup"><span data-stu-id="b3fe2-145">Specifies that the task runs in September.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="b3fe2-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3fe2-146">Requirements</span></span>



| <span data-ttu-id="b3fe2-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3fe2-147">Requirement</span></span> | <span data-ttu-id="b3fe2-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3fe2-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3fe2-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3fe2-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b3fe2-150">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3fe2-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3fe2-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3fe2-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b3fe2-152">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3fe2-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3fe2-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3fe2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3fe2-154">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b3fe2-154">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b3fe2-155">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b3fe2-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





