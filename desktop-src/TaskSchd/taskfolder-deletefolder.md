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
ms.openlocfilehash: 31080f017329cde376b646befd4b7e12ba02926b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387038"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="c1a52-106">Méthode TaskFolder. DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="c1a52-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="c1a52-107">Pour les scripts, supprime un sous-dossier du dossier parent.</span><span class="sxs-lookup"><span data-stu-id="c1a52-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a52-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1a52-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="c1a52-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1a52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a52-110">*NomDossier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1a52-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a52-111">Nom du sous-dossier à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c1a52-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="c1a52-112">Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="c1a52-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="c1a52-113">Ce paramètre peut être un chemin d’accès relatif au dossier que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="c1a52-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="c1a52-114">Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="c1a52-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="c1a52-115">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="c1a52-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="c1a52-116">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="c1a52-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="c1a52-117">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1a52-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a52-118">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c1a52-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a52-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c1a52-119">Return value</span></span>

<span data-ttu-id="c1a52-120">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c1a52-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a52-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c1a52-121">Requirements</span></span>



| <span data-ttu-id="c1a52-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1a52-122">Requirement</span></span> | <span data-ttu-id="c1a52-123">Value</span><span class="sxs-lookup"><span data-stu-id="c1a52-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a52-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1a52-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c1a52-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1a52-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c1a52-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1a52-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c1a52-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1a52-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1a52-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c1a52-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1a52-129"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1a52-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1a52-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c1a52-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1a52-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1a52-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a52-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1a52-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a52-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="c1a52-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="c1a52-134">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c1a52-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





