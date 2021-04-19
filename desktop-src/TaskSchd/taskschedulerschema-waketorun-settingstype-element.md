---
title: Élément WakeToRun (settingsType)
description: Spécifie que Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Élément WakeToRun Planificateur de tâches
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518115"
---
# <a name="waketorun-settingstype-element"></a><span data-ttu-id="5207a-104">Élément WakeToRun (settingsType)</span><span class="sxs-lookup"><span data-stu-id="5207a-104">WakeToRun (settingsType) Element</span></span>

<span data-ttu-id="5207a-105">Spécifie que Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="5207a-105">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span>

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

<span data-ttu-id="5207a-106">L’élément **WakeToRun** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5207a-106">The **WakeToRun** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5207a-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="5207a-107">Parent element</span></span>



| <span data-ttu-id="5207a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="5207a-108">Element</span></span>                                                           | <span data-ttu-id="5207a-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="5207a-109">Derived from</span></span>                                                         | <span data-ttu-id="5207a-110">Description</span><span class="sxs-lookup"><span data-stu-id="5207a-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5207a-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="5207a-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="5207a-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="5207a-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="5207a-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="5207a-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5207a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5207a-114">Remarks</span></span>

<span data-ttu-id="5207a-115">Lorsque le service Planificateur de tâches sort de l’ordinateur pour exécuter une tâche, l’écran peut rester inactif même si l’ordinateur n’est plus en mode veille ou veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="5207a-115">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="5207a-116">L’écran s’active lorsque Windows Vista détecte qu’un utilisateur a retourné pour utiliser l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5207a-116">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="5207a-117">Pour le développement C++, consultez la [**propriété WakeToRun de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span><span class="sxs-lookup"><span data-stu-id="5207a-117">For C++ development, see [**WakeToRun Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span></span>

<span data-ttu-id="5207a-118">Pour le développement de scripts, consultez [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).</span><span class="sxs-lookup"><span data-stu-id="5207a-118">For script development, see [**TaskSettings.WakeToRun**](tasksettings-waketorun.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5207a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5207a-119">Requirements</span></span>



| <span data-ttu-id="5207a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5207a-120">Requirement</span></span> | <span data-ttu-id="5207a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5207a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5207a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5207a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5207a-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5207a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5207a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5207a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5207a-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5207a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5207a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5207a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5207a-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5207a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5207a-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5207a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





