---
title: TaskSettings. WakeToRun, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Planificateur de tâches de la propriété WakeToRun
- Planificateur de tâches de la propriété WakeToRun, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété WakeToRun
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740804"
---
# <a name="tasksettingswaketorun-property"></a><span data-ttu-id="aaa60-106">TaskSettings. WakeToRun, propriété</span><span class="sxs-lookup"><span data-stu-id="aaa60-106">TaskSettings.WakeToRun property</span></span>

<span data-ttu-id="aaa60-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="aaa60-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

<span data-ttu-id="aaa60-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="aaa60-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaa60-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaa60-109">Syntax</span></span>


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a><span data-ttu-id="aaa60-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="aaa60-110">Property value</span></span>

<span data-ttu-id="aaa60-111">Si la valeur est true, la propriété indique que la Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="aaa60-111">If True, the property indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaa60-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aaa60-112">Remarks</span></span>

<span data-ttu-id="aaa60-113">Lorsque le service Planificateur de tâches sort de l’ordinateur pour exécuter une tâche, l’écran peut rester inactif même si l’ordinateur n’est plus en mode veille ou veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="aaa60-113">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="aaa60-114">L’écran s’active lorsque Windows Vista détecte qu’un utilisateur a retourné pour utiliser l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="aaa60-114">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="aaa60-115">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="aaa60-115">When reading or writing XML for a task, this setting is specified in the [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa60-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaa60-116">Requirements</span></span>



| <span data-ttu-id="aaa60-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaa60-117">Requirement</span></span> | <span data-ttu-id="aaa60-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaa60-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa60-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaa60-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa60-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aaa60-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aaa60-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aaa60-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa60-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aaa60-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aaa60-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="aaa60-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="aaa60-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aaa60-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aaa60-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aaa60-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaa60-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaa60-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaa60-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaa60-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa60-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="aaa60-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





