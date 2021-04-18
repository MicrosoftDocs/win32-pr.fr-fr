---
title: Élément RestartOnIdle (idleSettingsType)
description: Spécifie si la tâche est redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Élément RestartOnIdle Planificateur de tâches
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543059"
---
# <a name="restartonidle-idlesettingstype-element"></a><span data-ttu-id="1543d-104">Élément RestartOnIdle (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="1543d-104">RestartOnIdle (idleSettingsType) Element</span></span>

<span data-ttu-id="1543d-105">Spécifie si la tâche est redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="1543d-105">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="1543d-106">L’élément **RestartOnIdle** est défini par le type complexe [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1543d-106">The **RestartOnIdle** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1543d-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="1543d-107">Parent element</span></span>



| <span data-ttu-id="1543d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="1543d-108">Element</span></span>                                                                       | <span data-ttu-id="1543d-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="1543d-109">Derived from</span></span>                                                                 | <span data-ttu-id="1543d-110">Description</span><span class="sxs-lookup"><span data-stu-id="1543d-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1543d-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="1543d-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="1543d-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="1543d-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="1543d-113">Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="1543d-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1543d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1543d-114">Remarks</span></span>

<span data-ttu-id="1543d-115">Cet élément est utilisé uniquement si l’élément [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) est défini sur true.</span><span class="sxs-lookup"><span data-stu-id="1543d-115">This element is used only if the [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element is set to True.</span></span>

<span data-ttu-id="1543d-116">Pour le développement de scripts, ce paramètre de tâche est spécifié à l’aide de la propriété [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) .</span><span class="sxs-lookup"><span data-stu-id="1543d-116">For script development, this task settings is specified using the [**IdleSettings.RestartOnIdle**](idlesettings-restartonidle.md) property.</span></span>

<span data-ttu-id="1543d-117">Pour le développement C++, ce paramètre de tâche est spécifié à l’aide de la propriété [**IIdleSettings :: RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .</span><span class="sxs-lookup"><span data-stu-id="1543d-117">For C++ development, this task settings is specified using the [**IIdleSettings::RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) property.</span></span>

## <a name="examples"></a><span data-ttu-id="1543d-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="1543d-118">Examples</span></span>

<span data-ttu-id="1543d-119">Le code XML suivant définit un paramètre inactif qui indique que la tâche ne doit pas être redémarrée quand la condition d’inactivité est en cycle.</span><span class="sxs-lookup"><span data-stu-id="1543d-119">The following XML defines an idle setting that indicates that the task should not be restarted when the idle condition cycles.</span></span>


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="1543d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1543d-120">Requirements</span></span>



| <span data-ttu-id="1543d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1543d-121">Requirement</span></span> | <span data-ttu-id="1543d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1543d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1543d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1543d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1543d-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1543d-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1543d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1543d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1543d-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1543d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1543d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1543d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1543d-128">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1543d-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1543d-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1543d-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





