---
title: Élément StartWhenAvailable (settingsType)
description: Spécifie que les Planificateur de tâches peuvent démarrer la tâche à tout moment une fois l’heure planifiée passée.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Élément StartWhenAvailable Planificateur de tâches
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941822"
---
# <a name="startwhenavailable-settingstype-element"></a><span data-ttu-id="a216b-104">Élément StartWhenAvailable (settingsType)</span><span class="sxs-lookup"><span data-stu-id="a216b-104">StartWhenAvailable (settingsType) Element</span></span>

<span data-ttu-id="a216b-105">Spécifie que les Planificateur de tâches peuvent démarrer la tâche à tout moment une fois l’heure planifiée passée.</span><span class="sxs-lookup"><span data-stu-id="a216b-105">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="a216b-106">L’élément **StartWhenAvailable** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a216b-106">The **StartWhenAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a216b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a216b-107">Parent element</span></span>



| <span data-ttu-id="a216b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="a216b-108">Element</span></span>                                                           | <span data-ttu-id="a216b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="a216b-109">Derived from</span></span>                                                         | <span data-ttu-id="a216b-110">Description</span><span class="sxs-lookup"><span data-stu-id="a216b-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="a216b-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="a216b-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="a216b-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="a216b-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="a216b-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="a216b-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a216b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a216b-114">Remarks</span></span>

<span data-ttu-id="a216b-115">Cette propriété s’applique uniquement aux tâches chronométrées.</span><span class="sxs-lookup"><span data-stu-id="a216b-115">This property applies only to timed tasks.</span></span>

<span data-ttu-id="a216b-116">Pour le développement C++, consultez la [**propriété StartWhenAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span><span class="sxs-lookup"><span data-stu-id="a216b-116">For C++ development, see [**StartWhenAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span></span>

<span data-ttu-id="a216b-117">Pour le développement de scripts, consultez [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md).</span><span class="sxs-lookup"><span data-stu-id="a216b-117">For script development, see [**TaskSettings.StartWhenAvailable**](tasksettings-startwhenavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a216b-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="a216b-118">Examples</span></span>

<span data-ttu-id="a216b-119">Le code XML suivant définit un élément Settings qui permet au Planificateur de tâches de démarrer la tâche lorsqu’elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="a216b-119">The following XML defines a settings element that allows the Task Scheduler to start the task when it is available.</span></span>


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="a216b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a216b-120">Requirements</span></span>



| <span data-ttu-id="a216b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a216b-121">Requirement</span></span> | <span data-ttu-id="a216b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a216b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a216b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a216b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a216b-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a216b-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a216b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a216b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a216b-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a216b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a216b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a216b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a216b-128">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="a216b-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





