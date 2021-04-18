---
title: Objet TaskNamedValuePair
description: Objet de script utilisé pour créer une paire nom-valeur dans laquelle le nom est associé à la valeur.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Objet TaskNamedValuePair Planificateur de tâches
- Planificateur de tâches d’objets TaskNamedValuePair, Description
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512786"
---
# <a name="tasknamedvaluepair-object"></a><span data-ttu-id="a489a-105">Objet TaskNamedValuePair</span><span class="sxs-lookup"><span data-stu-id="a489a-105">TaskNamedValuePair object</span></span>

<span data-ttu-id="a489a-106">Objet de script utilisé pour créer une paire nom-valeur dans laquelle le nom est associé à la valeur.</span><span class="sxs-lookup"><span data-stu-id="a489a-106">Scripting object that is used to create a name-value pair in which the name is associated with the value.</span></span>

## <a name="members"></a><span data-ttu-id="a489a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a489a-107">Members</span></span>

<span data-ttu-id="a489a-108">L’objet **TaskNamedValuePair** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a489a-108">The **TaskNamedValuePair** object has these types of members:</span></span>

-   [<span data-ttu-id="a489a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a489a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a489a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a489a-110">Properties</span></span>

<span data-ttu-id="a489a-111">L’objet **TaskNamedValuePair** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a489a-111">The **TaskNamedValuePair** object has these properties.</span></span>



| <span data-ttu-id="a489a-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="a489a-112">Property</span></span>                                             | <span data-ttu-id="a489a-113">Description</span><span class="sxs-lookup"><span data-stu-id="a489a-113">Description</span></span>                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="a489a-114">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a489a-114">**Name**</span></span>](tasknamedvaluepair-name.md)<br/>   | <span data-ttu-id="a489a-115">Obtient ou définit le nom associé à une valeur dans une paire nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="a489a-115">Gets or sets the name that is associated with a value in a name-value pair.</span></span><br/> |
| [<span data-ttu-id="a489a-116">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a489a-116">**Value**</span></span>](tasknamedvaluepair-value.md)<br/> | <span data-ttu-id="a489a-117">Obtient ou définit la valeur associée à un nom dans une paire nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="a489a-117">Gets or sets the value that is associated with a name in a name-value pair.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a489a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a489a-118">Remarks</span></span>

<span data-ttu-id="a489a-119">Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, une paire nom-valeur est spécifiée à l’aide de l’élément [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="a489a-119">When reading or writing your own XML for a task, a name-value pair is specified using the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a489a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a489a-120">Requirements</span></span>



| <span data-ttu-id="a489a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a489a-121">Requirement</span></span> | <span data-ttu-id="a489a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a489a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a489a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a489a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a489a-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a489a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a489a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a489a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a489a-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a489a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a489a-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a489a-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a489a-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a489a-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a489a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a489a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a489a-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a489a-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a489a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a489a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a489a-132">**TaskNamedValueCollection**</span><span class="sxs-lookup"><span data-stu-id="a489a-132">**TaskNamedValueCollection**</span></span>](tasknamedvaluecollection.md)
</dt> </dl>

 

 





