---
title: TaskSettings. IdleSettings, propriété
description: Pour les scripts, obtient ou définit les informations qui spécifient la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans une condition d’inactivité.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Planificateur de tâches de la propriété IdleSettings
- Planificateur de tâches de la propriété IdleSettings, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété IdleSettings
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518093"
---
# <a name="tasksettingsidlesettings-property"></a><span data-ttu-id="7f0c4-106">TaskSettings. IdleSettings, propriété</span><span class="sxs-lookup"><span data-stu-id="7f0c4-106">TaskSettings.IdleSettings property</span></span>

<span data-ttu-id="7f0c4-107">Pour les scripts, obtient ou définit les informations qui spécifient la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans une condition d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-107">For scripting, gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="7f0c4-108">Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="7f0c4-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="7f0c4-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f0c4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f0c4-110">Syntax</span></span>


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a><span data-ttu-id="7f0c4-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7f0c4-111">Property value</span></span>

<span data-ttu-id="7f0c4-112">Objet [**IdleSettings**](idlesettings.md) qui spécifie la façon dont le planificateur de tâches gère la tâche lorsque l’ordinateur passe en état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-112">An [**IdleSettings**](idlesettings.md) object that specifies how the Task Scheduler handles the task when the computer goes into an idle condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f0c4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7f0c4-113">Remarks</span></span>

<span data-ttu-id="7f0c4-114">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-114">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f0c4-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f0c4-115">Requirements</span></span>



| <span data-ttu-id="7f0c4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f0c4-116">Requirement</span></span> | <span data-ttu-id="7f0c4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f0c4-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f0c4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f0c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7f0c4-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f0c4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7f0c4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f0c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7f0c4-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f0c4-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f0c4-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7f0c4-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f0c4-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7f0c4-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7f0c4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7f0c4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f0c4-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f0c4-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f0c4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f0c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f0c4-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7f0c4-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





