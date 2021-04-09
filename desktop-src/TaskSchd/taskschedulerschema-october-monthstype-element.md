---
title: Élément d’octobre (monthsType)
description: Spécifie que la tâche s’exécute en octobre.
ms.assetid: 62c8bb3e-a70f-45b8-8d80-7a7eef9dfaeb
keywords:
- Planificateur de tâches de l’élément octobre
topic_type:
- apiref
api_name:
- October
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79bf2a2dde46341f48808342ab6aefb78863524b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106360"
---
# <a name="october-monthstype-element"></a><span data-ttu-id="76375-104">Élément d’octobre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="76375-104">October (monthsType) Element</span></span>

<span data-ttu-id="76375-105">Spécifie que la tâche s’exécute en octobre.</span><span class="sxs-lookup"><span data-stu-id="76375-105">Specifies that the task runs in October.</span></span>

``` syntax
<xs:element name="October">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="76375-106">L’élément **octobre** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="76375-106">The **October** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="76375-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="76375-107">Parent element</span></span>



| <span data-ttu-id="76375-108">Élément</span><span class="sxs-lookup"><span data-stu-id="76375-108">Element</span></span>                                                                                                          | <span data-ttu-id="76375-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="76375-109">Derived from</span></span>                                                     | <span data-ttu-id="76375-110">Description</span><span class="sxs-lookup"><span data-stu-id="76375-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76375-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="76375-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="76375-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="76375-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="76375-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="76375-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="76375-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="76375-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="76375-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="76375-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="76375-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="76375-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="76375-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="76375-117">Examples</span></span>

<span data-ttu-id="76375-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche en octobre.</span><span class="sxs-lookup"><span data-stu-id="76375-118">The following XML defines a months calendar that runs the task in October.</span></span>


```XML
<Months>
    <October/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="76375-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76375-119">Requirements</span></span>



| <span data-ttu-id="76375-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76375-120">Requirement</span></span> | <span data-ttu-id="76375-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="76375-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76375-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76375-122">Minimum supported client</span></span><br/> | <span data-ttu-id="76375-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76375-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76375-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76375-124">Minimum supported server</span></span><br/> | <span data-ttu-id="76375-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76375-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76375-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76375-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76375-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="76375-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="76375-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="76375-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





