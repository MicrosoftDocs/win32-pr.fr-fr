---
title: Élément de février (monthsType)
description: Spécifie que la tâche s’exécute en février.
ms.assetid: 871449f8-fa3a-4e1f-be36-bc5c98125721
keywords:
- Planificateur de tâches de l’élément de février
topic_type:
- apiref
api_name:
- February
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727751964bfb9a752eb1190f8c7d3a86de2a9413
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511799"
---
# <a name="february-monthstype-element"></a><span data-ttu-id="810d8-104">Élément de février (monthsType)</span><span class="sxs-lookup"><span data-stu-id="810d8-104">February (monthsType) Element</span></span>

<span data-ttu-id="810d8-105">Spécifie que la tâche s’exécute en février.</span><span class="sxs-lookup"><span data-stu-id="810d8-105">Specifies that the task runs in February.</span></span>

``` syntax
<xs:element name="February">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="810d8-106">L’élément de **février** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="810d8-106">The **February** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="810d8-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="810d8-107">Parent element</span></span>



| <span data-ttu-id="810d8-108">Élément</span><span class="sxs-lookup"><span data-stu-id="810d8-108">Element</span></span>                                                                                                          | <span data-ttu-id="810d8-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="810d8-109">Derived from</span></span>                                                     | <span data-ttu-id="810d8-110">Description</span><span class="sxs-lookup"><span data-stu-id="810d8-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="810d8-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="810d8-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="810d8-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="810d8-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="810d8-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="810d8-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="810d8-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="810d8-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="810d8-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="810d8-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="810d8-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="810d8-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="810d8-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="810d8-117">Examples</span></span>

<span data-ttu-id="810d8-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche en février.</span><span class="sxs-lookup"><span data-stu-id="810d8-118">The following XML defines a months calendar that runs the task in February.</span></span>


```XML
<Months>
    <February/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="810d8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="810d8-119">Requirements</span></span>



| <span data-ttu-id="810d8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="810d8-120">Requirement</span></span> | <span data-ttu-id="810d8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="810d8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="810d8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="810d8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="810d8-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="810d8-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="810d8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="810d8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="810d8-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="810d8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="810d8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="810d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810d8-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="810d8-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="810d8-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="810d8-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





