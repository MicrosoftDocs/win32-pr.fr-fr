---
title: TaskSettings. RestartCount, propriété
description: Pour les scripts, obtient ou définit le nombre de fois que l’Planificateur de tâches tente de redémarrer la tâche.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Planificateur de tâches de la propriété RestartCount
- Planificateur de tâches de la propriété RestartCount, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété RestartCount
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384344"
---
# <a name="tasksettingsrestartcount-property"></a><span data-ttu-id="5edc7-106">TaskSettings. RestartCount, propriété</span><span class="sxs-lookup"><span data-stu-id="5edc7-106">TaskSettings.RestartCount property</span></span>

<span data-ttu-id="5edc7-107">Pour les scripts, obtient ou définit le nombre de fois que l’Planificateur de tâches tente de redémarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="5edc7-107">For scripting, gets or sets the number of times that the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="5edc7-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5edc7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5edc7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5edc7-109">Syntax</span></span>


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a><span data-ttu-id="5edc7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5edc7-110">Property value</span></span>

<span data-ttu-id="5edc7-111">Nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="5edc7-111">The number of times that the Task Scheduler will attempt to restart the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="5edc7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5edc7-112">Remarks</span></span>

<span data-ttu-id="5edc7-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Count**](taskschedulerschema-count-restarttype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="5edc7-113">When reading or writing XML for a task, this setting is specified in the [**Count**](taskschedulerschema-count-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5edc7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5edc7-114">Requirements</span></span>



| <span data-ttu-id="5edc7-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5edc7-115">Requirement</span></span> | <span data-ttu-id="5edc7-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5edc7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5edc7-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5edc7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5edc7-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5edc7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5edc7-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5edc7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5edc7-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5edc7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5edc7-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5edc7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="5edc7-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5edc7-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5edc7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5edc7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5edc7-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5edc7-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5edc7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5edc7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5edc7-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="5edc7-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





