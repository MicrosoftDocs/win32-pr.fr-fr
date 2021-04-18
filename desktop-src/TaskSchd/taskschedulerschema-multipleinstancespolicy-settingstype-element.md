---
title: Élément MultipleInstancesPolicy (settingsType)
description: Spécifie la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Élément MultipleInstancesPolicy Planificateur de tâches
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512584"
---
# <a name="multipleinstancespolicy-settingstype-element"></a><span data-ttu-id="f2649-104">Élément MultipleInstancesPolicy (settingsType)</span><span class="sxs-lookup"><span data-stu-id="f2649-104">MultipleInstancesPolicy (settingsType) Element</span></span>

<span data-ttu-id="f2649-105">Spécifie la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f2649-105">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

<span data-ttu-id="f2649-106">L’élément **MultipleInstancesPolicy** est défini par le type simple [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="f2649-106">The **MultipleInstancesPolicy** element is defined by the [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f2649-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f2649-107">Parent element</span></span>



| <span data-ttu-id="f2649-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f2649-108">Element</span></span>                                                           | <span data-ttu-id="f2649-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f2649-109">Derived from</span></span>                                                         | <span data-ttu-id="f2649-110">Description</span><span class="sxs-lookup"><span data-stu-id="f2649-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2649-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="f2649-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f2649-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="f2649-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f2649-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="f2649-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f2649-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f2649-114">Remarks</span></span>

<span data-ttu-id="f2649-115">Pour le développement C++, consultez la [**propriété MultipleInstances de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span><span class="sxs-lookup"><span data-stu-id="f2649-115">For C++ development, see [**MultipleInstances Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span></span>

<span data-ttu-id="f2649-116">Pour le développement de scripts, consultez [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md).</span><span class="sxs-lookup"><span data-stu-id="f2649-116">For script development, see [**TaskSettings.MultipleInstances**](tasksettings-multipleinstances.md).</span></span>

### <a name="restricted-values"></a><span data-ttu-id="f2649-117">Valeurs restreintes</span><span class="sxs-lookup"><span data-stu-id="f2649-117">Restricted Values</span></span>

<span data-ttu-id="f2649-118">Cet élément est limité aux valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f2649-118">This element is restricted to the following values.</span></span>

-   <span data-ttu-id="f2649-119">Parallel : démarre une nouvelle instance pendant l’exécution d’une instance existante.</span><span class="sxs-lookup"><span data-stu-id="f2649-119">Parallel: Starts a new instance while an existing instance is running.</span></span>
-   <span data-ttu-id="f2649-120">Queue : démarre une nouvelle instance de la tâche une fois que toutes les autres instances de la tâche sont terminées.</span><span class="sxs-lookup"><span data-stu-id="f2649-120">Queue: Starts a new instance of task after all other instances of the task are complete.</span></span>
-   <span data-ttu-id="f2649-121">IgnoreNew : valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f2649-121">IgnoreNew: Default.</span></span> <span data-ttu-id="f2649-122">Ne démarre pas une nouvelle instance si une instance existante de la tâche est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f2649-122">Does not start a new instance if an existing instance of the task is running.</span></span>
-   <span data-ttu-id="f2649-123">StopExisting : arrête une instance existante de la tâche avant de démarrer une nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="f2649-123">StopExisting: Stops an existing instance of the task before it starts a new instance.</span></span>

## <a name="examples"></a><span data-ttu-id="f2649-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="f2649-124">Examples</span></span>

<span data-ttu-id="f2649-125">Le code XML suivant définit un élément Settings qui permet à plusieurs instances de la tâche de s’exécuter en parallèle.</span><span class="sxs-lookup"><span data-stu-id="f2649-125">The following XML defines a settings element that allows multiple instances of the task to run in parallel.</span></span>


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="f2649-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2649-126">Requirements</span></span>



| <span data-ttu-id="f2649-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2649-127">Requirement</span></span> | <span data-ttu-id="f2649-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2649-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f2649-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2649-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2649-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2649-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2649-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2649-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2649-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2649-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2649-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2649-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2649-134">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f2649-134">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





