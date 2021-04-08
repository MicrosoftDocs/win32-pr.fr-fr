---
title: TaskSettings. RunOnlyIfNetworkAvailable, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Planificateur de tâches de la propriété RunOnlyIfNetworkAvailable
- Planificateur de tâches de la propriété RunOnlyIfNetworkAvailable, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844061"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a><span data-ttu-id="d04ba-106">TaskSettings. RunOnlyIfNetworkAvailable, propriété</span><span class="sxs-lookup"><span data-stu-id="d04ba-106">TaskSettings.RunOnlyIfNetworkAvailable property</span></span>

<span data-ttu-id="d04ba-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.</span><span class="sxs-lookup"><span data-stu-id="d04ba-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.</span></span>

<span data-ttu-id="d04ba-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d04ba-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d04ba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d04ba-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d04ba-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d04ba-110">Property value</span></span>

<span data-ttu-id="d04ba-111">Si la valeur est true, la propriété indique que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.</span><span class="sxs-lookup"><span data-stu-id="d04ba-111">If True, the property indicates that the Task Scheduler will run the task only when a network is available.</span></span> <span data-ttu-id="d04ba-112">La valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="d04ba-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="d04ba-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d04ba-113">Remarks</span></span>

<span data-ttu-id="d04ba-114">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="d04ba-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04ba-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d04ba-115">Requirements</span></span>



| <span data-ttu-id="d04ba-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d04ba-116">Requirement</span></span> | <span data-ttu-id="d04ba-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d04ba-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d04ba-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d04ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d04ba-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d04ba-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d04ba-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d04ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d04ba-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d04ba-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d04ba-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d04ba-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="d04ba-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d04ba-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d04ba-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d04ba-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d04ba-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d04ba-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d04ba-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d04ba-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d04ba-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d04ba-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





