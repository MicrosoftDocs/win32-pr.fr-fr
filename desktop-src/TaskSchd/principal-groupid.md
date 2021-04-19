---
title: Propriété principal. GroupId
description: Pour les scripts, obtient ou définit l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Propriété GroupId Planificateur de tâches
- Propriété GroupId Planificateur de tâches, objet principal
- Objet principal Planificateur de tâches, propriété GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509730"
---
# <a name="principalgroupid-property"></a><span data-ttu-id="bd207-106">Propriété principal. GroupId</span><span class="sxs-lookup"><span data-stu-id="bd207-106">Principal.GroupId property</span></span>

<span data-ttu-id="bd207-107">Pour les scripts, obtient ou définit l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.</span><span class="sxs-lookup"><span data-stu-id="bd207-107">For scripting, gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd207-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd207-108">Syntax</span></span>


```VB
Principal.GroupId As String
```



## <a name="property-value"></a><span data-ttu-id="bd207-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bd207-109">Property value</span></span>

<span data-ttu-id="bd207-110">Identificateur du groupe d’utilisateurs associé à ce principal.</span><span class="sxs-lookup"><span data-stu-id="bd207-110">The identifier of the user group that is associated with this principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd207-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bd207-111">Remarks</span></span>

<span data-ttu-id="bd207-112">Ne définissez pas cette propriété si un identificateur d’utilisateur est spécifié dans la propriété [**userid**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="bd207-112">Do not set this property if a user identifier is specified in the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="bd207-113">Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur de groupe pour un principal est spécifié dans l’élément [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="bd207-113">When reading or writing XML for a task, the group identifier for a principal is specified in the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd207-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd207-114">Requirements</span></span>



| <span data-ttu-id="bd207-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd207-115">Requirement</span></span> | <span data-ttu-id="bd207-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd207-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd207-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd207-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd207-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd207-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bd207-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd207-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd207-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd207-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd207-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bd207-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd207-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bd207-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bd207-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bd207-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd207-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd207-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd207-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd207-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd207-126">**IDutilisateur**</span><span class="sxs-lookup"><span data-stu-id="bd207-126">**UserId**</span></span>](principal-userid.md)
</dt> <dt>

[<span data-ttu-id="bd207-127">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="bd207-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="bd207-128">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="bd207-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





