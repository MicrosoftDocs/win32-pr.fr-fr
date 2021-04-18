---
title: Élément Enabled (settingsType)
description: Spécifie que la tâche est activée. La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Élément activé Planificateur de tâches
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc86b25fa29345fe120ac5e59d55d847b01c352e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512200"
---
# <a name="enabled-settingstype-element"></a><span data-ttu-id="f59f2-105">Élément Enabled (settingsType)</span><span class="sxs-lookup"><span data-stu-id="f59f2-105">Enabled (settingsType) Element</span></span>

<span data-ttu-id="f59f2-106">Spécifie que la tâche est activée.</span><span class="sxs-lookup"><span data-stu-id="f59f2-106">Specifies that the task is enabled.</span></span> <span data-ttu-id="f59f2-107">La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="f59f2-107">The task can be performed only when this setting is True.</span></span>

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

<span data-ttu-id="f59f2-108">L’élément **activé** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f59f2-108">The **Enabled** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f59f2-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f59f2-109">Parent element</span></span>



| <span data-ttu-id="f59f2-110">Élément</span><span class="sxs-lookup"><span data-stu-id="f59f2-110">Element</span></span>                                                           | <span data-ttu-id="f59f2-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f59f2-111">Derived from</span></span>                                                         | <span data-ttu-id="f59f2-112">Description</span><span class="sxs-lookup"><span data-stu-id="f59f2-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f59f2-113">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="f59f2-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f59f2-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="f59f2-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f59f2-115">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="f59f2-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f59f2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f59f2-116">Remarks</span></span>

<span data-ttu-id="f59f2-117">Pour le développement C++, consultez la [**propriété Enabled de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span><span class="sxs-lookup"><span data-stu-id="f59f2-117">For C++ development, see [**Enabled Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).</span></span>

<span data-ttu-id="f59f2-118">Pour le développement de scripts, consultez [**TaskSettings. Enabled**](tasksettings-enabled.md).</span><span class="sxs-lookup"><span data-stu-id="f59f2-118">For script development, see [**TaskSettings.Enabled**](tasksettings-enabled.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f59f2-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="f59f2-119">Examples</span></span>

<span data-ttu-id="f59f2-120">Pour obtenir un exemple complet du code XML d’une tâche qui est activée, consultez [exemple de déclenchement temporel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="f59f2-120">For a complete example of the XML for a task that is enabled, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f59f2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f59f2-121">Requirements</span></span>



| <span data-ttu-id="f59f2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f59f2-122">Requirement</span></span> | <span data-ttu-id="f59f2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f59f2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f59f2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f59f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f59f2-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f59f2-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f59f2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f59f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f59f2-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f59f2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





