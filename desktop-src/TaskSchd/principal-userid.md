---
title: Propriété principal. UserId
description: Pour les scripts, obtient ou définit l’identificateur de l’utilisateur qui est requis pour exécuter les tâches associées au principal.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserId, propriété Planificateur de tâches
- UserId, propriété Planificateur de tâches, objet principal
- Objet principal Planificateur de tâches, propriété UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104356"
---
# <a name="principaluserid-property"></a><span data-ttu-id="215ce-106">Propriété principal. UserId</span><span class="sxs-lookup"><span data-stu-id="215ce-106">Principal.UserId property</span></span>

<span data-ttu-id="215ce-107">Pour les scripts, obtient ou définit l’identificateur de l’utilisateur qui est requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="215ce-107">For scripting, gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="215ce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="215ce-108">Syntax</span></span>


```VB
Principal.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="215ce-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="215ce-109">Property value</span></span>

<span data-ttu-id="215ce-110">Identificateur d’utilisateur requis pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="215ce-110">The user identifier that is required to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="215ce-111">Notes</span><span class="sxs-lookup"><span data-stu-id="215ce-111">Remarks</span></span>

<span data-ttu-id="215ce-112">Ne définissez pas cette propriété si un identificateur de groupe est spécifié dans la propriété [**GroupID**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="215ce-112">Do not set this property if a group identifier is specified in the [**GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="215ce-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur d’utilisateur du principal est spécifié à l’aide de l’élément [**userid**](taskschedulerschema-userid-principaltype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="215ce-113">When reading or writing XML for a task, the user identifier for the principal is specified using the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="215ce-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="215ce-114">Requirements</span></span>



| <span data-ttu-id="215ce-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="215ce-115">Requirement</span></span> | <span data-ttu-id="215ce-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="215ce-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="215ce-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="215ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="215ce-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="215ce-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="215ce-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="215ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="215ce-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="215ce-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="215ce-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="215ce-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="215ce-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="215ce-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="215ce-123">DLL</span><span class="sxs-lookup"><span data-stu-id="215ce-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="215ce-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="215ce-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="215ce-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="215ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215ce-126">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="215ce-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="215ce-127">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="215ce-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="215ce-128">**Principal. GroupId**</span><span class="sxs-lookup"><span data-stu-id="215ce-128">**Principal.GroupId**</span></span>](principal-groupid.md)
</dt> </dl>

 

 





