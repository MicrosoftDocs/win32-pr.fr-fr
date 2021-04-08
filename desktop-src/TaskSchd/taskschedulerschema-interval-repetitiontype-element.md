---
title: Interval (élément repetitionType)
description: Spécifie la durée entre chaque redémarrage de la tâche.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Élément Interval Planificateur de tâches
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9720bc2257d4c0b45116089bfdd4113335fc6b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941893"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="f852a-104">Interval (élément repetitionType)</span><span class="sxs-lookup"><span data-stu-id="f852a-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="f852a-105">Spécifie la durée entre chaque redémarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f852a-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="f852a-106">Le format de cette chaîne est P <days> DT <hours> H <minutes> M <seconds> S (par exemple, « PT5M » est de 5 minutes, « PT1H » est 1 heure et « PT20M » est de 20 minutes).</span><span class="sxs-lookup"><span data-stu-id="f852a-106">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="f852a-107">La durée maximale autorisée est de 31 jours, et la durée minimale autorisée est de 1 minute.</span><span class="sxs-lookup"><span data-stu-id="f852a-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="f852a-108">L’élément est défini par le type complexe [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f852a-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f852a-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f852a-109">Parent element</span></span>



| <span data-ttu-id="f852a-110">Élément</span><span class="sxs-lookup"><span data-stu-id="f852a-110">Element</span></span>                                                                      | <span data-ttu-id="f852a-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f852a-111">Derived from</span></span>                                                             | <span data-ttu-id="f852a-112">Description</span><span class="sxs-lookup"><span data-stu-id="f852a-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f852a-113">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="f852a-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="f852a-114">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="f852a-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="f852a-115">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f852a-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f852a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f852a-116">Remarks</span></span>

<span data-ttu-id="f852a-117">Pour le développement de script, l’intervalle du modèle de répétition est spécifié à l’aide de la propriété [**RepetitionPattern. Interval**](repetitionpattern-interval.md) .</span><span class="sxs-lookup"><span data-stu-id="f852a-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="f852a-118">Pour le développement C++, l’intervalle du modèle de répétition est spécifié à l’aide de la propriété [**IRepetitionPattern :: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .</span><span class="sxs-lookup"><span data-stu-id="f852a-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f852a-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="f852a-119">Examples</span></span>

<span data-ttu-id="f852a-120">Pour obtenir un exemple complet du code XML d’une tâche qui utilise un intervalle de répétition, consultez [exemple de déclencheur quotidien (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="f852a-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f852a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f852a-121">Requirements</span></span>



| <span data-ttu-id="f852a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f852a-122">Requirement</span></span> | <span data-ttu-id="f852a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f852a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f852a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f852a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f852a-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f852a-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f852a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f852a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f852a-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f852a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f852a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f852a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f852a-129">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f852a-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f852a-130">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f852a-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





