---
title: Élément RestartOnFailure (settingsType)
description: Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Élément RestartOnFailure Planificateur de tâches
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200586"
---
# <a name="restartonfailure-settingstype-element"></a><span data-ttu-id="ae2d8-104">Élément RestartOnFailure (settingsType)</span><span class="sxs-lookup"><span data-stu-id="ae2d8-104">RestartOnFailure (settingsType) Element</span></span>

<span data-ttu-id="ae2d8-105">Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="ae2d8-105">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span>

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

<span data-ttu-id="ae2d8-106">L’élément **RestartOnFailure** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2d8-106">The **RestartOnFailure** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ae2d8-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ae2d8-107">Parent element</span></span>



| <span data-ttu-id="ae2d8-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ae2d8-108">Element</span></span>                                                           | <span data-ttu-id="ae2d8-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="ae2d8-109">Derived from</span></span>                                                         | <span data-ttu-id="ae2d8-110">Description</span><span class="sxs-lookup"><span data-stu-id="ae2d8-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae2d8-111">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="ae2d8-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="ae2d8-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="ae2d8-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="ae2d8-113">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="ae2d8-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="ae2d8-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ae2d8-114">Child elements</span></span>



| <span data-ttu-id="ae2d8-115">Élément</span><span class="sxs-lookup"><span data-stu-id="ae2d8-115">Element</span></span>                                                              | <span data-ttu-id="ae2d8-116">Type</span><span class="sxs-lookup"><span data-stu-id="ae2d8-116">Type</span></span>         | <span data-ttu-id="ae2d8-117">Description</span><span class="sxs-lookup"><span data-stu-id="ae2d8-117">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae2d8-118">**Saut**</span><span class="sxs-lookup"><span data-stu-id="ae2d8-118">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       | <span data-ttu-id="ae2d8-119">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ae2d8-119">unsignedByte</span></span> | <span data-ttu-id="ae2d8-120">Spécifie le nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="ae2d8-120">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span><br/> |
| [<span data-ttu-id="ae2d8-121">**Défini**</span><span class="sxs-lookup"><span data-stu-id="ae2d8-121">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) | <span data-ttu-id="ae2d8-122">duration</span><span class="sxs-lookup"><span data-stu-id="ae2d8-122">duration</span></span>     | <span data-ttu-id="ae2d8-123">Spécifie la durée pendant laquelle le Planificateur de tâches tente de redémarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="ae2d8-123">Specifies how long the Task Scheduler will attempt to restart the task.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="ae2d8-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ae2d8-124">Remarks</span></span>

<span data-ttu-id="ae2d8-125">Lorsqu’une application spécifie des paramètres de tâche, ces informations sont accessibles via les propriétés [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) et [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) de l’interface [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) .</span><span class="sxs-lookup"><span data-stu-id="ae2d8-125">When an application specifies task settings, this information is accessed through the [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) and [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) properties of the [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) interface.</span></span> <span data-ttu-id="ae2d8-126">Pour les scripts, ces informations sont accessibles via les propriétés [**TaskSettings. RestartCount**](tasksettings-restartcount.md) et [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2d8-126">For scripting, this information is accessed through the [**TaskSettings.RestartCount**](tasksettings-restartcount.md) and [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md) properties.</span></span>

<span data-ttu-id="ae2d8-127">Les deux éléments enfants doivent être définis pour spécifier la façon dont le Planificateur de tâches redémarre la tâche.</span><span class="sxs-lookup"><span data-stu-id="ae2d8-127">Both child elements must be set to specify how the Task Scheduler restarts the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2d8-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae2d8-128">Requirements</span></span>



| <span data-ttu-id="ae2d8-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae2d8-129">Requirement</span></span> | <span data-ttu-id="ae2d8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae2d8-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae2d8-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae2d8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2d8-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae2d8-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae2d8-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae2d8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2d8-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae2d8-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae2d8-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae2d8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2d8-136">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="ae2d8-136">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





