---
title: Élément Delay (bootTriggerType)
description: Spécifie la durée entre le démarrage du système et le démarrage de la tâche.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
keywords:
- Retarder l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942865"
---
# <a name="delay-boottriggertype-element"></a><span data-ttu-id="650f6-104">Élément Delay (bootTriggerType)</span><span class="sxs-lookup"><span data-stu-id="650f6-104">Delay (bootTriggerType) Element</span></span>

<span data-ttu-id="650f6-105">Spécifie la durée entre le démarrage du système et le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="650f6-105">Specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="650f6-106">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="650f6-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="650f6-107">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="650f6-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="650f6-108">L’élément **delay** est défini par le type complexe [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="650f6-108">The **Delay** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="650f6-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="650f6-109">Parent element</span></span>



| <span data-ttu-id="650f6-110">Élément</span><span class="sxs-lookup"><span data-stu-id="650f6-110">Element</span></span>                                                                     | <span data-ttu-id="650f6-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="650f6-111">Derived from</span></span>                                                               | <span data-ttu-id="650f6-112">Description</span><span class="sxs-lookup"><span data-stu-id="650f6-112">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="650f6-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="650f6-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md) | [<span data-ttu-id="650f6-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="650f6-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md) | <span data-ttu-id="650f6-115">Spécifie un déclencheur qui démarre une tâche au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="650f6-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="650f6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="650f6-116">Remarks</span></span>

<span data-ttu-id="650f6-117">Pour le développement de scripts, le délai de déclenchement des événements est spécifié par la propriété [**BootTrigger. Delay**](boottrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="650f6-117">For script development, the event trigger delay is specified by the [**BootTrigger.Delay**](boottrigger-delay.md) property.</span></span>

<span data-ttu-id="650f6-118">Pour le développement C++, le délai de déclenchement des événements est spécifié par la propriété [**IBootTrigger ::D Nouv**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="650f6-118">For C++ development, the event trigger delay is specified by the [**IBootTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="650f6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="650f6-119">Requirements</span></span>



| <span data-ttu-id="650f6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="650f6-120">Requirement</span></span> | <span data-ttu-id="650f6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="650f6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="650f6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="650f6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="650f6-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="650f6-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="650f6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="650f6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="650f6-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="650f6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="650f6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="650f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650f6-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="650f6-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="650f6-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="650f6-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





