---
title: Élément de juin (monthsType)
description: Spécifie que la tâche s’exécute en juin.
ms.assetid: 15b0e8c2-4dc1-4ca3-99c5-bd9a36718904
keywords:
- Planificateur de tâches de l’élément juin
topic_type:
- apiref
api_name:
- June
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e6c21834348a70033af69a71534c60c1b08d91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742421"
---
# <a name="june-monthstype-element"></a><span data-ttu-id="de169-104">Élément de juin (monthsType)</span><span class="sxs-lookup"><span data-stu-id="de169-104">June (monthsType) Element</span></span>

<span data-ttu-id="de169-105">Spécifie que la tâche s’exécute en juin.</span><span class="sxs-lookup"><span data-stu-id="de169-105">Specifies that the task runs in June.</span></span>

``` syntax
<xs:element name="June">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="de169-106">L’élément **juin** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="de169-106">The **June** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="de169-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="de169-107">Parent element</span></span>



| <span data-ttu-id="de169-108">Élément</span><span class="sxs-lookup"><span data-stu-id="de169-108">Element</span></span>                                                                                                          | <span data-ttu-id="de169-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="de169-109">Derived from</span></span>                                                     | <span data-ttu-id="de169-110">Description</span><span class="sxs-lookup"><span data-stu-id="de169-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de169-111">**Mois (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="de169-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="de169-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="de169-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="de169-113">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.</span><span class="sxs-lookup"><span data-stu-id="de169-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="de169-114">**Mois (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="de169-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="de169-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="de169-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="de169-116">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="de169-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="de169-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="de169-117">Examples</span></span>

<span data-ttu-id="de169-118">Le code XML suivant définit un calendrier de mois qui exécute la tâche en juin.</span><span class="sxs-lookup"><span data-stu-id="de169-118">The following XML defines a months calendar that runs the task in June.</span></span>


```XML
<Months>
    <June/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="de169-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de169-119">Requirements</span></span>



| <span data-ttu-id="de169-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de169-120">Requirement</span></span> | <span data-ttu-id="de169-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="de169-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de169-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de169-122">Minimum supported client</span></span><br/> | <span data-ttu-id="de169-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de169-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="de169-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de169-124">Minimum supported server</span></span><br/> | <span data-ttu-id="de169-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de169-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de169-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de169-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de169-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="de169-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="de169-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="de169-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





