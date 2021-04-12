---
title: Objet IdleSettings
description: Objet de script qui spécifie la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans une condition d’inactivité.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Objet IdleSettings Planificateur de tâches
- Planificateur de tâches d’objets IdleSettings, Description
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384367"
---
# <a name="idlesettings-object"></a><span data-ttu-id="599df-105">Objet IdleSettings</span><span class="sxs-lookup"><span data-stu-id="599df-105">IdleSettings object</span></span>

<span data-ttu-id="599df-106">Objet de script qui spécifie la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans une condition d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="599df-106">A scripting object that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="599df-107">Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="599df-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="599df-108">Membres</span><span class="sxs-lookup"><span data-stu-id="599df-108">Members</span></span>

<span data-ttu-id="599df-109">L’objet **IdleSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="599df-109">The **IdleSettings** object has these types of members:</span></span>

- [<span data-ttu-id="599df-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="599df-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="599df-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="599df-111">Properties</span></span>

<span data-ttu-id="599df-112">L’objet **IdleSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="599df-112">The **IdleSettings** object has these properties.</span></span>

> [!NOTE]
> <span data-ttu-id="599df-113">Les paramètres *IdleDuration* et *WaitTimeout* sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="599df-113">The *IdleDuration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="599df-114">Elles sont toujours présentes dans l’interface utilisateur Planificateur de tâches et leurs méthodes d’interface peuvent toujours retourner des valeurs valides, mais elles ne sont plus utilisées.</span><span class="sxs-lookup"><span data-stu-id="599df-114">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="599df-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="599df-115">Property</span></span>                                                       | <span data-ttu-id="599df-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="599df-116">Access type</span></span>           | <span data-ttu-id="599df-117">Description</span><span class="sxs-lookup"><span data-stu-id="599df-117">Description</span></span>                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="599df-118">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="599df-118">**RestartOnIdle**</span></span>](idlesettings-restartonidle.md)<br/> | <span data-ttu-id="599df-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="599df-119">Read/write</span></span><br/> | <span data-ttu-id="599df-120">Obtient ou définit une valeur booléenne qui indique si la tâche est redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="599df-120">Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>            |
| [<span data-ttu-id="599df-121">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="599df-121">**StopOnIdleEnd**</span></span>](idlesettings-stoponidleend.md)<br/> | <span data-ttu-id="599df-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="599df-122">Read/write</span></span><br/> | <span data-ttu-id="599df-123">Obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met fin à la tâche si la condition d’inactivité se termine avant la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="599df-123">Gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="599df-124">**Déconseillé**: [ **IdleDuration**](idlesettings-idleduration.md)</span><span class="sxs-lookup"><span data-stu-id="599df-124">**Deprecated**: [**IdleDuration**](idlesettings-idleduration.md)</span></span><br/>   | <span data-ttu-id="599df-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="599df-125">Read/write</span></span><br/> | <span data-ttu-id="599df-126">Obtient ou définit une valeur qui indique la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche soit exécutée.</span><span class="sxs-lookup"><span data-stu-id="599df-126">Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span><br/>                            |
| <span data-ttu-id="599df-127">**Déconseillé**: [ **WaitTimeout**](idlesettings-waittimeout.md)</span><span class="sxs-lookup"><span data-stu-id="599df-127">**Deprecated**: [**WaitTimeout**](idlesettings-waittimeout.md)</span></span><br/>     | <span data-ttu-id="599df-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="599df-128">Read/write</span></span><br/> | <span data-ttu-id="599df-129">Obtient ou définit une valeur qui indique la durée pendant laquelle le Planificateur de tâches attendra qu’une condition d’inactivité se produise.</span><span class="sxs-lookup"><span data-stu-id="599df-129">Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                             |

## <a name="remarks"></a><span data-ttu-id="599df-130">Notes</span><span class="sxs-lookup"><span data-stu-id="599df-130">Remarks</span></span>

<span data-ttu-id="599df-131">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="599df-131">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="599df-132">Si une tâche est déclenchée par un déclencheur inactif, la propriété [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) est ignorée.</span><span class="sxs-lookup"><span data-stu-id="599df-132">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="599df-133">*IdleSettings. IdleDuration* et *IdleSettings. WaitTimeout* sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="599df-133">*IdleSettings.IdleDuration* and *IdleSettings.WaitTimeout* are deprecated.</span></span>

## <a name="requirements"></a><span data-ttu-id="599df-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="599df-134">Requirements</span></span>

| <span data-ttu-id="599df-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="599df-135">Requirement</span></span> | <span data-ttu-id="599df-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="599df-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="599df-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="599df-137">Minimum supported client</span></span><br/> | <span data-ttu-id="599df-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="599df-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="599df-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="599df-139">Minimum supported server</span></span><br/> | <span data-ttu-id="599df-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="599df-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="599df-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="599df-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="599df-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="599df-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="599df-143">DLL</span><span class="sxs-lookup"><span data-stu-id="599df-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="599df-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="599df-144"><dt>Taskschd.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="599df-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="599df-145">See also</span></span>

[<span data-ttu-id="599df-146">Objets Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="599df-146">Task Scheduler Objects</span></span>](task-scheduler-objects.md)

[<span data-ttu-id="599df-147">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="599df-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
