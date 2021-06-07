---
title: TaskFolder. CreateFolder, méthode
description: Pour les scripts, crée un dossier pour les tâches associées.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- CreateFolder, méthode Planificateur de tâches
- CreateFolder, méthode Planificateur de tâches, objet TaskFolder
- Objet TaskFolder Planificateur de tâches, méthode CreateFolder
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387077"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="d9588-106">TaskFolder. CreateFolder, méthode</span><span class="sxs-lookup"><span data-stu-id="d9588-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="d9588-107">Pour les scripts, crée un dossier pour les tâches associées.</span><span class="sxs-lookup"><span data-stu-id="d9588-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9588-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9588-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="d9588-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9588-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9588-110">*NomDossier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9588-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9588-111">Nom utilisé pour identifier le dossier.</span><span class="sxs-lookup"><span data-stu-id="d9588-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="d9588-112">Si « NomDossier \\ sous \\ SubFolder2 » est spécifié, la totalité de l’arborescence de dossiers est créée si les dossiers n’existent pas.</span><span class="sxs-lookup"><span data-stu-id="d9588-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="d9588-113">Ce paramètre peut être un chemin d’accès relatif à l’instance [**TaskFolder**](taskfolder.md) actuelle.</span><span class="sxs-lookup"><span data-stu-id="d9588-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="d9588-114">Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="d9588-114">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="d9588-115">Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="d9588-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="d9588-116">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="d9588-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="d9588-117">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d9588-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="d9588-118">*langage SDDL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d9588-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9588-119">Descripteur de sécurité associé au dossier.</span><span class="sxs-lookup"><span data-stu-id="d9588-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9588-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d9588-120">Return value</span></span>

<span data-ttu-id="d9588-121">Objet [**TaskFolder**](taskfolder.md) qui représente le nouveau sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="d9588-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9588-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d9588-122">Requirements</span></span>



| <span data-ttu-id="d9588-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9588-123">Requirement</span></span> | <span data-ttu-id="d9588-124">Value</span><span class="sxs-lookup"><span data-stu-id="d9588-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9588-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9588-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9588-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9588-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d9588-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9588-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9588-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9588-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9588-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d9588-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9588-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9588-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9588-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d9588-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9588-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9588-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9588-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9588-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9588-134">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d9588-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





