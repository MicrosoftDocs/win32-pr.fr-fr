---
title: Élément UseUnifiedSchedulingEngine (settingsType)
description: Spécifie que le moteur de planification unifiée sera utilisé pour exécuter cette tâche.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Élément UseUnifiedSchedulingEngine Planificateur de tâches
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032644"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a><span data-ttu-id="c1607-104">Élément UseUnifiedSchedulingEngine (settingsType)</span><span class="sxs-lookup"><span data-stu-id="c1607-104">UseUnifiedSchedulingEngine (settingsType) Element</span></span>

<span data-ttu-id="c1607-105">Spécifie que le moteur de planification unifiée sera utilisé pour exécuter cette tâche.</span><span class="sxs-lookup"><span data-stu-id="c1607-105">Specifies that the Unified Scheduling Engine will be used to run this task.</span></span>

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="c1607-106">L’élément **UseUnifiedSchedulingEngine** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c1607-106">The **UseUnifiedSchedulingEngine** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c1607-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c1607-107">Parent element</span></span>



| <span data-ttu-id="c1607-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c1607-108">Element</span></span>                                                           | <span data-ttu-id="c1607-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c1607-109">Derived from</span></span>                                                         | <span data-ttu-id="c1607-110">Description</span><span class="sxs-lookup"><span data-stu-id="c1607-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1607-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="c1607-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c1607-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c1607-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c1607-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="c1607-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c1607-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c1607-114">Remarks</span></span>

<span data-ttu-id="c1607-115">La valeur par défaut de cet élément est false.</span><span class="sxs-lookup"><span data-stu-id="c1607-115">The default setting for this element is False.</span></span>

<span data-ttu-id="c1607-116">Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**ITaskSettings2 :: UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .</span><span class="sxs-lookup"><span data-stu-id="c1607-116">For C++ development, this information is accessed through the [**ITaskSettings2::UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c1607-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c1607-117">Examples</span></span>

<span data-ttu-id="c1607-118">Le code XML suivant définit un élément Settings qui spécifie que le moteur de planification unifié sera utilisé pour exécuter cette tâche.</span><span class="sxs-lookup"><span data-stu-id="c1607-118">The following XML defines a settings element that specifies that the Unified Scheduling Engine will be used to run this task.</span></span>


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="c1607-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1607-119">Requirements</span></span>



| <span data-ttu-id="c1607-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1607-120">Requirement</span></span> | <span data-ttu-id="c1607-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1607-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c1607-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1607-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c1607-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1607-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c1607-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1607-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c1607-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1607-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1607-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1607-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1607-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c1607-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





