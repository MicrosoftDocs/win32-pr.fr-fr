---
title: Count (élément restartType)
description: Spécifie le nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Count, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464810"
---
# <a name="count-restarttype-element"></a><span data-ttu-id="bc684-104">Count (élément restartType)</span><span class="sxs-lookup"><span data-stu-id="bc684-104">Count (restartType) Element</span></span>

<span data-ttu-id="bc684-105">Spécifie le nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="bc684-105">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span>

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="bc684-106">L’élément est défini par le type complexe [**restartType**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bc684-106">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bc684-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="bc684-107">Parent element</span></span>



| <span data-ttu-id="bc684-108">Élément</span><span class="sxs-lookup"><span data-stu-id="bc684-108">Element</span></span>                                                                               | <span data-ttu-id="bc684-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="bc684-109">Derived from</span></span>                                                       | <span data-ttu-id="bc684-110">Description</span><span class="sxs-lookup"><span data-stu-id="bc684-110">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc684-111">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="bc684-111">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="bc684-112">**restartType**</span><span class="sxs-lookup"><span data-stu-id="bc684-112">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="bc684-113">Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="bc684-113">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bc684-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bc684-114">Remarks</span></span>

<span data-ttu-id="bc684-115">Si cet élément est spécifié, l’élément [**Interval**](taskschedulerschema-interval-restarttype-element.md) doit également être spécifié pour indiquer au planificateur de tâches la durée de la tentative de redémarrage de la tâche.</span><span class="sxs-lookup"><span data-stu-id="bc684-115">If this element is specified, the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element must also be specified to tell the Task Scheduler how long to attempt to restart the task.</span></span>

<span data-ttu-id="bc684-116">Pour le développement C++, consultez la [**propriété RestartCount de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span><span class="sxs-lookup"><span data-stu-id="bc684-116">For C++ development, see [**RestartCount Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span></span>

<span data-ttu-id="bc684-117">Pour le développement de scripts, consultez [**TaskSettings. RestartCount**](tasksettings-restartcount.md).</span><span class="sxs-lookup"><span data-stu-id="bc684-117">For script development, see [**TaskSettings.RestartCount**](tasksettings-restartcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc684-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc684-118">Requirements</span></span>



| <span data-ttu-id="bc684-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc684-119">Requirement</span></span> | <span data-ttu-id="bc684-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc684-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc684-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc684-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bc684-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc684-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc684-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc684-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bc684-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc684-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc684-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc684-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc684-126">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="bc684-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





