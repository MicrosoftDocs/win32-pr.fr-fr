---
title: Élément MaintenanceSettings (maintenanceSettingsType)
description: Spécifie comment l’Planificateur de tâches effectue des tâches pendant la maintenance automatique.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Élément MaintenanceSettings Planificateur de tâches
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105217"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a><span data-ttu-id="f466a-104">Élément MaintenanceSettings (maintenanceSettingsType)</span><span class="sxs-lookup"><span data-stu-id="f466a-104">MaintenanceSettings (maintenanceSettingsType) Element</span></span>

<span data-ttu-id="f466a-105">Spécifie comment l’Planificateur de tâches effectue des tâches pendant la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="f466a-105">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span>

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="f466a-106">L’élément **MaintenanceSettings** est défini par le type complexe [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f466a-106">The **MaintenanceSettings** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f466a-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f466a-107">Parent element</span></span>



| <span data-ttu-id="f466a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f466a-108">Element</span></span>                                                           | <span data-ttu-id="f466a-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="f466a-109">Derived from</span></span>                                                         | <span data-ttu-id="f466a-110">Description</span><span class="sxs-lookup"><span data-stu-id="f466a-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f466a-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="f466a-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f466a-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="f466a-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f466a-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="f466a-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f466a-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f466a-114">Child elements</span></span>



| <span data-ttu-id="f466a-115">Élément</span><span class="sxs-lookup"><span data-stu-id="f466a-115">Element</span></span>                                                    | <span data-ttu-id="f466a-116">Type</span><span class="sxs-lookup"><span data-stu-id="f466a-116">Type</span></span>    | <span data-ttu-id="f466a-117">Description</span><span class="sxs-lookup"><span data-stu-id="f466a-117">Description</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f466a-118">**Échéance**</span><span class="sxs-lookup"><span data-stu-id="f466a-118">**Deadline**</span></span>](taskschedulerschema-deadline-element.md)   |         | <span data-ttu-id="f466a-119">Spécifie la durée après laquelle le planificateur de tâches tente de démarrer la tâche pendant la maintenance automatique d’urgence, si elle n’a pas pu se terminer pendant une maintenance régulière.</span><span class="sxs-lookup"><span data-stu-id="f466a-119">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span> <br/> |
| [<span data-ttu-id="f466a-120">**Exclusif**</span><span class="sxs-lookup"><span data-stu-id="f466a-120">**Exclusive**</span></span>](taskschedulerschema-exclusive-element.md) | <span data-ttu-id="f466a-121">boolean</span><span class="sxs-lookup"><span data-stu-id="f466a-121">boolean</span></span> | <span data-ttu-id="f466a-122">Si la valeur est true, la tâche est démarrée en mode exclusif parmi les autres tâches de maintenance.</span><span class="sxs-lookup"><span data-stu-id="f466a-122">If set to true, the task will be started exclusively among other maintenance tasks.</span></span> <br/>                                                                                                 |
| [<span data-ttu-id="f466a-123">**Heures**</span><span class="sxs-lookup"><span data-stu-id="f466a-123">**Period**</span></span>](taskschedulerschema-period-element.md)       |         | <span data-ttu-id="f466a-124">Spécifie la fréquence à laquelle la tâche doit être démarrée pendant la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="f466a-124">Specifies how often the task needs to be started during Automatic maintenance.</span></span> <br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="f466a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f466a-125">Remarks</span></span>

<span data-ttu-id="f466a-126">Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**ITaskSettings3 :: MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) .</span><span class="sxs-lookup"><span data-stu-id="f466a-126">For C++ programming, this idle setting is specified using the [**ITaskSettings3::MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f466a-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="f466a-127">Examples</span></span>

<span data-ttu-id="f466a-128">Le code XML suivant définit un élément Settings qui indique à Planificateur de tâches d’exécuter la tâche une fois par période de 5 jours au cours d’une maintenance automatique normale et, en cas d’échec pendant 15 jours, de démarrer la tâche pendant la maintenance automatique d’urgence.</span><span class="sxs-lookup"><span data-stu-id="f466a-128">The following XML defines a settings element that instructs Task Scheduler to execute task once in 5 days during regular Automatic maintenance and if failed for 15 days, start attempting the task during the emergency Automatic maintenance.</span></span>


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="f466a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f466a-129">Requirements</span></span>



| <span data-ttu-id="f466a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f466a-130">Requirement</span></span> | <span data-ttu-id="f466a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f466a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f466a-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f466a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f466a-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f466a-133">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="f466a-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f466a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f466a-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f466a-135">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f466a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f466a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f466a-137">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f466a-137">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f466a-138">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f466a-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





