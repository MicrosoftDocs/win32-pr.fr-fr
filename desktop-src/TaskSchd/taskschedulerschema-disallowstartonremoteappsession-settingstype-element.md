---
title: Élément DisallowStartOnRemoteAppSession (settingsType)
description: Spécifie que la tâche ne sera pas démarrée si elle est déclenchée pour s’exécuter dans une session à distance intégrée à des applications locales (RAIL).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Élément DisallowStartOnRemoteAppSession Planificateur de tâches
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531613"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a><span data-ttu-id="407d3-104">Élément DisallowStartOnRemoteAppSession (settingsType)</span><span class="sxs-lookup"><span data-stu-id="407d3-104">DisallowStartOnRemoteAppSession (settingsType) Element</span></span>

<span data-ttu-id="407d3-105">Spécifie que la tâche ne sera pas démarrée si elle est déclenchée pour s’exécuter dans une session à distance intégrée à des applications locales (RAIL).</span><span class="sxs-lookup"><span data-stu-id="407d3-105">Specifies that the task will not be started if triggered to run in a Remote Applications Integrated Locally (RAIL) session.</span></span>

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="407d3-106">L’élément **DisallowStartOnRemoteAppSession** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="407d3-106">The **DisallowStartOnRemoteAppSession** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="407d3-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="407d3-107">Parent element</span></span>



| <span data-ttu-id="407d3-108">Élément</span><span class="sxs-lookup"><span data-stu-id="407d3-108">Element</span></span>                                                           | <span data-ttu-id="407d3-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="407d3-109">Derived from</span></span>                                                         | <span data-ttu-id="407d3-110">Description</span><span class="sxs-lookup"><span data-stu-id="407d3-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="407d3-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="407d3-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="407d3-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="407d3-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="407d3-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="407d3-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="407d3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="407d3-114">Remarks</span></span>

<span data-ttu-id="407d3-115">La valeur par défaut de cet élément est false.</span><span class="sxs-lookup"><span data-stu-id="407d3-115">The default setting for this element is False.</span></span>

<span data-ttu-id="407d3-116">Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**ITaskSettings2 ::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .</span><span class="sxs-lookup"><span data-stu-id="407d3-116">For C++ development, this information is accessed through the [**ITaskSettings2::DisallowStartOnRemoteAppSession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) property.</span></span>

## <a name="examples"></a><span data-ttu-id="407d3-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="407d3-117">Examples</span></span>

<span data-ttu-id="407d3-118">Le code XML suivant définit un élément Settings qui n’autorise pas la tâche à démarrer si la tâche est déclenchée pour s’exécuter dans une session de RAIL.</span><span class="sxs-lookup"><span data-stu-id="407d3-118">The following XML defines a settings element that does not allow the task to start if the task is triggered to run in a RAIL session.</span></span>


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="407d3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="407d3-119">Requirements</span></span>



| <span data-ttu-id="407d3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="407d3-120">Requirement</span></span> | <span data-ttu-id="407d3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="407d3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="407d3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="407d3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="407d3-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="407d3-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="407d3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="407d3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="407d3-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="407d3-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="407d3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="407d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="407d3-127">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="407d3-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





