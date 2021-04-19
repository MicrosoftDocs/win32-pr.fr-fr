---
title: Élément RandomDelay (timeTriggerType)
description: Contient le délai d’attente ajouté de manière aléatoire à l’heure de début du déclencheur. | Élément RandomDelay (timeTriggerType)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
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
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531292"
---
# <a name="randomdelay-timetriggertype-element"></a><span data-ttu-id="204e4-105">Élément RandomDelay (timeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="204e4-105">RandomDelay (timeTriggerType) Element</span></span>

<span data-ttu-id="204e4-106">Contient le délai d’attente ajouté de manière aléatoire à l’heure de début du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="204e4-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="204e4-107">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="204e4-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="204e4-108">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="204e4-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="204e4-109">L’élément est défini par le type complexe [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="204e4-109">The element is defined by the [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="204e4-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="204e4-110">Parent element</span></span>



| <span data-ttu-id="204e4-111">Élément</span><span class="sxs-lookup"><span data-stu-id="204e4-111">Element</span></span>                                                                                    | <span data-ttu-id="204e4-112">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="204e4-112">Derived from</span></span>                                                               | <span data-ttu-id="204e4-113">Description</span><span class="sxs-lookup"><span data-stu-id="204e4-113">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="204e4-114">**TimeTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="204e4-114">**TimeTrigger (triggerGroup)**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md) | [<span data-ttu-id="204e4-115">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="204e4-115">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md) | <span data-ttu-id="204e4-116">Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.</span><span class="sxs-lookup"><span data-stu-id="204e4-116">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="204e4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="204e4-117">Remarks</span></span>

<span data-ttu-id="204e4-118">Pour le développement C++, consultez la [**propriété RandomDelay de ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span><span class="sxs-lookup"><span data-stu-id="204e4-118">For C++ development, see [**RandomDelay Property of ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span></span>

<span data-ttu-id="204e4-119">Pour le développement de scripts, consultez [**timetrigger. RandomDelay**](timetrigger-randomdelay.md).</span><span class="sxs-lookup"><span data-stu-id="204e4-119">For script development, see [**TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="204e4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="204e4-120">Requirements</span></span>



| <span data-ttu-id="204e4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="204e4-121">Requirement</span></span> | <span data-ttu-id="204e4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="204e4-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="204e4-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="204e4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="204e4-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="204e4-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="204e4-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="204e4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="204e4-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="204e4-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





