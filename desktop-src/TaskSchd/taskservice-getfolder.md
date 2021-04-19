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
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510368"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="0605b-106">TaskService. GetFolder, méthode</span><span class="sxs-lookup"><span data-stu-id="0605b-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="0605b-107">Pour les scripts, obtient un dossier de tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="0605b-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="0605b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0605b-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="0605b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0605b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0605b-110">*chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0605b-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0605b-111">Chemin d’accès au dossier à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0605b-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="0605b-112">N’utilisez pas de barre oblique inverse à la suite du nom du dernier dossier dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="0605b-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="0605b-113">Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \) .</span><span class="sxs-lookup"><span data-stu-id="0605b-113">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="0605b-114">Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="0605b-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="0605b-115">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="0605b-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="0605b-116">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="0605b-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0605b-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0605b-117">Return value</span></span>

<span data-ttu-id="0605b-118">Objet [**TaskFolder**](taskfolder.md) pour le dossier demandé.</span><span class="sxs-lookup"><span data-stu-id="0605b-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="0605b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0605b-119">Requirements</span></span>



| <span data-ttu-id="0605b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0605b-120">Requirement</span></span> | <span data-ttu-id="0605b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0605b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0605b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0605b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0605b-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0605b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0605b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0605b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0605b-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0605b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0605b-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0605b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="0605b-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0605b-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0605b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0605b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0605b-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0605b-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0605b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0605b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0605b-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0605b-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





