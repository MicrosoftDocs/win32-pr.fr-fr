---
title: ExecAction. WorkingDirectory, propriété
description: Pour les scripts, obtient ou définit le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Planificateur de tâches de la propriété WorkingDirectory
- Planificateur de tâches de la propriété WorkingDirectory, objet ExecAction
- Planificateur de tâches objet ExecAction, propriété WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509912"
---
# <a name="execactionworkingdirectory-property"></a><span data-ttu-id="49224-106">ExecAction. WorkingDirectory, propriété</span><span class="sxs-lookup"><span data-stu-id="49224-106">ExecAction.WorkingDirectory property</span></span>

<span data-ttu-id="49224-107">Pour les scripts, obtient ou définit le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="49224-107">For scripting, gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="49224-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49224-108">Syntax</span></span>


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a><span data-ttu-id="49224-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="49224-109">Property value</span></span>

<span data-ttu-id="49224-110">Le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="49224-110">The directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="49224-111">Notes</span><span class="sxs-lookup"><span data-stu-id="49224-111">Remarks</span></span>

<span data-ttu-id="49224-112">Lors de la lecture ou de l’écriture de code XML, le répertoire de travail de l’application est spécifié dans l’élément [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="49224-112">When reading or writing XML, the working directory of the application is specified in the [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="49224-113">Le chemin d’accès est vérifié pour s’assurer qu’il est valide lorsque la tâche est inscrite, et non lorsque cette propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="49224-113">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="49224-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49224-114">Requirements</span></span>



| <span data-ttu-id="49224-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49224-115">Requirement</span></span> | <span data-ttu-id="49224-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="49224-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49224-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49224-117">Minimum supported client</span></span><br/> | <span data-ttu-id="49224-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49224-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="49224-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49224-119">Minimum supported server</span></span><br/> | <span data-ttu-id="49224-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49224-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49224-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="49224-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="49224-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="49224-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="49224-123">DLL</span><span class="sxs-lookup"><span data-stu-id="49224-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49224-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49224-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49224-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49224-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49224-126">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="49224-126">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="49224-127">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="49224-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





