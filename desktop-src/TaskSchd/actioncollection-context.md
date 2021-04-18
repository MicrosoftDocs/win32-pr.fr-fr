---
title: ActionCollection. Context, propriété
description: Pour les scripts, obtient ou définit l’identificateur du principal pour la tâche.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Planificateur de tâches de la propriété de contexte
- Planificateur de tâches de propriété de contexte, objet ActionCollection
- Planificateur de tâches objet ActionCollection, propriété de contexte
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509335"
---
# <a name="actioncollectioncontext-property"></a><span data-ttu-id="bd2e9-106">ActionCollection. Context, propriété</span><span class="sxs-lookup"><span data-stu-id="bd2e9-106">ActionCollection.Context property</span></span>

<span data-ttu-id="bd2e9-107">Pour les scripts, obtient ou définit l’identificateur du principal pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="bd2e9-107">For scripting, gets or sets the identifier of the principal for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd2e9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd2e9-108">Syntax</span></span>


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a><span data-ttu-id="bd2e9-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bd2e9-109">Property value</span></span>

<span data-ttu-id="bd2e9-110">Identificateur du principal de la tâche.</span><span class="sxs-lookup"><span data-stu-id="bd2e9-110">The identifier of the principal for the task.</span></span> <span data-ttu-id="bd2e9-111">L’identificateur spécifié ici doit correspondre à l’identificateur spécifié dans la propriété ID de l’interface IPrincipal qui définit le principal.</span><span class="sxs-lookup"><span data-stu-id="bd2e9-111">The identifier that is specified here must match the identifier that is specified in the Id property of the IPrincipal interface that defines the principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd2e9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd2e9-112">Requirements</span></span>



| <span data-ttu-id="bd2e9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd2e9-113">Requirement</span></span> | <span data-ttu-id="bd2e9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd2e9-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2e9-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd2e9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2e9-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd2e9-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bd2e9-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd2e9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2e9-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd2e9-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd2e9-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bd2e9-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd2e9-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bd2e9-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bd2e9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="bd2e9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd2e9-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd2e9-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd2e9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd2e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd2e9-124">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="bd2e9-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="bd2e9-125">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="bd2e9-125">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





