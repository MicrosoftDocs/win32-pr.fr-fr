---
title: Type complexe monthlyScheduleType
description: Définit les éléments enfants et les informations de séquencement pour l’élément ScheduleByMonth (calendarTriggerType).
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- Planificateur de tâches de type complexe monthlyScheduleType
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c2fafe2b05a01380c13aae2ab7cb3ddaa5330
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509307"
---
# <a name="monthlyscheduletype-complex-type"></a><span data-ttu-id="b6b86-104">Type complexe monthlyScheduleType</span><span class="sxs-lookup"><span data-stu-id="b6b86-104">monthlyScheduleType Complex Type</span></span>

<span data-ttu-id="b6b86-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b6b86-105">Defines the child elements and sequencing information for the [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b6b86-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b6b86-106">Child elements</span></span>



| <span data-ttu-id="b6b86-107">Élément</span><span class="sxs-lookup"><span data-stu-id="b6b86-107">Element</span></span>                                                                            | <span data-ttu-id="b6b86-108">Type</span><span class="sxs-lookup"><span data-stu-id="b6b86-108">Type</span></span>                                                                       | <span data-ttu-id="b6b86-109">Description</span><span class="sxs-lookup"><span data-stu-id="b6b86-109">Description</span></span>                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6b86-110">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="b6b86-110">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="b6b86-111">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="b6b86-111">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="b6b86-112">Spécifie les jours du mois pendant lesquels la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="b6b86-112">Specifies the days of the month during which the task runs.</span></span><br/>                         |
| [<span data-ttu-id="b6b86-113">**Suivent**</span><span class="sxs-lookup"><span data-stu-id="b6b86-113">**Months**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="b6b86-114">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="b6b86-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="b6b86-115">Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.</span><span class="sxs-lookup"><span data-stu-id="b6b86-115">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b6b86-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6b86-116">Requirements</span></span>



| <span data-ttu-id="b6b86-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6b86-117">Requirement</span></span> | <span data-ttu-id="b6b86-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6b86-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6b86-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6b86-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b86-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6b86-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6b86-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6b86-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b86-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6b86-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6b86-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6b86-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b86-124">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b6b86-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b6b86-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b6b86-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





