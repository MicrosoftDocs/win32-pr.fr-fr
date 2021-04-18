---
title: IdleSettings. RestartOnIdle, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique si la tâche est redémarrée lorsque l’ordinateur est à plusieurs reprises dans une condition d’inactivité.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Planificateur de tâches de la propriété RestartOnIdle
- Planificateur de tâches de la propriété RestartOnIdle, objet IdleSettings
- Planificateur de tâches objet IdleSettings, propriété RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543052"
---
# <a name="idlesettingsrestartonidle-property"></a><span data-ttu-id="4b8a2-106">IdleSettings. RestartOnIdle, propriété</span><span class="sxs-lookup"><span data-stu-id="4b8a2-106">IdleSettings.RestartOnIdle property</span></span>

<span data-ttu-id="4b8a2-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique si la tâche est redémarrée lorsque l’ordinateur est à plusieurs reprises dans une condition d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="4b8a2-107">For scripting, gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8a2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b8a2-108">Syntax</span></span>


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="4b8a2-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4b8a2-109">Property value</span></span>

<span data-ttu-id="4b8a2-110">Valeur booléenne qui indique si la tâche doit être redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="4b8a2-110">A Boolean value that indicates whether the task must be restarted when the computer cycles into an idle condition more than once.</span></span> <span data-ttu-id="4b8a2-111">La valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="4b8a2-111">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b8a2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4b8a2-112">Remarks</span></span>

<span data-ttu-id="4b8a2-113">Cette propriété est utilisée uniquement si la propriété [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="4b8a2-113">This property is only used if the [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) property is set to True.</span></span>

<span data-ttu-id="4b8a2-114">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="4b8a2-114">When reading or writing XML for a task, this setting is specified in the [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8a2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b8a2-115">Requirements</span></span>



| <span data-ttu-id="4b8a2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b8a2-116">Requirement</span></span> | <span data-ttu-id="4b8a2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b8a2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8a2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b8a2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8a2-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b8a2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4b8a2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b8a2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8a2-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b8a2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b8a2-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4b8a2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b8a2-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4b8a2-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4b8a2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4b8a2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b8a2-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b8a2-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b8a2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b8a2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8a2-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4b8a2-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4b8a2-128">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="4b8a2-128">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





