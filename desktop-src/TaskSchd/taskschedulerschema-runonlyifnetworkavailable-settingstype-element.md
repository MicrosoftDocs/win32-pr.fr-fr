---
title: Élément RunOnlyIfNetworkAvailable (settingsType)
description: Spécifie que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Élément RunOnlyIfNetworkAvailable Planificateur de tâches
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ff1e7c838c142e30b75eb4abb935c0de352d9f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942619"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a><span data-ttu-id="7ee98-104">Élément RunOnlyIfNetworkAvailable (settingsType)</span><span class="sxs-lookup"><span data-stu-id="7ee98-104">RunOnlyIfNetworkAvailable (settingsType) Element</span></span>

<span data-ttu-id="7ee98-105">Spécifie que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.</span><span class="sxs-lookup"><span data-stu-id="7ee98-105">Specifies that the Task Scheduler will run the task only when a network is available.</span></span>

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="7ee98-106">L’élément **RunOnlyIfNetworkAvailable** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7ee98-106">The **RunOnlyIfNetworkAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7ee98-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7ee98-107">Parent element</span></span>



| <span data-ttu-id="7ee98-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7ee98-108">Element</span></span>                                                           | <span data-ttu-id="7ee98-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7ee98-109">Derived from</span></span>                                                         | <span data-ttu-id="7ee98-110">Description</span><span class="sxs-lookup"><span data-stu-id="7ee98-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ee98-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="7ee98-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="7ee98-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="7ee98-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="7ee98-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="7ee98-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7ee98-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7ee98-114">Remarks</span></span>

<span data-ttu-id="7ee98-115">Pour le développement C++, consultez la [**propriété RunOnlyIfNetworkAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span><span class="sxs-lookup"><span data-stu-id="7ee98-115">For C++ development, see [**RunOnlyIfNetworkAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).</span></span>

<span data-ttu-id="7ee98-116">Pour le développement de scripts, consultez [**TaskSettings. RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span><span class="sxs-lookup"><span data-stu-id="7ee98-116">For script development, see [**TaskSettings.RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7ee98-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="7ee98-117">Examples</span></span>

<span data-ttu-id="7ee98-118">Le code XML suivant définit un élément Settings qui permet à la tâche de démarrer uniquement si un réseau est disponible.</span><span class="sxs-lookup"><span data-stu-id="7ee98-118">The following XML defines a settings element that allows the task to start only if a network is available.</span></span>


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="7ee98-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ee98-119">Requirements</span></span>



| <span data-ttu-id="7ee98-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ee98-120">Requirement</span></span> | <span data-ttu-id="7ee98-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ee98-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ee98-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ee98-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ee98-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ee98-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ee98-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ee98-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ee98-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ee98-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ee98-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ee98-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ee98-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7ee98-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





