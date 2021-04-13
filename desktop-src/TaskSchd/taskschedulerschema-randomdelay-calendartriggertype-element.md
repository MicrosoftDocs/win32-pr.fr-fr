---
title: Élément RandomDelay (calendarTriggerType)
description: Contient le délai d’attente ajouté de manière aléatoire à l’heure de début du déclencheur. | Élément RandomDelay (calendarTriggerType)
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
keywords:
- Élément RandomDelay Planificateur de tâches
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322329"
---
# <a name="randomdelay-calendartriggertype-element"></a><span data-ttu-id="ae377-105">Élément RandomDelay (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="ae377-105">RandomDelay (calendarTriggerType) Element</span></span>

<span data-ttu-id="ae377-106">Contient le délai d’attente ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="ae377-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="ae377-107">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="ae377-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="ae377-108">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="ae377-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="ae377-109">L’élément **RandomDelay** est défini par le type complexe [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae377-109">The **RandomDelay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ae377-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ae377-110">Parent element</span></span>



| <span data-ttu-id="ae377-111">Élément</span><span class="sxs-lookup"><span data-stu-id="ae377-111">Element</span></span>                                                                                            | <span data-ttu-id="ae377-112">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="ae377-112">Derived from</span></span>                                                                       | <span data-ttu-id="ae377-113">Description</span><span class="sxs-lookup"><span data-stu-id="ae377-113">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae377-114">**CalendarTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="ae377-114">**CalendarTrigger (triggerGroup)**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="ae377-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ae377-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="ae377-116">Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.</span><span class="sxs-lookup"><span data-stu-id="ae377-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="ae377-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae377-117">Requirements</span></span>



| <span data-ttu-id="ae377-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae377-118">Requirement</span></span> | <span data-ttu-id="ae377-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae377-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae377-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae377-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae377-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae377-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae377-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae377-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae377-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae377-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





