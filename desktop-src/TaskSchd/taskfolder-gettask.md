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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387675"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="41d04-106">TaskFolder. GetTask, propriété</span><span class="sxs-lookup"><span data-stu-id="41d04-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="41d04-107">Pour les scripts, obtient une tâche à un emplacement spécifié dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="41d04-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d04-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41d04-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="41d04-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="41d04-109">Property value</span></span>

<span data-ttu-id="41d04-110">Chemin d’accès (emplacement) à la tâche dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="41d04-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="41d04-111">Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="41d04-111">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="41d04-112">Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="41d04-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="41d04-113">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="41d04-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="41d04-114">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="41d04-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="41d04-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="41d04-115">Error codes</span></span>

<span data-ttu-id="41d04-116">Tâche à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="41d04-116">The task at the specified location.</span></span> <span data-ttu-id="41d04-117">La tâche est un objet [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="41d04-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="41d04-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41d04-118">Requirements</span></span>



| <span data-ttu-id="41d04-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41d04-119">Requirement</span></span> | <span data-ttu-id="41d04-120">Value</span><span class="sxs-lookup"><span data-stu-id="41d04-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d04-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41d04-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41d04-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="41d04-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41d04-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41d04-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41d04-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="41d04-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="41d04-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="41d04-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="41d04-127">DLL</span><span class="sxs-lookup"><span data-stu-id="41d04-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41d04-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d04-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





