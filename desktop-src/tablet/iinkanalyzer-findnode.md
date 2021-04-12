---
description: Récupère l’objet IContextNode pour un identificateur global unique (GUID) spécifié.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'IInkAnalyzer :: FindNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034013"
---
# <a name="iinkanalyzerfindnode-method"></a><span data-ttu-id="9014f-103">IInkAnalyzer :: FindNode, méthode</span><span class="sxs-lookup"><span data-stu-id="9014f-103">IInkAnalyzer::FindNode method</span></span>

<span data-ttu-id="9014f-104">Récupère l’objet [**IContextNode**](icontextnode.md) pour un identificateur global unique (Guid) spécifié.</span><span class="sxs-lookup"><span data-stu-id="9014f-104">Retrieves the [**IContextNode**](icontextnode.md) object for a specified globally unique identifier (GUID).</span></span>

## <a name="syntax"></a><span data-ttu-id="9014f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9014f-105">Syntax</span></span>


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a><span data-ttu-id="9014f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9014f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9014f-107">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9014f-107">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9014f-108">Identificateur de l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="9014f-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9014f-109">*ppContextNodeFound* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9014f-109">*ppContextNodeFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9014f-110">Pointeur vers l’objet [**IContextNode**](icontextnode.md) avec l’identificateur *PID* .</span><span class="sxs-lookup"><span data-stu-id="9014f-110">A pointer to the [**IContextNode**](icontextnode.md) object with the *pId* identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9014f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9014f-111">Return value</span></span>

<span data-ttu-id="9014f-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="9014f-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9014f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9014f-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9014f-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodeFound* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="9014f-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="9014f-115">Si aucun objet [**IContextNode**](icontextnode.md) de ce type n’existe en tant que descendant du nœud racine [**IInkAnalyzer**](iinkanalyzer.md) , la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="9014f-115">If no such [**IContextNode**](icontextnode.md) object exists as a descendant of the [**IInkAnalyzer**](iinkanalyzer.md) root node, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="9014f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9014f-116">Requirements</span></span>



| <span data-ttu-id="9014f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9014f-117">Requirement</span></span> | <span data-ttu-id="9014f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9014f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9014f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9014f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9014f-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9014f-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9014f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9014f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9014f-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9014f-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9014f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9014f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9014f-124"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9014f-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9014f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9014f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9014f-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9014f-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9014f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9014f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9014f-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9014f-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9014f-129">**IInkAnalyzer :: FindInkLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="9014f-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="9014f-130">**IInkAnalyzer :: FindInkLeafNodesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="9014f-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="9014f-131">**IInkAnalyzer :: FindLeafNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="9014f-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="9014f-132">**IInkAnalyzer :: FindNodesOfType, méthode**</span><span class="sxs-lookup"><span data-stu-id="9014f-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="9014f-133">**IInkAnalyzer :: FindNodesOfTypeForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="9014f-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="9014f-134">**IInkAnalyzer :: FindNodesOfTypeInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="9014f-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="9014f-135">**IInkAnalyzer :: FindNodesWithCallBack, méthode**</span><span class="sxs-lookup"><span data-stu-id="9014f-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="9014f-136">**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**</span><span class="sxs-lookup"><span data-stu-id="9014f-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="9014f-137">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="9014f-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

