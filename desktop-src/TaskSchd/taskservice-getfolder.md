---
title: TaskService. GetFolder, méthode
description: Pour les scripts, obtient un dossier de tâches inscrites.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Méthode GetFolder Planificateur de tâches
- Méthode GetFolder Planificateur de tâches, objet TaskService
- Objet TaskService Planificateur de tâches, méthode GetFolder
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387098"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="e4544-106">TaskService. GetFolder, méthode</span><span class="sxs-lookup"><span data-stu-id="e4544-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="e4544-107">Pour les scripts, obtient un dossier de tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="e4544-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4544-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4544-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="e4544-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4544-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4544-110">*chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4544-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4544-111">Chemin d’accès au dossier à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e4544-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="e4544-112">N’utilisez pas de barre oblique inverse à la suite du nom du dernier dossier dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="e4544-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="e4544-113">Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="e4544-113">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="e4544-114">Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="e4544-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="e4544-115">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="e4544-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="e4544-116">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="e4544-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4544-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e4544-117">Return value</span></span>

<span data-ttu-id="e4544-118">Objet [**TaskFolder**](taskfolder.md) pour le dossier demandé.</span><span class="sxs-lookup"><span data-stu-id="e4544-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4544-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e4544-119">Requirements</span></span>



| <span data-ttu-id="e4544-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4544-120">Requirement</span></span> | <span data-ttu-id="e4544-121">Value</span><span class="sxs-lookup"><span data-stu-id="e4544-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4544-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4544-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e4544-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4544-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e4544-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4544-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e4544-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4544-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4544-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e4544-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="e4544-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e4544-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e4544-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e4544-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4544-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4544-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4544-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4544-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4544-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="e4544-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





