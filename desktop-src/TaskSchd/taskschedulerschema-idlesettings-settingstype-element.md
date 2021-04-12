---
title: Élément IdleSettings (settingsType)
description: Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Élément IdleSettings Planificateur de tâches
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105220"
---
# <a name="idlesettings-settingstype-element"></a><span data-ttu-id="159ca-104">Élément IdleSettings (settingsType)</span><span class="sxs-lookup"><span data-stu-id="159ca-104">IdleSettings (settingsType) Element</span></span>

<span data-ttu-id="159ca-105">Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="159ca-105">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span> <span data-ttu-id="159ca-106">Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="159ca-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="159ca-107">L’élément **IdleSettings** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="159ca-107">The **IdleSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="159ca-108">Élément parent</span><span class="sxs-lookup"><span data-stu-id="159ca-108">Parent element</span></span>

| <span data-ttu-id="159ca-109">Élément</span><span class="sxs-lookup"><span data-stu-id="159ca-109">Element</span></span>                                                           | <span data-ttu-id="159ca-110">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="159ca-110">Derived from</span></span>                                                         | <span data-ttu-id="159ca-111">Description</span><span class="sxs-lookup"><span data-stu-id="159ca-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="159ca-112">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="159ca-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="159ca-113">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="159ca-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="159ca-114">Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="159ca-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |

## <a name="child-elements"></a><span data-ttu-id="159ca-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="159ca-115">Child elements</span></span>

> [!NOTE]
> <span data-ttu-id="159ca-116">Les paramètres *Duration* et *WaitTimeout* sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="159ca-116">The *Duration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="159ca-117">Elles sont toujours présentes dans l’interface utilisateur Planificateur de tâches et leurs méthodes d’interface peuvent toujours retourner des valeurs valides, mais elles ne sont plus utilisées.</span><span class="sxs-lookup"><span data-stu-id="159ca-117">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="159ca-118">Élément</span><span class="sxs-lookup"><span data-stu-id="159ca-118">Element</span></span>                                                                                  | <span data-ttu-id="159ca-119">Type</span><span class="sxs-lookup"><span data-stu-id="159ca-119">Type</span></span>     | <span data-ttu-id="159ca-120">Description</span><span class="sxs-lookup"><span data-stu-id="159ca-120">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="159ca-121">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="159ca-121">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="159ca-122">boolean</span><span class="sxs-lookup"><span data-stu-id="159ca-122">boolean</span></span>  | <span data-ttu-id="159ca-123">Spécifie si la tâche est redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="159ca-123">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>       |
| [<span data-ttu-id="159ca-124">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="159ca-124">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="159ca-125">boolean</span><span class="sxs-lookup"><span data-stu-id="159ca-125">boolean</span></span>  | <span data-ttu-id="159ca-126">Spécifie que l’Planificateur de tâches arrêtera la tâche si la condition d’inactivité se termine avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="159ca-126">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="159ca-127">**Déconseillé**: [ **durée**](taskschedulerschema-duration-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="159ca-127">**Deprecated**: [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)</span></span>                | <span data-ttu-id="159ca-128">duration</span><span class="sxs-lookup"><span data-stu-id="159ca-128">duration</span></span> | <span data-ttu-id="159ca-129">Spécifie la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche ne soit exécutée.</span><span class="sxs-lookup"><span data-stu-id="159ca-129">Specifies how long the computer must be in an idle state before the task is run.</span></span><br/>                              |
| <span data-ttu-id="159ca-130">**Déconseillé**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="159ca-130">**Deprecated**: [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span></span>          | <span data-ttu-id="159ca-131">duration</span><span class="sxs-lookup"><span data-stu-id="159ca-131">duration</span></span> | <span data-ttu-id="159ca-132">Spécifie la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="159ca-132">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                |

## <a name="remarks"></a><span data-ttu-id="159ca-133">Notes</span><span class="sxs-lookup"><span data-stu-id="159ca-133">Remarks</span></span>

<span data-ttu-id="159ca-134">Pour le développement de scripts, les paramètres inactifs sont spécifiés à l’aide de la propriété [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="159ca-134">For script development, idle settings are specified using the [**TaskSettings.IdleSettings**](tasksettings-idlesettings.md) property.</span></span>

<span data-ttu-id="159ca-135">Pour le développement C++, les paramètres inactifs sont spécifiés à l’aide de la propriété [**ITaskSettings :: IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .</span><span class="sxs-lookup"><span data-stu-id="159ca-135">For C++ development, idle settings are specified using the [**ITaskSettings::IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="159ca-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="159ca-136">Examples</span></span>

<span data-ttu-id="159ca-137">Le code XML suivant définit un élément Settings qui permet à Planificateur de tâches d’attendre 24 heures pour une condition d’inactivité, puis autorise uniquement 10 minutes {IdleDuration) à lancer la tâche.</span><span class="sxs-lookup"><span data-stu-id="159ca-137">The following XML defines a settings element that allows Task Scheduler to wait 24 hours for an idle condition and then allows only 10 minutes {IdleDuration) to initiate the task.</span></span>

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a><span data-ttu-id="159ca-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="159ca-138">Requirements</span></span>

| <span data-ttu-id="159ca-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="159ca-139">Requirement</span></span> | <span data-ttu-id="159ca-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="159ca-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="159ca-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="159ca-141">Minimum supported client</span></span><br/> | <span data-ttu-id="159ca-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="159ca-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="159ca-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="159ca-143">Minimum supported server</span></span><br/> | <span data-ttu-id="159ca-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="159ca-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="159ca-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="159ca-145">See also</span></span>

[<span data-ttu-id="159ca-146">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="159ca-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="159ca-147">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="159ca-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
