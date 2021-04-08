---
title: ExecAction. arguments, propriété
description: Pour les scripts, obtient ou définit les arguments associés à l’opération de ligne de commande.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments, propriété Planificateur de tâches
- Arguments, propriété Planificateur de tâches, objet ExecAction
- Planificateur de tâches objet ExecAction, propriété arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941897"
---
# <a name="execactionarguments-property"></a><span data-ttu-id="f27a0-106">ExecAction. arguments, propriété</span><span class="sxs-lookup"><span data-stu-id="f27a0-106">ExecAction.Arguments property</span></span>

<span data-ttu-id="f27a0-107">Pour les scripts, obtient ou définit les arguments associés à l’opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f27a0-107">For scripting, gets or sets the arguments associated with the command-line operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f27a0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f27a0-108">Syntax</span></span>


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a><span data-ttu-id="f27a0-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f27a0-109">Property value</span></span>

<span data-ttu-id="f27a0-110">Arguments requis par l’opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f27a0-110">The arguments that are needed by the command-line operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f27a0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f27a0-111">Remarks</span></span>

<span data-ttu-id="f27a0-112">Lors de la lecture ou de l’écriture de données XML, les arguments de l’opération de ligne de commande sont spécifiés dans l’élément [**arguments**](taskschedulerschema-arguments-exectype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="f27a0-112">When reading or writing XML, the command-line operation arguments are specified in the [**Arguments**](taskschedulerschema-arguments-exectype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f27a0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f27a0-113">Requirements</span></span>



| <span data-ttu-id="f27a0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f27a0-114">Requirement</span></span> | <span data-ttu-id="f27a0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f27a0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f27a0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f27a0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f27a0-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f27a0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f27a0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f27a0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f27a0-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f27a0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f27a0-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f27a0-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="f27a0-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f27a0-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f27a0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f27a0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f27a0-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f27a0-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f27a0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f27a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f27a0-125">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="f27a0-125">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="f27a0-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="f27a0-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





