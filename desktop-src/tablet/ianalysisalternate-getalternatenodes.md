---
description: Obtient les objets IContextNode associés à cet autre.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'IAnalysisAlternate :: GetAlternateNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514838"
---
# <a name="ianalysisalternategetalternatenodes-method"></a><span data-ttu-id="590ac-103">IAnalysisAlternate :: GetAlternateNodes, méthode</span><span class="sxs-lookup"><span data-stu-id="590ac-103">IAnalysisAlternate::GetAlternateNodes method</span></span>

<span data-ttu-id="590ac-104">Obtient les objets [**IContextNode**](icontextnode.md) associés à cet autre.</span><span class="sxs-lookup"><span data-stu-id="590ac-104">Gets the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="590ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="590ac-105">Syntax</span></span>


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a><span data-ttu-id="590ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="590ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="590ac-107">*ppAlternateNodes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="590ac-107">*ppAlternateNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="590ac-108">Pointeur vers la collection [**IContextNodes**](icontextnodes.md) qui contient les objets [**IContextNode**](icontextnode.md) associés à cet autre.</span><span class="sxs-lookup"><span data-stu-id="590ac-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection that contains [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="590ac-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="590ac-109">Return value</span></span>

<span data-ttu-id="590ac-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="590ac-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="590ac-111">Notes</span><span class="sxs-lookup"><span data-stu-id="590ac-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="590ac-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppAlternateNodes* lorsque vous n’avez plus besoin d’utiliser la collection de nœuds de contexte.</span><span class="sxs-lookup"><span data-stu-id="590ac-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternateNodes* when you no longer need to use the context node collection.</span></span>

 

<span data-ttu-id="590ac-113">Cette méthode retourne les nœuds de contexte feuille associés à cet autre.</span><span class="sxs-lookup"><span data-stu-id="590ac-113">This method returns the leaf context nodes that are associated with this alternate.</span></span> <span data-ttu-id="590ac-114">Les nœuds terminaux sont, par exemple, InkWord, TextWord, image, InkDrawing et InkBullet.</span><span class="sxs-lookup"><span data-stu-id="590ac-114">Examples of leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet context nodes.</span></span> <span data-ttu-id="590ac-115">Pour plus d’informations, consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et [types de nœuds de contexte](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="590ac-115">For more information, see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="590ac-116">Étant donné qu’ils correspondent à des substitutions, ces objets [**IContextNode**](icontextnode.md) ne sont pas des descendants de la racine **IContextNode** de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md)), sauf s’il s’agit de l’alternative supérieure, qui est le premier élément d’une collection [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="590ac-116">Because they correspond to alternates, these [**IContextNode**](icontextnode.md) objects are not descendants of the [**IInkAnalyzer**](iinkanalyzer.md) object's root **IContextNode** (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)) unless they are the top alternate, which is the first element in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="590ac-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="590ac-117">Requirements</span></span>



| <span data-ttu-id="590ac-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="590ac-118">Requirement</span></span> | <span data-ttu-id="590ac-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="590ac-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="590ac-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="590ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="590ac-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="590ac-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="590ac-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="590ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="590ac-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="590ac-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="590ac-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="590ac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="590ac-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="590ac-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="590ac-126">DLL</span><span class="sxs-lookup"><span data-stu-id="590ac-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="590ac-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="590ac-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="590ac-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="590ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="590ac-129">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="590ac-129">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="590ac-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="590ac-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="590ac-131">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="590ac-131">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="590ac-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="590ac-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> <dt>

[<span data-ttu-id="590ac-133">System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. AlternateNodes</span><span class="sxs-lookup"><span data-stu-id="590ac-133">System.Windows.Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes</span></span>](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

