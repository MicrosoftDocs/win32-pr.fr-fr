---
title: Élément Duration (repetitionType)
description: Spécifie la durée de répétition du modèle.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Élément Duration Planificateur de tâches
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317506"
---
# <a name="duration-repetitiontype-element"></a><span data-ttu-id="f999f-104">Élément Duration (repetitionType)</span><span class="sxs-lookup"><span data-stu-id="f999f-104">Duration (repetitionType) Element</span></span>

<span data-ttu-id="f999f-105">Spécifie la durée de répétition du modèle.</span><span class="sxs-lookup"><span data-stu-id="f999f-105">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="f999f-106">Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes).</span><span class="sxs-lookup"><span data-stu-id="f999f-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="f999f-107">Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="f999f-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="f999f-108">Si aucune valeur n’est spécifiée pour la durée, le modèle est répété indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="f999f-108">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span> <span data-ttu-id="f999f-109">La valeur minimale est d’une minute.</span><span class="sxs-lookup"><span data-stu-id="f999f-109">The minimum value is one minute.</span></span>

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="f999f-110">L’élément est défini par le type complexe [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f999f-110">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f999f-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f999f-111">Parent element</span></span>



| <span data-ttu-id="f999f-112">Élément</span><span class="sxs-lookup"><span data-stu-id="f999f-112">Element</span></span>                                                                      | <span data-ttu-id="f999f-113">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f999f-113">Derived from</span></span>                                                             | <span data-ttu-id="f999f-114">Description</span><span class="sxs-lookup"><span data-stu-id="f999f-114">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f999f-115">**Répétition**</span><span class="sxs-lookup"><span data-stu-id="f999f-115">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="f999f-116">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="f999f-116">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="f999f-117">Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f999f-117">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f999f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f999f-118">Remarks</span></span>

<span data-ttu-id="f999f-119">Pour les applications de script, la durée du modèle est spécifiée à l’aide de la propriété [**RepetitionPattern. Duration**](repetitionpattern-duration.md) .</span><span class="sxs-lookup"><span data-stu-id="f999f-119">For scripting applications, the duration of the pattern is specified using the [**RepetitionPattern.Duration**](repetitionpattern-duration.md) property.</span></span>

<span data-ttu-id="f999f-120">Pour les applications C++, la durée du modèle est spécifiée à l’aide de la propriété [**IRepetitionPattern ::D figuration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="f999f-120">For C++ applications, the duration of the pattern is specified using the [**IRepetitionPattern::Duration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f999f-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="f999f-121">Examples</span></span>

<span data-ttu-id="f999f-122">Le code XML suivant définit un modèle de répétition pour un déclencheur.</span><span class="sxs-lookup"><span data-stu-id="f999f-122">The following XML defines a repetition pattern for a trigger.</span></span>


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



## <a name="requirements"></a><span data-ttu-id="f999f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f999f-123">Requirements</span></span>



| <span data-ttu-id="f999f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f999f-124">Requirement</span></span> | <span data-ttu-id="f999f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f999f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f999f-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f999f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f999f-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f999f-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f999f-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f999f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f999f-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f999f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f999f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f999f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f999f-131">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f999f-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f999f-132">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f999f-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





