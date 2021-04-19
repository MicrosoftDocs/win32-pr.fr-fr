---
title: Élément exclusive
description: Indique si le planificateur de tâches doit démarrer la tâche pendant la maintenance automatique en mode exclusif.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Planificateur de tâches d’élément exclusif
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509903"
---
# <a name="exclusive-element"></a><span data-ttu-id="bc69b-104">Élément exclusive</span><span class="sxs-lookup"><span data-stu-id="bc69b-104">Exclusive Element</span></span>

<span data-ttu-id="bc69b-105">Indique si le planificateur de tâches doit démarrer la tâche pendant la maintenance automatique en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="bc69b-105">Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode.</span></span>

<span data-ttu-id="bc69b-106">L’exclusivité est garantie uniquement entre les autres tâches de maintenance et n’accorde aucune priorité de classement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="bc69b-106">The exclusivity is guaranteed only between other maintenance tasks and doesn't grant any ordering priority of the task.</span></span> <span data-ttu-id="bc69b-107">Si l’exclusivité n’est pas spécifiée, la tâche est démarrée en parallèle avec d’autres tâches de maintenance.</span><span class="sxs-lookup"><span data-stu-id="bc69b-107">If exclusivity is not specified, the task is started in parallel with other maintenance tasks.</span></span>

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="bc69b-108">L’élément **exclusive** est défini par le type complexe [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bc69b-108">The **Exclusive** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bc69b-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="bc69b-109">Parent element</span></span>



| <span data-ttu-id="bc69b-110">Élément</span><span class="sxs-lookup"><span data-stu-id="bc69b-110">Element</span></span>                                                                                                                          | <span data-ttu-id="bc69b-111">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="bc69b-111">Derived from</span></span>                                                                               | <span data-ttu-id="bc69b-112">Description</span><span class="sxs-lookup"><span data-stu-id="bc69b-112">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc69b-113">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="bc69b-113">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="bc69b-114">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="bc69b-114">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="bc69b-115">Spécifie les paramètres de tâche que le planificateur de tâches utilisera pour démarrer la tâche pendant la maintenance automatique.</span><span class="sxs-lookup"><span data-stu-id="bc69b-115">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bc69b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bc69b-116">Remarks</span></span>

<span data-ttu-id="bc69b-117">Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IMaintenanceSettings :: exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .</span><span class="sxs-lookup"><span data-stu-id="bc69b-117">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) property.</span></span>

## <a name="examples"></a><span data-ttu-id="bc69b-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="bc69b-118">Examples</span></span>

<span data-ttu-id="bc69b-119">Le code XML suivant définit des tâches de maintenance avec des exigences d’échéance définies sur 15 jours.</span><span class="sxs-lookup"><span data-stu-id="bc69b-119">The following XML defines maintenance task with deadline requirement set to 15 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="bc69b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc69b-120">Requirements</span></span>



| <span data-ttu-id="bc69b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc69b-121">Requirement</span></span> | <span data-ttu-id="bc69b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc69b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc69b-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc69b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc69b-124">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc69b-124">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="bc69b-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc69b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc69b-126">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc69b-126">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc69b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc69b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc69b-128">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="bc69b-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bc69b-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="bc69b-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





