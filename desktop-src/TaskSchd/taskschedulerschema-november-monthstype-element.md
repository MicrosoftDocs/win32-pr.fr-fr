---
title: Élément de novembre (monthsType)
description: Spécifie que la tâche s’exécute en novembre.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- Planificateur de tâches de l’élément de novembre
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536293"
---
# <a name="november-monthstype-element"></a><span data-ttu-id="71659-104">Élément de novembre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="71659-104">November (monthsType) Element</span></span>

<span data-ttu-id="71659-105">Spécifie que la tâche s’exécute en novembre.</span><span class="sxs-lookup"><span data-stu-id="71659-105">Specifies that the task runs in November.</span></span>

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="71659-106">L’élément **novembre** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="71659-106">The **November** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="71659-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="71659-107">Parent element</span></span>



| <span data-ttu-id="71659-108">Élément</span><span class="sxs-lookup"><span data-stu-id="71659-108">Element</span></span>                                                                                                          | <span data-ttu-id="71659-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="71659-109">Derived from</span></span>                                                     | <span data-ttu-id="71659-110">Description</span><span class="sxs-lookup"><span data-stu-id="71659-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71659-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="71659-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="71659-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="71659-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="71659-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="71659-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="71659-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="71659-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="71659-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="71659-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="71659-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="71659-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="71659-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="71659-117">Examples</span></span>

<span data-ttu-id="71659-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche en novembre.</span><span class="sxs-lookup"><span data-stu-id="71659-118">The following XML defines a months calendar that runs the task in November.</span></span>


```XML
<Months>
    <November/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="71659-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71659-119">Requirements</span></span>



| <span data-ttu-id="71659-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71659-120">Requirement</span></span> | <span data-ttu-id="71659-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="71659-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71659-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71659-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71659-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71659-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="71659-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71659-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71659-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71659-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71659-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71659-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71659-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="71659-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="71659-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="71659-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





