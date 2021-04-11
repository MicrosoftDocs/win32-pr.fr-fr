---
description: Récupère tous les objets IContextNode Hint d’analyse attachés au IInkAnalyzer et portant le nom spécifié.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'IInkAnalyzer :: GetAnalysisHintsByName, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201500"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a><span data-ttu-id="99f32-103">IInkAnalyzer :: GetAnalysisHintsByName, méthode</span><span class="sxs-lookup"><span data-stu-id="99f32-103">IInkAnalyzer::GetAnalysisHintsByName method</span></span>

<span data-ttu-id="99f32-104">Récupère tous les objets [**IContextNode**](icontextnode.md) Hint d’analyse attachés au [**IInkAnalyzer**](iinkanalyzer.md) et portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="99f32-104">Retrieves all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md) and that have the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99f32-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="99f32-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99f32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99f32-107">*hintName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99f32-107">*hintName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99f32-108">Nom de l’indicateur à rechercher.</span><span class="sxs-lookup"><span data-stu-id="99f32-108">The hint name for which to search.</span></span>

</dd> <dt>

<span data-ttu-id="99f32-109">*ppAnalysisHints* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="99f32-109">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99f32-110">L’indicateur d’analyse [**IContextNode**](icontextnode.md) les objets du [**IInkAnalyzer**](iinkanalyzer.md) qui portent le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="99f32-110">The analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) that have the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99f32-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99f32-111">Return value</span></span>

<span data-ttu-id="99f32-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md) de l’encre valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="99f32-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="99f32-113">Notes</span><span class="sxs-lookup"><span data-stu-id="99f32-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="99f32-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAnalysisHints* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="99f32-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="99f32-115">Cette méthode retourne une collection vide si aucun nœud d’indicateur d’analyse n’est attaché à [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="99f32-115">This method returns an empty collection if no such analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="99f32-116">Un nœud d’indicateur d’analyse est un [**IContextNode**](icontextnode.md) avec un type de nœud de contexte AnalysisHint (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et [types de nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="99f32-116">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="99f32-117">Pour ajouter des informations de contexte à l’indicateur, utilisez [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md) avec le paramètre *pPropertyDataId* défini sur l’un des identificateurs globaux uniques (Guid) dans les constantes des propriétés de l' [indicateur d’analyse](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="99f32-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="99f32-118">Pour rechercher les valeurs de propriété qui sont définies sur un nœud de contexte, utilisez [**IContextNode :: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="99f32-118">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="99f32-119">Pour rechercher la valeur d’une propriété, utilisez [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="99f32-119">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99f32-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99f32-120">Requirements</span></span>



| <span data-ttu-id="99f32-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99f32-121">Requirement</span></span> | <span data-ttu-id="99f32-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="99f32-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99f32-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99f32-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99f32-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99f32-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="99f32-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99f32-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99f32-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="99f32-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="99f32-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="99f32-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99f32-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="99f32-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="99f32-129">DLL</span><span class="sxs-lookup"><span data-stu-id="99f32-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99f32-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99f32-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="99f32-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99f32-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f32-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="99f32-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="99f32-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="99f32-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="99f32-134">**IInkAnalyzer :: CreateAnalysisHint, méthode**</span><span class="sxs-lookup"><span data-stu-id="99f32-134">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="99f32-135">**IInkAnalyzer ::D méthode eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="99f32-135">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="99f32-136">**IInkAnalyzer :: GetAnalysisHints, méthode**</span><span class="sxs-lookup"><span data-stu-id="99f32-136">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="99f32-137">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="99f32-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

