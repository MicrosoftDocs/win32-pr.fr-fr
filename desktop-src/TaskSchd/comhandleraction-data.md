---
title: ComHandlerAction. Data, propriété
description: Pour les scripts, obtient ou définit les données supplémentaires associées au gestionnaire.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Planificateur de tâches de propriétés de données
- Planificateur de tâches de propriétés de données, objet ComHandlerAction
- Objet ComHandlerAction Planificateur de tâches, propriété de données
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385131"
---
# <a name="comhandleractiondata-property"></a><span data-ttu-id="0f6d8-106">ComHandlerAction. Data, propriété</span><span class="sxs-lookup"><span data-stu-id="0f6d8-106">ComHandlerAction.Data property</span></span>

<span data-ttu-id="0f6d8-107">Pour les scripts, obtient ou définit les données supplémentaires associées au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="0f6d8-107">For scripting, gets or sets additional data that is associated with the handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f6d8-108">Syntax</span></span>


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a><span data-ttu-id="0f6d8-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0f6d8-109">Property value</span></span>

<span data-ttu-id="0f6d8-110">Arguments requis par le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="0f6d8-110">The arguments that are needed by the handler.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6d8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0f6d8-111">Remarks</span></span>

<span data-ttu-id="0f6d8-112">Lors de la lecture ou de l’écriture de code XML, les données d’un gestionnaire COM sont spécifiées dans l’élément [**Data**](taskschedulerschema-data-comhandlertype-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="0f6d8-112">When reading or writing XML, the data of a COM handler is specified in the [**Data**](taskschedulerschema-data-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6d8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f6d8-113">Requirements</span></span>



| <span data-ttu-id="0f6d8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f6d8-114">Requirement</span></span> | <span data-ttu-id="0f6d8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f6d8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6d8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6d8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6d8-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f6d8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0f6d8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f6d8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6d8-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f6d8-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0f6d8-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0f6d8-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f6d8-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0f6d8-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0f6d8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0f6d8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f6d8-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f6d8-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f6d8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f6d8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6d8-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0f6d8-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0f6d8-126">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="0f6d8-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





