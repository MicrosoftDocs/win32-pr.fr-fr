---
title: Volatile (élément)
description: Indique si la tâche est automatiquement désactivée à chaque démarrage de Windows.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Planificateur de tâches d’élément volatile
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743316"
---
# <a name="volatile-element"></a><span data-ttu-id="e9dd7-104">Volatile (élément)</span><span class="sxs-lookup"><span data-stu-id="e9dd7-104">Volatile Element</span></span>

<span data-ttu-id="e9dd7-105">Indique si la tâche est automatiquement désactivée à chaque démarrage de Windows.</span><span class="sxs-lookup"><span data-stu-id="e9dd7-105">Indicates whether the task is automatically disabled every time Windows starts.</span></span>

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

<span data-ttu-id="e9dd7-106">L’élément **volatile** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9dd7-106">The **Volatile** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e9dd7-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e9dd7-107">Parent element</span></span>



| <span data-ttu-id="e9dd7-108">Élément</span><span class="sxs-lookup"><span data-stu-id="e9dd7-108">Element</span></span>                                                           | <span data-ttu-id="e9dd7-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="e9dd7-109">Derived from</span></span> | <span data-ttu-id="e9dd7-110">Description</span><span class="sxs-lookup"><span data-stu-id="e9dd7-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9dd7-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="e9dd7-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) |              | <span data-ttu-id="e9dd7-112">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="e9dd7-112">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9dd7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e9dd7-113">Remarks</span></span>

<span data-ttu-id="e9dd7-114">Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**ITaskSettings3 :: volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) .</span><span class="sxs-lookup"><span data-stu-id="e9dd7-114">For C++ programming, this idle setting is specified using the [**ITaskSettings3::Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9dd7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9dd7-115">Requirements</span></span>



| <span data-ttu-id="e9dd7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9dd7-116">Requirement</span></span> | <span data-ttu-id="e9dd7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9dd7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9dd7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9dd7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e9dd7-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9dd7-119">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="e9dd7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9dd7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e9dd7-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9dd7-121">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9dd7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9dd7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9dd7-123">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e9dd7-123">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e9dd7-124">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e9dd7-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





