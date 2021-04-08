---
title: TaskSettings. Hidden, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas visible dans l’interface utilisateur.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Planificateur de tâches de propriétés masquées
- Propriété masquée Planificateur de tâches, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété masquée
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742740"
---
# <a name="tasksettingshidden-property"></a><span data-ttu-id="fd8d7-106">TaskSettings. Hidden, propriété</span><span class="sxs-lookup"><span data-stu-id="fd8d7-106">TaskSettings.Hidden property</span></span>

<span data-ttu-id="fd8d7-107">Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas visible dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd8d7-107">For scripting, gets or sets a Boolean value that indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="fd8d7-108">Toutefois, les administrateurs peuvent remplacer ce paramètre à l’aide d’un « commutateur maître » qui rend toutes les tâches visibles dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd8d7-108">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

<span data-ttu-id="fd8d7-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fd8d7-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8d7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd8d7-110">Syntax</span></span>


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a><span data-ttu-id="fd8d7-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fd8d7-111">Property value</span></span>

<span data-ttu-id="fd8d7-112">Si la valeur est **true**, la valeur indique que la tâche ne sera pas visible dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd8d7-112">If **True**, the value indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="fd8d7-113">Si la **valeur est false**, la tâche est visible dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd8d7-113">If **False**, the task will be visible in the UI.</span></span> <span data-ttu-id="fd8d7-114">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="fd8d7-114">The default is **False**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8d7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fd8d7-115">Remarks</span></span>

<span data-ttu-id="fd8d7-116">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="fd8d7-116">When reading or writing XML for a task, this setting is specified in the [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd8d7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd8d7-117">Requirements</span></span>



| <span data-ttu-id="fd8d7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd8d7-118">Requirement</span></span> | <span data-ttu-id="fd8d7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd8d7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8d7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd8d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd8d7-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd8d7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fd8d7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd8d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd8d7-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd8d7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd8d7-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fd8d7-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd8d7-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d7-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fd8d7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fd8d7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd8d7-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd8d7-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd8d7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd8d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8d7-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="fd8d7-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





