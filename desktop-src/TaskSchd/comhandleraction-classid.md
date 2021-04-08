---
title: ComHandlerAction. ClassId, propriété
description: Pour les scripts, obtient ou définit l’identificateur de la classe de gestionnaire.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Propriété ClassId Planificateur de tâches
- ClassId, propriété Planificateur de tâches, objet ComHandlerAction
- Objet ComHandlerAction Planificateur de tâches, propriété ClassId
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740868"
---
# <a name="comhandleractionclassid-property"></a><span data-ttu-id="b518b-106">ComHandlerAction. ClassId, propriété</span><span class="sxs-lookup"><span data-stu-id="b518b-106">ComHandlerAction.ClassId property</span></span>

<span data-ttu-id="b518b-107">Pour les scripts, obtient ou définit l’identificateur de la classe de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="b518b-107">For scripting, gets or sets the identifier of the handler class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b518b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b518b-108">Syntax</span></span>


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a><span data-ttu-id="b518b-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b518b-109">Property value</span></span>

<span data-ttu-id="b518b-110">Identificateur de la classe qui définit le gestionnaire à déclencher.</span><span class="sxs-lookup"><span data-stu-id="b518b-110">The identifier of the class that defines the handler to be fired.</span></span>

## <a name="remarks"></a><span data-ttu-id="b518b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b518b-111">Remarks</span></span>

<span data-ttu-id="b518b-112">Lors de la lecture ou de l’écriture de données XML, la classe d’un gestionnaire COM est spécifiée dans l’élément [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="b518b-112">When reading or writing XML, the class of a COM handler is specified in the [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b518b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b518b-113">Requirements</span></span>



| <span data-ttu-id="b518b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b518b-114">Requirement</span></span> | <span data-ttu-id="b518b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b518b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b518b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b518b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b518b-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b518b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b518b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b518b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b518b-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b518b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b518b-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b518b-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="b518b-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b518b-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b518b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b518b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b518b-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b518b-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b518b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b518b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b518b-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="b518b-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b518b-126">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="b518b-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





