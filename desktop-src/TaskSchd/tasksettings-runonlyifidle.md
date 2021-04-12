---
title: TaskSettings. RunOnlyIfIdle, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement si l’ordinateur est dans une condition d’inactivité.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Planificateur de tâches de la propriété RunOnlyIfIdle
- Planificateur de tâches de la propriété RunOnlyIfIdle, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété RunOnlyIfIdle
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384343"
---
# <a name="tasksettingsrunonlyifidle-property"></a><span data-ttu-id="b6c5e-106">TaskSettings. RunOnlyIfIdle, propriété</span><span class="sxs-lookup"><span data-stu-id="b6c5e-106">TaskSettings.RunOnlyIfIdle property</span></span>

<span data-ttu-id="b6c5e-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement si l’ordinateur est dans une condition d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="b6c5e-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span>

<span data-ttu-id="b6c5e-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b6c5e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c5e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6c5e-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b6c5e-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b6c5e-110">Property value</span></span>

<span data-ttu-id="b6c5e-111">Si la valeur est true, la propriété indique que le Planificateur de tâches exécutera la tâche uniquement si l’ordinateur est dans une condition d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="b6c5e-111">If True, the property indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span> <span data-ttu-id="b6c5e-112">La valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="b6c5e-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6c5e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b6c5e-113">Remarks</span></span>

<span data-ttu-id="b6c5e-114">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="b6c5e-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c5e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6c5e-115">Requirements</span></span>



| <span data-ttu-id="b6c5e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6c5e-116">Requirement</span></span> | <span data-ttu-id="b6c5e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6c5e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c5e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6c5e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c5e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6c5e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b6c5e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6c5e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c5e-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6c5e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6c5e-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b6c5e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6c5e-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6c5e-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6c5e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b6c5e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6c5e-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6c5e-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c5e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6c5e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c5e-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b6c5e-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





