---
title: Type complexe daysOfMonthType
description: Définit l’élément enfant et les informations de séquencement pour l’élément DaysOfMonth (monthlyScheduleType).
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- Planificateur de tâches de type complexe daysOfMonthType
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385072"
---
# <a name="daysofmonthtype-complex-type"></a><span data-ttu-id="a1860-104">Type complexe daysOfMonthType</span><span class="sxs-lookup"><span data-stu-id="a1860-104">daysOfMonthType Complex Type</span></span>

<span data-ttu-id="a1860-105">Définit l’élément enfant et les informations de séquencement pour l’élément [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a1860-105">Defines the child element and sequencing information for the [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element.</span></span>

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a1860-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a1860-106">Child elements</span></span>



| <span data-ttu-id="a1860-107">Élément</span><span class="sxs-lookup"><span data-stu-id="a1860-107">Element</span></span>                                                        | <span data-ttu-id="a1860-108">Type</span><span class="sxs-lookup"><span data-stu-id="a1860-108">Type</span></span>                                                                    | <span data-ttu-id="a1860-109">Description</span><span class="sxs-lookup"><span data-stu-id="a1860-109">Description</span></span>                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="a1860-110">**Temps**</span><span class="sxs-lookup"><span data-stu-id="a1860-110">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="a1860-111">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="a1860-111">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="a1860-112">Spécifie un jour du mois pendant lequel la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="a1860-112">Specifies a day of the month during which the task runs.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="a1860-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1860-113">Requirements</span></span>



| <span data-ttu-id="a1860-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1860-114">Requirement</span></span> | <span data-ttu-id="a1860-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1860-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1860-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1860-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1860-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1860-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1860-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1860-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1860-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1860-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1860-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1860-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1860-121">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a1860-121">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a1860-122">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a1860-122">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





