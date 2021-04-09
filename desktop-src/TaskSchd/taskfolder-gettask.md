---
title: TaskFolder. GetTask, propriété
description: Pour les scripts, obtient une tâche à un emplacement spécifié dans un dossier.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Planificateur de tâches de la propriété GetTask
- Planificateur de tâches de la propriété GetTask, objet TaskFolder
- Planificateur de tâches objet TaskFolder, propriété GetTask
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740597"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="eb876-106">TaskFolder. GetTask, propriété</span><span class="sxs-lookup"><span data-stu-id="eb876-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="eb876-107">Pour les scripts, obtient une tâche à un emplacement spécifié dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="eb876-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb876-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb876-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="eb876-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="eb876-109">Property value</span></span>

<span data-ttu-id="eb876-110">Chemin d’accès (emplacement) à la tâche dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="eb876-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="eb876-111">Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \) .</span><span class="sxs-lookup"><span data-stu-id="eb876-111">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="eb876-112">Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="eb876-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="eb876-113">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="eb876-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="eb876-114">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="eb876-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb876-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="eb876-115">Error codes</span></span>

<span data-ttu-id="eb876-116">Tâche à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb876-116">The task at the specified location.</span></span> <span data-ttu-id="eb876-117">La tâche est un objet [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="eb876-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb876-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb876-118">Requirements</span></span>



| <span data-ttu-id="eb876-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb876-119">Requirement</span></span> | <span data-ttu-id="eb876-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb876-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb876-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb876-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eb876-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb876-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eb876-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb876-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eb876-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb876-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb876-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="eb876-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb876-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb876-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb876-127">DLL</span><span class="sxs-lookup"><span data-stu-id="eb876-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb876-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb876-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





