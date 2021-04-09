---
description: Récupère d’autres analyses pour les nœuds d’une collection IContextNodes spécifiée.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'IInkAnalyzer :: GetAlternatesForContextNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113343"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a><span data-ttu-id="c2585-103">IInkAnalyzer :: GetAlternatesForContextNodes, méthode</span><span class="sxs-lookup"><span data-stu-id="c2585-103">IInkAnalyzer::GetAlternatesForContextNodes method</span></span>

<span data-ttu-id="c2585-104">Récupère d’autres analyses pour les nœuds d’une collection [**IContextNodes**](icontextnodes.md) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c2585-104">Retrieves analysis alternates for the nodes in a specified [**IContextNodes**](icontextnodes.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2585-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2585-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="c2585-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2585-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2585-107">*pContextNodes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2585-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2585-108">Collection [**IContextNodes**](icontextnodes.md) pour laquelle les alternatives d’analyse sont retournées.</span><span class="sxs-lookup"><span data-stu-id="c2585-108">The [**IContextNodes**](icontextnodes.md) collection for which the analysis alternatives are returned.</span></span>

</dd> <dt>

<span data-ttu-id="c2585-109">*ulMaximumAlternates* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2585-109">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2585-110">Nombre maximal d’alternatives à retourner.</span><span class="sxs-lookup"><span data-stu-id="c2585-110">The maximum number of alternatives to return.</span></span>

</dd> <dt>

<span data-ttu-id="c2585-111">*ppAlternates* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c2585-111">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2585-112">Objet [**IAnalysisAlternates**](ianalysisalternates.md) contenant les alternatives d’analyse.</span><span class="sxs-lookup"><span data-stu-id="c2585-112">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2585-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2585-113">Return value</span></span>

<span data-ttu-id="c2585-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="c2585-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2585-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c2585-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c2585-116">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAlternates* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="c2585-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="c2585-117">Le [**IAnalysisAlternate**](ianalysisalternate.md) supérieur est retourné en tant que premier remplacement de la collection.</span><span class="sxs-lookup"><span data-stu-id="c2585-117">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="c2585-118">Les objets [**IContextNode**](icontextnode.md) dans *pContextNodes* n’ont pas besoin de représenter des zones adjacentes du document.</span><span class="sxs-lookup"><span data-stu-id="c2585-118">The [**IContextNode**](icontextnode.md) objects in *pContextNodes* do not have to represent adjacent areas of the document.</span></span>

<span data-ttu-id="c2585-119">Pour chaque indicateur d’analyse dans les nœuds, le [**IInkAnalyzer**](iinkanalyzer.md) retourne uniquement l’alternative supérieure.</span><span class="sxs-lookup"><span data-stu-id="c2585-119">For each analysis hint in nodes, the [**IInkAnalyzer**](iinkanalyzer.md) returns only the top alternate.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2585-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2585-120">Requirements</span></span>



| <span data-ttu-id="c2585-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2585-121">Requirement</span></span> | <span data-ttu-id="c2585-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2585-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2585-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2585-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c2585-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2585-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c2585-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2585-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c2585-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2585-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c2585-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2585-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2585-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c2585-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c2585-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c2585-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2585-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2585-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c2585-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2585-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2585-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c2585-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c2585-133">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="c2585-133">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="c2585-134">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="c2585-134">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="c2585-135">**IInkAnalyzer :: GetAlternates, méthode**</span><span class="sxs-lookup"><span data-stu-id="c2585-135">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="c2585-136">**IInkAnalyzer :: GetAlternatesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="c2585-136">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="c2585-137">**IInkAnalyzer :: ModifyTopAlternate, méthode**</span><span class="sxs-lookup"><span data-stu-id="c2585-137">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="c2585-138">**IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode**</span><span class="sxs-lookup"><span data-stu-id="c2585-138">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="c2585-139">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="c2585-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

