---
description: Remplace le en-tête supérieur actuel par le autre spécifié et efface le type de confirmation pour tous les objets IContextNode associés à l’autre.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'IInkAnalyzer :: ModifyTopAlternate, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515041"
---
# <a name="iinkanalyzermodifytopalternate-method"></a><span data-ttu-id="64a2d-103">IInkAnalyzer :: ModifyTopAlternate, méthode</span><span class="sxs-lookup"><span data-stu-id="64a2d-103">IInkAnalyzer::ModifyTopAlternate method</span></span>

<span data-ttu-id="64a2d-104">Remplace le en-tête supérieur actuel par le autre spécifié et efface le type de confirmation pour tous les objets [**IContextNode**](icontextnode.md) associés à l’autre.</span><span class="sxs-lookup"><span data-stu-id="64a2d-104">Changes the current top alternate to the specified alternate and clears the confirmation type for all [**IContextNode**](icontextnode.md) objects associated with the alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64a2d-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="64a2d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64a2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64a2d-107">*pAlternate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64a2d-107">*pAlternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64a2d-108">Objet [**IAnalysisAlternate**](ianalysisalternate.md) contenant la nouvelle alternative supérieure.</span><span class="sxs-lookup"><span data-stu-id="64a2d-108">The [**IAnalysisAlternate**](ianalysisalternate.md) object containing the new top alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64a2d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64a2d-109">Return value</span></span>

<span data-ttu-id="64a2d-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="64a2d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64a2d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="64a2d-111">Remarks</span></span>

<span data-ttu-id="64a2d-112">Pour récupérer des analyses alternatives, utilisez la méthode [**IInkAnalyzer :: GetAlternates**](iinkanalyzer-getalternates.md), [**IInkAnalyzer :: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)ou la [**méthode IInkAnalyzer :: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="64a2d-112">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="64a2d-113">Pour récupérer les objets [**IContextNode**](icontextnode.md) associés à une analyse alternative, utilisez la [**méthode IAnalysisAlternate :: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="64a2d-113">To get the [**IContextNode**](icontextnode.md) objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="64a2d-114">Pour modifier le type de confirmation d’un nœud de contexte, utilisez [**IContextNode :: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="64a2d-114">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64a2d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64a2d-115">Requirements</span></span>



| <span data-ttu-id="64a2d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64a2d-116">Requirement</span></span> | <span data-ttu-id="64a2d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="64a2d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64a2d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64a2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="64a2d-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64a2d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="64a2d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64a2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="64a2d-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="64a2d-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="64a2d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="64a2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="64a2d-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="64a2d-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="64a2d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="64a2d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64a2d-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64a2d-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="64a2d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64a2d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64a2d-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="64a2d-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="64a2d-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="64a2d-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="64a2d-129">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="64a2d-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="64a2d-130">**ConfirmationType**</span><span class="sxs-lookup"><span data-stu-id="64a2d-130">**ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="64a2d-131">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="64a2d-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




