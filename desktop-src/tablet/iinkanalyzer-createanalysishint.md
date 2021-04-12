---
description: Ajoute un nouveau nœud d’indicateur d’analyse avec une zone infinie à la IInkAnalyzer.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'IInkAnalyzer :: CreateAnalysisHint, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318458"
---
# <a name="iinkanalyzercreateanalysishint-method"></a><span data-ttu-id="a1211-103">IInkAnalyzer :: CreateAnalysisHint, méthode</span><span class="sxs-lookup"><span data-stu-id="a1211-103">IInkAnalyzer::CreateAnalysisHint method</span></span>

<span data-ttu-id="a1211-104">Ajoute un nouveau nœud d’indicateur d’analyse avec une zone infinie à la [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a1211-104">Adds a new analysis hint node with an infinite area to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1211-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1211-105">Syntax</span></span>


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="a1211-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1211-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1211-107">*ppAnalysisHint* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a1211-107">*ppAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1211-108">Nouveau nœud d’indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a1211-108">The new analysis hint node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1211-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1211-109">Return value</span></span>

<span data-ttu-id="a1211-110">Consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md) de l’encre pour obtenir une description des valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="a1211-110">See [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) for a description of the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1211-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a1211-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a1211-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAnalysisHint* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="a1211-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHint* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a1211-113">Pour fournir des informations de contexte supplémentaires pour [**IInkAnalyzer**](iinkanalyzer.md), vous pouvez ajouter des indicateurs d’analyse à l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="a1211-113">To provide extra context information for the [**IInkAnalyzer**](iinkanalyzer.md), you can add analysis hints to the ink analyzer.</span></span> <span data-ttu-id="a1211-114">Les indicateurs d’analyse peuvent améliorer la précision de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a1211-114">Analysis hints can improve recognition accuracy.</span></span> <span data-ttu-id="a1211-115">Par exemple, vous pouvez ajouter des Factoid et des informations de guide pour les champs dans une application de formulaire.</span><span class="sxs-lookup"><span data-stu-id="a1211-115">For example, you can add factoid and guide information for fields in a form application.</span></span>

<span data-ttu-id="a1211-116">Cette méthode crée un nouveau [**IContextNode**](icontextnode.md) avec un type de nœud de contexte AnalysisHint (voir [**IContextNode :: GetType**](icontextnode-gettype.md)) et ajoute le nouvel indicateur en tant que sous-nœud du nœud racine de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) et [**IInkAnalyzer :: GetRootNode méthode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="a1211-116">This method creates a new [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)) and adds the new hint as a subnode of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="a1211-117">Pour ajouter des informations de contexte à l’indicateur, utilisez [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md) avec le paramètre *pPropertyDataId* défini sur l’une des constantes de propriétés de l' [indicateur d’analyse](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="a1211-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="a1211-118">Si une indication est assignée à une zone infinie, appelée indication globale, le [**IInkAnalyzer**](iinkanalyzer.md) applique le contexte de l’indicateur à toute l’encre qui ne se trouve pas dans la zone d’un autre indicateur.</span><span class="sxs-lookup"><span data-stu-id="a1211-118">If a hint is assigned an infinite area, termed a global hint, the [**IInkAnalyzer**](iinkanalyzer.md) applies the hint's context to all ink that is not within another hint's area.</span></span> <span data-ttu-id="a1211-119">Plusieurs indicateurs peuvent être attachés à un seul **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="a1211-119">Multiple hints may be attached to a single **IInkAnalyzer**.</span></span> <span data-ttu-id="a1211-120">Toutefois, un seul indicateur global peut être attaché à un analyseur d’encre unique, et aucun indicateur non global ne peut se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="a1211-120">However, only one global hint can be attached to a single ink analyzer, and no non-global hints can overlap.</span></span> <span data-ttu-id="a1211-121">Pour plus d’informations sur les types d’informations de contexte qu’un indicateur peut fournir, consultez Propriétés de l' [indicateur d’analyse](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a1211-121">For more information about the types of context information that a hint can provide, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="a1211-122">L’ajout d’un indicateur d’analyse ne marque pas la zone de l’indicateur pour la réanalyse.</span><span class="sxs-lookup"><span data-stu-id="a1211-122">Adding an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="a1211-123">Pour marquer la zone dans l’indicateur pour la réanalyse, utilisez la [**méthode IInkAnalyzer :: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) pour définir la région de modification sur l’Union de la région et de la zone de modification actuelles de l’indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a1211-123">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="a1211-124">Lorsque vous utilisez des indicateurs pour une application de formulaire, l’application doit éviter de mélanger le contexte de texte avec de l’encre dans les formulaires.</span><span class="sxs-lookup"><span data-stu-id="a1211-124">When using hints for a form application, the application should avoid mixing text context with ink in the forms.</span></span> <span data-ttu-id="a1211-125">Cela signifie, par exemple, que les noms de champs de texte ne doivent pas être créés dans l’arborescence d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a1211-125">This means for example that text field names should not be created in the analysis tree.</span></span> <span data-ttu-id="a1211-126">Les indicateurs sont destinés à associer l’encre à des zones sur des pages ; tout contexte de texte interfère avec cette association d’entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="a1211-126">Hints are meant to associate the ink to areas on pages; any text context interferes with this ink-to-hint association.</span></span> <span data-ttu-id="a1211-127">L’opération d’analyse peut fusionner l’encre et le contexte de texte dans la même région d’écriture, ce qui empêche l’encre d’être associée à la zone d’indication.</span><span class="sxs-lookup"><span data-stu-id="a1211-127">The analysis operation may merge the ink and the text context in the same writing region which would prevent the ink from being associated with the hint area.</span></span>

<span data-ttu-id="a1211-128">Pour plus d’informations sur l’analyse des encres, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a1211-128">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1211-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1211-129">Requirements</span></span>



| <span data-ttu-id="a1211-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1211-130">Requirement</span></span> | <span data-ttu-id="a1211-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1211-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1211-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1211-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a1211-133">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1211-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a1211-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1211-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a1211-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1211-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a1211-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1211-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1211-137"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1211-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1211-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a1211-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1211-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1211-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a1211-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1211-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1211-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a1211-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a1211-142">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a1211-142">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="a1211-143">**IInkAnalyzer ::D méthode eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="a1211-143">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="a1211-144">**IInkAnalyzer :: GetAnalysisHints, méthode**</span><span class="sxs-lookup"><span data-stu-id="a1211-144">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="a1211-145">**IInkAnalyzer :: GetAnalysisHintsByName, méthode**</span><span class="sxs-lookup"><span data-stu-id="a1211-145">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="a1211-146">Propriétés de l’indicateur d’analyse</span><span class="sxs-lookup"><span data-stu-id="a1211-146">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="a1211-147">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="a1211-147">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

