---
title: Interval (élément restartType)
description: Spécifie la durée pendant laquelle le Planificateur de tâches tente de redémarrer la tâche.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
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
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734184"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="93b81-104">Interval (élément restartType)</span><span class="sxs-lookup"><span data-stu-id="93b81-104">Interval (restartType) Element</span></span>

<span data-ttu-id="93b81-105">Spécifie la durée pendant laquelle le Planificateur de tâches tente de redémarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="93b81-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="93b81-106">Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, « PT5M » est de 5 minutes, « PT1H » est 1 heure et « PT20M » est 20 minutes).</span><span class="sxs-lookup"><span data-stu-id="93b81-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="93b81-107">La durée maximale autorisée est de 31 jours, et la durée minimale autorisée est de 1 minute.</span><span class="sxs-lookup"><span data-stu-id="93b81-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

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

<span data-ttu-id="93b81-108">L’élément est défini par le type complexe [**restartType**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="93b81-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="93b81-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="93b81-109">Parent element</span></span>



| <span data-ttu-id="93b81-110">Élément</span><span class="sxs-lookup"><span data-stu-id="93b81-110">Element</span></span>                                                                               | <span data-ttu-id="93b81-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="93b81-111">Derived from</span></span>                                                       | <span data-ttu-id="93b81-112">Description</span><span class="sxs-lookup"><span data-stu-id="93b81-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93b81-113">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="93b81-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="93b81-114">**restartType**</span><span class="sxs-lookup"><span data-stu-id="93b81-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="93b81-115">Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="93b81-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="93b81-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="93b81-116">Remarks</span></span>

<span data-ttu-id="93b81-117">Si cet élément est spécifié, l’élément [**Count**](taskschedulerschema-count-restarttype-element.md) doit également être spécifié pour indiquer au planificateur de tâches combien de fois il doit essayer de redémarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="93b81-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="93b81-118">Pour le développement C++, consultez la [**propriété RestartInterval de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span><span class="sxs-lookup"><span data-stu-id="93b81-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="93b81-119">Pour le développement de scripts, consultez [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md).</span><span class="sxs-lookup"><span data-stu-id="93b81-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93b81-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93b81-120">Requirements</span></span>



| <span data-ttu-id="93b81-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93b81-121">Requirement</span></span> | <span data-ttu-id="93b81-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="93b81-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93b81-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93b81-123">Minimum supported client</span></span><br/> | <span data-ttu-id="93b81-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93b81-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="93b81-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93b81-125">Minimum supported server</span></span><br/> | <span data-ttu-id="93b81-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93b81-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93b81-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93b81-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b81-128">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="93b81-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





