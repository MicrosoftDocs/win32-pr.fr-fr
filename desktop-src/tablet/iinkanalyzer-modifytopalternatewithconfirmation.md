---
description: Remplace le IAnalysisAlternate actuel par le haut de la valeur spécifiée.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318453"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a><span data-ttu-id="e376e-103">IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode</span><span class="sxs-lookup"><span data-stu-id="e376e-103">IInkAnalyzer::ModifyTopAlternateWithConfirmation method</span></span>

<span data-ttu-id="e376e-104">Remplace le [**IAnalysisAlternate**](ianalysisalternate.md)actuel par le haut de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e376e-104">Changes the current top alternate to the specified [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e376e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e376e-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a><span data-ttu-id="e376e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e376e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e376e-107">*autre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e376e-107">*alternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e376e-108">L’analyse alternative à définir en tant que nouvelle alternative supérieure.</span><span class="sxs-lookup"><span data-stu-id="e376e-108">The analysis alternate to set as the new top alternate.</span></span>

</dd> <dt>

<span data-ttu-id="e376e-109">*fconfirmAutomatically* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e376e-109">*fconfirmAutomatically* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e376e-110">**Variante \_ TRUE** pour définir tous les nœuds de contexte de feuille manuscrite qui correspondent à l’analyse alternative à un type de confirmation **ConfirmationType \_ NodeTypeAndProperties** (consultez [**IContextNode :: IsConfirmed**](icontextnode-isconfirmed.md) et [**ConfirmationType**](confirmationtype.md)); **Variante \_ FALSe** pour définir tous les nœuds de contexte de feuille manuscrite qui correspondent à l’analyse alternative à un type de confirmation **ConfirmationType \_ None**.</span><span class="sxs-lookup"><span data-stu-id="e376e-110">**VARIANT\_TRUE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_NodeTypeAndProperties** (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md) and [**ConfirmationType**](confirmationtype.md)); **VARIANT\_FALSE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_None**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e376e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e376e-111">Return value</span></span>

<span data-ttu-id="e376e-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="e376e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e376e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e376e-113">Remarks</span></span>

<span data-ttu-id="e376e-114">Pour récupérer des analyses alternatives, utilisez la méthode [**IInkAnalyzer :: GetAlternates**](iinkanalyzer-getalternates.md), [**IInkAnalyzer :: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)ou la [**méthode IInkAnalyzer :: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="e376e-114">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="e376e-115">Pour récupérer les objets de nœud de contexte associés à une analyse alternative, utilisez la [**méthode IAnalysisAlternate :: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="e376e-115">To get the context node objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="e376e-116">Pour modifier le type de confirmation d’un nœud de contexte, utilisez [**IContextNode :: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="e376e-116">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e376e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e376e-117">Requirements</span></span>



| <span data-ttu-id="e376e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e376e-118">Requirement</span></span> | <span data-ttu-id="e376e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e376e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e376e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e376e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e376e-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e376e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e376e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e376e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e376e-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e376e-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e376e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e376e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e376e-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e376e-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e376e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e376e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e376e-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e376e-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e376e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e376e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e376e-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e376e-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e376e-130">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="e376e-130">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="e376e-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e376e-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e376e-132">**ConfirmationType de l’analyse de l’encre**</span><span class="sxs-lookup"><span data-stu-id="e376e-132">**Ink Analysis ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="e376e-133">Référence</span><span class="sxs-lookup"><span data-stu-id="e376e-133">Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




