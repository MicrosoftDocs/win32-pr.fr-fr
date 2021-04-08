---
title: Méthode TaskFolder. DeleteTask
description: Pour les scripts, supprime une tâche du dossier.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Planificateur de tâches de la méthode DeleteTask
- Méthode DeleteTask Planificateur de tâches, objet TaskFolder
- Planificateur de tâches objet TaskFolder, méthode DeleteTask
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742173"
---
# <a name="taskfolderdeletetask-method"></a><span data-ttu-id="042fb-106">Méthode TaskFolder. DeleteTask</span><span class="sxs-lookup"><span data-stu-id="042fb-106">TaskFolder.DeleteTask method</span></span>

<span data-ttu-id="042fb-107">Pour les scripts, supprime une tâche du dossier.</span><span class="sxs-lookup"><span data-stu-id="042fb-107">For scripting, deletes a task from the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="042fb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="042fb-108">Syntax</span></span>


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="042fb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="042fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="042fb-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="042fb-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="042fb-111">Nom de la tâche qui est spécifiée lors de l’inscription de la tâche.</span><span class="sxs-lookup"><span data-stu-id="042fb-111">The name of the task that is specified when the task was registered.</span></span> <span data-ttu-id="042fb-112">Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. '</span><span class="sxs-lookup"><span data-stu-id="042fb-112">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="042fb-113">les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="042fb-113">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="042fb-114">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="042fb-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="042fb-115">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="042fb-115">Not supported.</span></span> <span data-ttu-id="042fb-116">La valeur est 0</span><span class="sxs-lookup"><span data-stu-id="042fb-116">Value is 0</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="042fb-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="042fb-117">Return value</span></span>

<span data-ttu-id="042fb-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="042fb-118">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="042fb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="042fb-119">Requirements</span></span>



| <span data-ttu-id="042fb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="042fb-120">Requirement</span></span> | <span data-ttu-id="042fb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="042fb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="042fb-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="042fb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="042fb-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="042fb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="042fb-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="042fb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="042fb-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="042fb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="042fb-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="042fb-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="042fb-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="042fb-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="042fb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="042fb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="042fb-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="042fb-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="042fb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="042fb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="042fb-131">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="042fb-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





