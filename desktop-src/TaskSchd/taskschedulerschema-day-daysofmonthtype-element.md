---
title: Élément Day (daysOfMonthType)
description: Spécifie un jour du mois pendant lequel la tâche s’exécute.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Jour, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032588"
---
# <a name="day-daysofmonthtype-element"></a><span data-ttu-id="e97d7-104">Élément Day (daysOfMonthType)</span><span class="sxs-lookup"><span data-stu-id="e97d7-104">Day (daysOfMonthType) Element</span></span>

<span data-ttu-id="e97d7-105">Spécifie un jour du mois pendant lequel la tâche s’exécute.</span><span class="sxs-lookup"><span data-stu-id="e97d7-105">Specifies a day of the month during which the task runs.</span></span>

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

<span data-ttu-id="e97d7-106">L’élément **Day** est défini par le type complexe [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e97d7-106">The **Day** element is defined by the [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e97d7-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e97d7-107">Parent element</span></span>



| <span data-ttu-id="e97d7-108">Élément</span><span class="sxs-lookup"><span data-stu-id="e97d7-108">Element</span></span>                                                                            | <span data-ttu-id="e97d7-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="e97d7-109">Derived from</span></span>                                                               | <span data-ttu-id="e97d7-110">Description</span><span class="sxs-lookup"><span data-stu-id="e97d7-110">Description</span></span>                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="e97d7-111">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="e97d7-111">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="e97d7-112">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="e97d7-112">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="e97d7-113">Spécifie les jours du mois pendant lesquels la tâche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="e97d7-113">Specifies the days of the month during which the task runs.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="e97d7-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="e97d7-114">Examples</span></span>

<span data-ttu-id="e97d7-115">Le code XML suivant définit la partie jours d’un calendrier mensuel qui exécute la tâche le 1er et le quinzième jour du mois.</span><span class="sxs-lookup"><span data-stu-id="e97d7-115">The following XML defines the days portion of a monthly calendar that runs the task on the 1st and 15th day of the month.</span></span>


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a><span data-ttu-id="e97d7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e97d7-116">Requirements</span></span>



| <span data-ttu-id="e97d7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e97d7-117">Requirement</span></span> | <span data-ttu-id="e97d7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e97d7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e97d7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e97d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e97d7-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e97d7-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e97d7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e97d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e97d7-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e97d7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e97d7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e97d7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e97d7-124">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e97d7-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





