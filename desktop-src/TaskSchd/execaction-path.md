---
title: ExecAction. Path, propriété
description: Pour les scripts, obtient ou définit le chemin d’accès à un fichier exécutable.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Propriété Path Planificateur de tâches
- Propriété Path Planificateur de tâches, objet ExecAction
- Planificateur de tâches objet ExecAction, propriété Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740860"
---
# <a name="execactionpath-property"></a><span data-ttu-id="4f6fd-106">ExecAction. Path, propriété</span><span class="sxs-lookup"><span data-stu-id="4f6fd-106">ExecAction.Path property</span></span>

<span data-ttu-id="4f6fd-107">Pour les scripts, obtient ou définit le chemin d’accès à un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="4f6fd-107">For scripting, gets or sets the path to an executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f6fd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f6fd-108">Syntax</span></span>


```VB
ExecAction.Path As String
```



## <a name="property-value"></a><span data-ttu-id="4f6fd-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4f6fd-109">Property value</span></span>

<span data-ttu-id="4f6fd-110">Chemin d’accès au fichier exécutable à exécuter par l’action.</span><span class="sxs-lookup"><span data-stu-id="4f6fd-110">The path to the executable file to be run by the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f6fd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4f6fd-111">Remarks</span></span>

<span data-ttu-id="4f6fd-112">Cette action effectue une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4f6fd-112">This action performs a command-line operation.</span></span> <span data-ttu-id="4f6fd-113">Par exemple, l’action peut exécuter un script ou lancer un exécutable.</span><span class="sxs-lookup"><span data-stu-id="4f6fd-113">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="4f6fd-114">Lors de la lecture ou de l’écriture de données XML, le chemin d’accès de l’opération de ligne de commande est spécifié dans l’élément [**Command**](taskschedulerschema-command-exectype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="4f6fd-114">When reading or writing XML, the command-line operation path is specified in the [**Command**](taskschedulerschema-command-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="4f6fd-115">Le chemin d’accès est vérifié pour s’assurer qu’il est valide lorsque la tâche est inscrite, et non lorsque cette propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="4f6fd-115">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f6fd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f6fd-116">Requirements</span></span>



| <span data-ttu-id="4f6fd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f6fd-117">Requirement</span></span> | <span data-ttu-id="4f6fd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f6fd-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6fd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f6fd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f6fd-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f6fd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4f6fd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f6fd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f6fd-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f6fd-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f6fd-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4f6fd-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f6fd-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f6fd-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f6fd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4f6fd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f6fd-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f6fd-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f6fd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f6fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f6fd-128">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="4f6fd-128">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="4f6fd-129">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4f6fd-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





