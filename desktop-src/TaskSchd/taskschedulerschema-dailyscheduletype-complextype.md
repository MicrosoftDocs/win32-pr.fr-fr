---
title: Type complexe dailyScheduleType
description: Définit les éléments enfants et les informations de séquencement pour l’élément ScheduleByDay.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- Planificateur de tâches de type complexe dailyScheduleType
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509122"
---
# <a name="dailyscheduletype-complex-type"></a><span data-ttu-id="af1aa-104">Type complexe dailyScheduleType</span><span class="sxs-lookup"><span data-stu-id="af1aa-104">dailyScheduleType Complex Type</span></span>

<span data-ttu-id="af1aa-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="af1aa-105">Defines the child elements and sequencing information for the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="af1aa-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="af1aa-106">Child elements</span></span>



| <span data-ttu-id="af1aa-107">Élément</span><span class="sxs-lookup"><span data-stu-id="af1aa-107">Element</span></span>                                                                            | <span data-ttu-id="af1aa-108">Type</span><span class="sxs-lookup"><span data-stu-id="af1aa-108">Type</span></span> | <span data-ttu-id="af1aa-109">Description</span><span class="sxs-lookup"><span data-stu-id="af1aa-109">Description</span></span>                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [<span data-ttu-id="af1aa-110">**DaysInterval**</span><span class="sxs-lookup"><span data-stu-id="af1aa-110">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | <span data-ttu-id="af1aa-111">Spécifie l’intervalle entre les jours de la planification.</span><span class="sxs-lookup"><span data-stu-id="af1aa-111">Specifies the interval between the days in the schedule.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="af1aa-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af1aa-112">Requirements</span></span>



| <span data-ttu-id="af1aa-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af1aa-113">Requirement</span></span> | <span data-ttu-id="af1aa-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="af1aa-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af1aa-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af1aa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="af1aa-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af1aa-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af1aa-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af1aa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="af1aa-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af1aa-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af1aa-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af1aa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1aa-120">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="af1aa-120">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="af1aa-121">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="af1aa-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





