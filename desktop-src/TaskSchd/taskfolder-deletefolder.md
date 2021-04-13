---
title: Méthode TaskFolder. DeleteFolder
description: Pour les scripts, supprime un sous-dossier du dossier parent.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Planificateur de tâches de la méthode DeleteFolder
- Méthode DeleteFolder Planificateur de tâches, objet TaskFolder
- Planificateur de tâches objet TaskFolder, méthode DeleteFolder
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465818"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="61aa2-106">Méthode TaskFolder. DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="61aa2-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="61aa2-107">Pour les scripts, supprime un sous-dossier du dossier parent.</span><span class="sxs-lookup"><span data-stu-id="61aa2-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="61aa2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61aa2-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="61aa2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61aa2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61aa2-110">*NomDossier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61aa2-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61aa2-111">Nom du sous-dossier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="61aa2-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="61aa2-112">Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \) .</span><span class="sxs-lookup"><span data-stu-id="61aa2-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="61aa2-113">Ce paramètre peut être un chemin d’accès relatif au dossier que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="61aa2-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="61aa2-114">Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="61aa2-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="61aa2-115">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="61aa2-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="61aa2-116">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="61aa2-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="61aa2-117">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61aa2-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61aa2-118">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="61aa2-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61aa2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61aa2-119">Return value</span></span>

<span data-ttu-id="61aa2-120">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="61aa2-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="61aa2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61aa2-121">Requirements</span></span>



| <span data-ttu-id="61aa2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61aa2-122">Requirement</span></span> | <span data-ttu-id="61aa2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="61aa2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61aa2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61aa2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="61aa2-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61aa2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="61aa2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61aa2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="61aa2-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61aa2-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61aa2-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="61aa2-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="61aa2-129"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="61aa2-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="61aa2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="61aa2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61aa2-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61aa2-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61aa2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61aa2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61aa2-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="61aa2-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="61aa2-134">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="61aa2-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





