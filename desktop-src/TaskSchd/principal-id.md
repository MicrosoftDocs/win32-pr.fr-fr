---
title: Propriété Principal.Id
description: Pour les scripts, obtient ou définit l’identificateur du principal.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Propriété ID Planificateur de tâches
- ID de propriété Planificateur de tâches, objet principal
- Planificateur de tâches de l’objet principal, propriété ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385008"
---
# <a name="principalid-property"></a><span data-ttu-id="1c309-106">Propriété Principal.Id</span><span class="sxs-lookup"><span data-stu-id="1c309-106">Principal.Id property</span></span>

<span data-ttu-id="1c309-107">Pour les scripts, obtient ou définit l’identificateur du principal.</span><span class="sxs-lookup"><span data-stu-id="1c309-107">For scripting, gets or sets the identifier of the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c309-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c309-108">Syntax</span></span>


```VB
Principal.Id As String
```



## <a name="property-value"></a><span data-ttu-id="1c309-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1c309-109">Property value</span></span>

<span data-ttu-id="1c309-110">Identificateur du principal.</span><span class="sxs-lookup"><span data-stu-id="1c309-110">The identifier of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c309-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1c309-111">Remarks</span></span>

<span data-ttu-id="1c309-112">Cet identificateur est également utilisé lors de la spécification de la propriété [**ActionCollection. Context**](actioncollection-context.md) .</span><span class="sxs-lookup"><span data-stu-id="1c309-112">This identifier is also used when specifying the [**ActionCollection.Context**](actioncollection-context.md) property.</span></span>

<span data-ttu-id="1c309-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur de l’entité de sécurité est spécifié dans l’attribut ID de l’élément [**principal**](taskschedulerschema-principal-principaltype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="1c309-113">When reading or writing XML for a task, the identifier of the principal is specified in the Id attribute of the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c309-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c309-114">Requirements</span></span>



| <span data-ttu-id="1c309-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c309-115">Requirement</span></span> | <span data-ttu-id="1c309-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c309-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c309-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c309-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c309-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c309-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1c309-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c309-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c309-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c309-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c309-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1c309-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c309-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1c309-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1c309-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1c309-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c309-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c309-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c309-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c309-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c309-126">**ActionCollection. Context**</span><span class="sxs-lookup"><span data-stu-id="1c309-126">**ActionCollection.Context**</span></span>](actioncollection-context.md)
</dt> <dt>

[<span data-ttu-id="1c309-127">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="1c309-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="1c309-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="1c309-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





