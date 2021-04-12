---
title: Type complexe weeklyScheduleType
description: Définit les éléments enfants et les informations de séquencement pour l’élément ScheduleByWeek.
ms.assetid: 048832fa-2262-4461-9cfc-823a4eb7a1df
keywords:
- Planificateur de tâches de type complexe weeklyScheduleType
topic_type:
- apiref
api_name:
- weeklyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 797e01c20e749593d64bad12f017af8be613992e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384348"
---
# <a name="weeklyscheduletype-complex-type"></a><span data-ttu-id="aa3f0-104">Type complexe weeklyScheduleType</span><span class="sxs-lookup"><span data-stu-id="aa3f0-104">weeklyScheduleType Complex Type</span></span>

<span data-ttu-id="aa3f0-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aa3f0-105">Defines the child elements and sequencing information for the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeklyScheduleType">
    <xs:all>
        <xs:element name="WeeksInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="52"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="aa3f0-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aa3f0-106">Child elements</span></span>



| <span data-ttu-id="aa3f0-107">Élément</span><span class="sxs-lookup"><span data-stu-id="aa3f0-107">Element</span></span>                                                                               | <span data-ttu-id="aa3f0-108">Type</span><span class="sxs-lookup"><span data-stu-id="aa3f0-108">Type</span></span>                                                                     | <span data-ttu-id="aa3f0-109">Description</span><span class="sxs-lookup"><span data-stu-id="aa3f0-109">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="aa3f0-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="aa3f0-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="aa3f0-111">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="aa3f0-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="aa3f0-112">Spécifie les jours de la semaine d’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="aa3f0-112">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="aa3f0-113">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="aa3f0-113">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) |                                                                          | <span data-ttu-id="aa3f0-114">Spécifie l’intervalle entre les semaines de la planification.</span><span class="sxs-lookup"><span data-stu-id="aa3f0-114">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="aa3f0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa3f0-115">Requirements</span></span>



| <span data-ttu-id="aa3f0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa3f0-116">Requirement</span></span> | <span data-ttu-id="aa3f0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa3f0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa3f0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa3f0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa3f0-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa3f0-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa3f0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa3f0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa3f0-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa3f0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa3f0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa3f0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa3f0-123">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="aa3f0-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





