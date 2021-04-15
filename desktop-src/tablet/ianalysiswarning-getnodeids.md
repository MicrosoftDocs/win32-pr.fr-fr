---
description: Retourne les identificateurs de tous les nœuds de contexte appropriés associés à cet avertissement.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'IAnalysisWarning :: GetNodeIds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526541"
---
# <a name="ianalysiswarninggetnodeids-method"></a><span data-ttu-id="05428-103">IAnalysisWarning :: GetNodeIds, méthode</span><span class="sxs-lookup"><span data-stu-id="05428-103">IAnalysisWarning::GetNodeIds method</span></span>

<span data-ttu-id="05428-104">Retourne les identificateurs de tous les nœuds de contexte appropriés associés à cet avertissement.</span><span class="sxs-lookup"><span data-stu-id="05428-104">Returns the identifiers of any relevant context nodes that are associated with this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="05428-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05428-105">Syntax</span></span>


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a><span data-ttu-id="05428-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05428-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05428-107">*pulCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="05428-107">*pulCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="05428-108">Nombre d’identificateurs globaux uniques (GUID) dans *ppNodeIds*.</span><span class="sxs-lookup"><span data-stu-id="05428-108">The number of globally unique identifiers (GUIDs) in *ppNodeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="05428-109">*ppNodeIds* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05428-109">*ppNodeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05428-110">Pointeur vers un tableau de GUID qui identifie les nœuds de contexte associés à cet avertissement d’analyse, ou **null** si aucun nœud de contexte n’est associé à l’avertissement.</span><span class="sxs-lookup"><span data-stu-id="05428-110">A pointer to an array of GUIDs that identifies the context nodes that are associated with this analysis warning, or **NULL** if no context nodes are associated with the warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05428-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05428-111">Return value</span></span>

<span data-ttu-id="05428-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="05428-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05428-113">Notes</span><span class="sxs-lookup"><span data-stu-id="05428-113">Remarks</span></span>

<span data-ttu-id="05428-114">Si *ppNodeIds* est passé comme **null**, la méthode **GetNodeIds** retourne **S \_ OK** et le nombre de rectangles est retourné dans *pulCount*.</span><span class="sxs-lookup"><span data-stu-id="05428-114">If *ppNodeIds* is passed as **NULL**, the **GetNodeIds** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="05428-115">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppNodeIds* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="05428-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppNodeIds* when you no longer need the information.</span></span>

 

## <a name="examples"></a><span data-ttu-id="05428-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="05428-116">Examples</span></span>

<span data-ttu-id="05428-117">L’exemple suivant montre comment récupérer les objets [**IContextNode**](icontextnode.md) qui se trouvent dans le [**IAnalysisWarning**](ianalysiswarning.md), `warning` et comment récupérer uniquement le nombre d’objets **IContextNode**</span><span class="sxs-lookup"><span data-stu-id="05428-117">The following example shows how to get the [**IContextNode**](icontextnode.md) objects that are in the [**IAnalysisWarning**](ianalysiswarning.md), `warning`, and how to get only the number of **IContextNode** objects</span></span>


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="05428-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05428-118">Requirements</span></span>



| <span data-ttu-id="05428-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05428-119">Requirement</span></span> | <span data-ttu-id="05428-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="05428-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05428-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05428-121">Minimum supported client</span></span><br/> | <span data-ttu-id="05428-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05428-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="05428-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05428-123">Minimum supported server</span></span><br/> | <span data-ttu-id="05428-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="05428-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="05428-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="05428-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="05428-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="05428-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="05428-127">DLL</span><span class="sxs-lookup"><span data-stu-id="05428-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05428-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05428-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="05428-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05428-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05428-130">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="05428-130">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="05428-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="05428-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="05428-132">**IInkAnalyzer :: FindNode, méthode**</span><span class="sxs-lookup"><span data-stu-id="05428-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="05428-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="05428-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

