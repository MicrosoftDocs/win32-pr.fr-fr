---
title: Élément RunOnlyIfIdle (settingsType)
description: Spécifie que la tâche est exécutée uniquement lorsque l’ordinateur est dans un état d’inactivité.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Élément RunOnlyIfIdle Planificateur de tâches
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033121"
---
# <a name="runonlyifidle-settingstype-element"></a><span data-ttu-id="72fd2-104">Élément RunOnlyIfIdle (settingsType)</span><span class="sxs-lookup"><span data-stu-id="72fd2-104">RunOnlyIfIdle (settingsType) Element</span></span>

<span data-ttu-id="72fd2-105">Spécifie que la tâche est exécutée uniquement lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="72fd2-105">Specifies that the task is run only when the computer is in an idle state.</span></span>

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

<span data-ttu-id="72fd2-106">L’élément **RunOnlyIfIdle** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="72fd2-106">The **RunOnlyIfIdle** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="72fd2-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="72fd2-107">Parent element</span></span>



| <span data-ttu-id="72fd2-108">Élément</span><span class="sxs-lookup"><span data-stu-id="72fd2-108">Element</span></span>                                                           | <span data-ttu-id="72fd2-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="72fd2-109">Derived from</span></span>                                                         | <span data-ttu-id="72fd2-110">Description</span><span class="sxs-lookup"><span data-stu-id="72fd2-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="72fd2-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="72fd2-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="72fd2-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="72fd2-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="72fd2-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="72fd2-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="72fd2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="72fd2-114">Remarks</span></span>

<span data-ttu-id="72fd2-115">Pour le développement C++, consultez la [**propriété RunOnlyIfIdle de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span><span class="sxs-lookup"><span data-stu-id="72fd2-115">For C++ development, see [**RunOnlyIfIdle Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span></span>

<span data-ttu-id="72fd2-116">Pour le développement de scripts, consultez [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span><span class="sxs-lookup"><span data-stu-id="72fd2-116">For script development, see [**TaskSettings.RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72fd2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72fd2-117">Requirements</span></span>



| <span data-ttu-id="72fd2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72fd2-118">Requirement</span></span> | <span data-ttu-id="72fd2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="72fd2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72fd2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72fd2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72fd2-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72fd2-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="72fd2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72fd2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72fd2-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72fd2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72fd2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72fd2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72fd2-125">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="72fd2-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="72fd2-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="72fd2-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





