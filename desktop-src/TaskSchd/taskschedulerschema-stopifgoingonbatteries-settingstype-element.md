---
title: Élément StopIfGoingOnBatteries (settingsType)
description: Spécifie que la tâche sera arrêtée si l’ordinateur va sur des batteries.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Élément StopIfGoingOnBatteries Planificateur de tâches
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509910"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a><span data-ttu-id="3751b-104">Élément StopIfGoingOnBatteries (settingsType)</span><span class="sxs-lookup"><span data-stu-id="3751b-104">StopIfGoingOnBatteries (settingsType) Element</span></span>

<span data-ttu-id="3751b-105">Spécifie que la tâche sera arrêtée si l’ordinateur va sur des batteries.</span><span class="sxs-lookup"><span data-stu-id="3751b-105">Specifies that the task will be stopped if the computer is going onto batteries.</span></span>

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="3751b-106">L’élément **StopIfGoingOnBatteries** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3751b-106">The **StopIfGoingOnBatteries** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3751b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="3751b-107">Parent element</span></span>



| <span data-ttu-id="3751b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="3751b-108">Element</span></span>                                                           | <span data-ttu-id="3751b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="3751b-109">Derived from</span></span>                                                         | <span data-ttu-id="3751b-110">Description</span><span class="sxs-lookup"><span data-stu-id="3751b-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="3751b-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="3751b-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="3751b-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="3751b-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="3751b-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="3751b-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3751b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3751b-114">Remarks</span></span>

<span data-ttu-id="3751b-115">La valeur par défaut de cet élément est false.</span><span class="sxs-lookup"><span data-stu-id="3751b-115">The default setting for this element is False.</span></span> <span data-ttu-id="3751b-116">Notez que la valeur par défaut a été modifiée par rapport aux versions précédentes de Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="3751b-116">Note that the default value has changed from previous versions of Task Scheduler.</span></span>

<span data-ttu-id="3751b-117">Pour le développement de script, ce paramètre est spécifié à l’aide de la propriété [**TaskSettings. StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) .</span><span class="sxs-lookup"><span data-stu-id="3751b-117">For scripting development, this setting is specified using the [**TaskSettings.StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) property.</span></span>

<span data-ttu-id="3751b-118">Pour le développement C++, ce paramètre est spécifié à l’aide de la propriété [**ITaskSettings :: StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) .</span><span class="sxs-lookup"><span data-stu-id="3751b-118">For C++ development, this setting is specified using the [**ITaskSettings::StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) property.</span></span>

## <a name="examples"></a><span data-ttu-id="3751b-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="3751b-119">Examples</span></span>

<span data-ttu-id="3751b-120">Le code XML suivant définit un élément Settings qui permet un arrêt forcé de la tâche.</span><span class="sxs-lookup"><span data-stu-id="3751b-120">The following XML defines a settings element that allows a hard termination of the task.</span></span>


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="3751b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3751b-121">Requirements</span></span>



| <span data-ttu-id="3751b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3751b-122">Requirement</span></span> | <span data-ttu-id="3751b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3751b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3751b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3751b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3751b-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3751b-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3751b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3751b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3751b-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3751b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3751b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3751b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3751b-129">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="3751b-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





