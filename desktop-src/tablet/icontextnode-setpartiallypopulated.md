---
description: Modifie la valeur qui indique si ce IContextNode est partiellement ou entièrement rempli.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'IContextNode :: SetPartiallyPopulated, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034016"
---
# <a name="icontextnodesetpartiallypopulated-method"></a><span data-ttu-id="3121a-103">IContextNode :: SetPartiallyPopulated, méthode</span><span class="sxs-lookup"><span data-stu-id="3121a-103">IContextNode::SetPartiallyPopulated method</span></span>

<span data-ttu-id="3121a-104">Modifie la valeur qui indique si ce [**IContextNode**](icontextnode.md) est partiellement ou entièrement rempli.</span><span class="sxs-lookup"><span data-stu-id="3121a-104">Modifies the value that indicates whether this [**IContextNode**](icontextnode.md) is partially or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3121a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3121a-105">Syntax</span></span>


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="3121a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3121a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3121a-107">*fPartiallyPopulated* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3121a-107">*fPartiallyPopulated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3121a-108">**Variante \_ TRUE** si ce [**IContextNode**](icontextnode.md) est partiellement rempli ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="3121a-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) is partially populated; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3121a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3121a-109">Return value</span></span>

<span data-ttu-id="3121a-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3121a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3121a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3121a-111">Remarks</span></span>

<span data-ttu-id="3121a-112">Utilisez cette méthode lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3121a-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="3121a-113">Pour plus d’informations, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3121a-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="3121a-114">Lors de la virtualisation de votre arborescence de documents, veillez à définir la valeur PropertyGuidsForContextNodes. RotatedBoundingBox (à l’aide de ContextNode. AddPropertyValue) sur tous les objets ContextNode.</span><span class="sxs-lookup"><span data-stu-id="3121a-114">When virtualizing your document tree, be sure to set the PropertyGuidsForContextNodes.RotatedBoundingBox value (using ContextNode.AddPropertyValue) on all ContextNode objects.</span></span> <span data-ttu-id="3121a-115">La propriété RotatedBoundingBox est calculée par le InkAnalyzer et doit être définie par défaut sur tous les ContextNodes d’écriture.</span><span class="sxs-lookup"><span data-stu-id="3121a-115">The RotatedBoundingBox property is calculated by the InkAnalyzer and by default should be on all writing ContextNodes.</span></span> <span data-ttu-id="3121a-116">Toutefois, si votre application virtualise les résultats de l’analyse en définissant la propriété PartiallyPopulated, lors de la gestion de l’événement PopulateContextNode, veillez à remplir la propriété RotatedBoundingBox.</span><span class="sxs-lookup"><span data-stu-id="3121a-116">However, if your application virtualizes the analysis results by setting the PartiallyPopulated property, when handling the PopulateContextNode event be sure to populate the RotatedBoundingBox property.</span></span> <span data-ttu-id="3121a-117">Si vous ne définissez pas la propriété RotatedBoundingBox, vous risquez d’utiliser des données de document potentiellement plus utilisées dans l’opération d’analyse en cours</span><span class="sxs-lookup"><span data-stu-id="3121a-117">Failure to set the RotatedBoundingBox property will result in potentially more document data being used in the current analysis operation</span></span>

## <a name="requirements"></a><span data-ttu-id="3121a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3121a-118">Requirements</span></span>



| <span data-ttu-id="3121a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3121a-119">Requirement</span></span> | <span data-ttu-id="3121a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3121a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3121a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3121a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3121a-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3121a-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3121a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3121a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3121a-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3121a-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3121a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3121a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3121a-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3121a-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3121a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3121a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3121a-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3121a-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3121a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3121a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3121a-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3121a-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3121a-131">**\_IAnalysisProxyEvents ::P opulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="3121a-131">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="3121a-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="3121a-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="3121a-133">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="3121a-133">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="3121a-134">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3121a-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




