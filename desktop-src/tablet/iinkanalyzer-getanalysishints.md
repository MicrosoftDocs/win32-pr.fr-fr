---
description: Obtient tous les objets IContextNode Hint d’analyse attachés à IInkAnalyzer.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'IInkAnalyzer :: GetAnalysisHints, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113339"
---
# <a name="iinkanalyzergetanalysishints-method"></a><span data-ttu-id="0a45e-103">IInkAnalyzer :: GetAnalysisHints, méthode</span><span class="sxs-lookup"><span data-stu-id="0a45e-103">IInkAnalyzer::GetAnalysisHints method</span></span>

<span data-ttu-id="0a45e-104">Obtient tous les objets [**IContextNode**](icontextnode.md) Hint d’analyse attachés à [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="0a45e-104">Gets all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a45e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a45e-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="0a45e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a45e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a45e-107">*ppAnalysisHints* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0a45e-107">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a45e-108">Pointeur vers tous les objets Hint d’analyse [**IContextNode**](icontextnode.md) dans le [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="0a45e-108">A pointer to all the analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a45e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a45e-109">Return value</span></span>

<span data-ttu-id="0a45e-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="0a45e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a45e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0a45e-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="0a45e-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAnalysisHints* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="0a45e-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="0a45e-113">Cette méthode retourne une collection vide si aucun nœud d’indicateur d’analyse n’est attaché à [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="0a45e-113">This method returns an empty collection if no analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="0a45e-114">Un nœud d’indicateur d’analyse est un [**IContextNode**](icontextnode.md) avec un type de nœud de contexte AnalysisHint (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et [types de nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="0a45e-114">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="0a45e-115">Pour ajouter des informations de contexte à l’indicateur, utilisez [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md) avec le paramètre *pPropertyDataId* défini sur l’un des identificateurs globaux uniques (Guid) dans les constantes des propriétés de l' [indicateur d’analyse](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="0a45e-115">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="0a45e-116">Pour rechercher les valeurs de propriété qui sont définies sur un nœud de contexte, utilisez [**IContextNode :: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="0a45e-116">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="0a45e-117">Pour rechercher la valeur d’une propriété, utilisez [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="0a45e-117">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a45e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a45e-118">Requirements</span></span>



| <span data-ttu-id="0a45e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a45e-119">Requirement</span></span> | <span data-ttu-id="0a45e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a45e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a45e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a45e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0a45e-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a45e-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0a45e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a45e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0a45e-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a45e-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0a45e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a45e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a45e-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0a45e-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0a45e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0a45e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a45e-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a45e-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0a45e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a45e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a45e-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="0a45e-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0a45e-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="0a45e-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="0a45e-132">**IInkAnalyzer :: CreateAnalysisHint, méthode**</span><span class="sxs-lookup"><span data-stu-id="0a45e-132">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="0a45e-133">**IInkAnalyzer ::D méthode eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="0a45e-133">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="0a45e-134">**IInkAnalyzer :: GetAnalysisHintsByName, méthode**</span><span class="sxs-lookup"><span data-stu-id="0a45e-134">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="0a45e-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="0a45e-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

