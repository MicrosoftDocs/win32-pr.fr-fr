---
title: Type simple multipleInstancesPolicyType
description: Définit les constantes de stratégie d’instance pour l’élément MultipleInstancesPolicy (settingsType).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- Planificateur de tâches de type simple multipleInstancesPolicyType
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942343"
---
# <a name="multipleinstancespolicytype-simple-type"></a><span data-ttu-id="76b5f-104">Type simple multipleInstancesPolicyType</span><span class="sxs-lookup"><span data-stu-id="76b5f-104">multipleInstancesPolicyType Simple Type</span></span>

<span data-ttu-id="76b5f-105">Définit les constantes de stratégie d’instance pour l’élément [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="76b5f-105">Defines the instance policy constants for the [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="76b5f-106">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="76b5f-106">Enumeration values</span></span>

<span data-ttu-id="76b5f-107">Le type simple **multipleInstancesPolicyType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="76b5f-107">The **multipleInstancesPolicyType** simple type defines the following values.</span></span>



| <span data-ttu-id="76b5f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="76b5f-108">Value</span></span>        | <span data-ttu-id="76b5f-109">Description</span><span class="sxs-lookup"><span data-stu-id="76b5f-109">Description</span></span>                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76b5f-110">Parallèle</span><span class="sxs-lookup"><span data-stu-id="76b5f-110">Parallel</span></span>     | <span data-ttu-id="76b5f-111">Démarre une nouvelle instance pendant l’exécution d’une instance existante.</span><span class="sxs-lookup"><span data-stu-id="76b5f-111">Starts new instance while an existing instance is running.</span></span><br/>                           |
| <span data-ttu-id="76b5f-112">File d'attente</span><span class="sxs-lookup"><span data-stu-id="76b5f-112">Queue</span></span>        | <span data-ttu-id="76b5f-113">Démarre une nouvelle instance de la tâche une fois que toutes les autres instances de la tâche sont terminées.</span><span class="sxs-lookup"><span data-stu-id="76b5f-113">Starts new instance of task after all other instances of the task are complete.</span></span><br/>      |
| <span data-ttu-id="76b5f-114">IgnoreNew</span><span class="sxs-lookup"><span data-stu-id="76b5f-114">IgnoreNew</span></span>    | <span data-ttu-id="76b5f-115">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="76b5f-115">Default.</span></span> <span data-ttu-id="76b5f-116">Ne démarre pas une nouvelle instance si une instance existante de la tâche est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="76b5f-116">Does not start new instance if an existing instance of the task is running.</span></span><br/> |
| <span data-ttu-id="76b5f-117">StopExisting</span><span class="sxs-lookup"><span data-stu-id="76b5f-117">StopExisting</span></span> | <span data-ttu-id="76b5f-118">Arrête une instance existante de la tâche avant de démarrer une nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="76b5f-118">Stops an existing instance of the task before it starts new instance.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="76b5f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76b5f-119">Requirements</span></span>



| <span data-ttu-id="76b5f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76b5f-120">Requirement</span></span> | <span data-ttu-id="76b5f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="76b5f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76b5f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76b5f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="76b5f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76b5f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76b5f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76b5f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="76b5f-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76b5f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76b5f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76b5f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76b5f-127">Types simples de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="76b5f-127">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="76b5f-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="76b5f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





