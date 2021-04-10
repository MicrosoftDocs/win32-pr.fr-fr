---
description: Crée un nouveau nœud de reconnaissance personnalisé pour IInkAnalyzer.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'IInkAnalyzer :: CreateCustomRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201503"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a><span data-ttu-id="05dab-103">IInkAnalyzer :: CreateCustomRecognizer, méthode</span><span class="sxs-lookup"><span data-stu-id="05dab-103">IInkAnalyzer::CreateCustomRecognizer method</span></span>

<span data-ttu-id="05dab-104">Crée un nouveau nœud de reconnaissance personnalisé pour [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="05dab-104">Creates a new custom recognizer node for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="05dab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05dab-105">Syntax</span></span>


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="05dab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05dab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05dab-107">*pInkAnalysisRecognizerId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05dab-107">*pInkAnalysisRecognizerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05dab-108">Identificateur global unique (GUID) du [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pour lequel créer un nœud.</span><span class="sxs-lookup"><span data-stu-id="05dab-108">The globally unique identifier (GUID) of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) for which to create a node.</span></span>

</dd> <dt>

<span data-ttu-id="05dab-109">*ppContextNode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05dab-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05dab-110">Pointeur vers l’objet [**IContextNode**](icontextnode.md) qui représente le nouveau nœud de reconnaissance personnalisé.</span><span class="sxs-lookup"><span data-stu-id="05dab-110">A pointer to the [**IContextNode**](icontextnode.md) object representing the new custom recognizer node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05dab-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05dab-111">Return value</span></span>

<span data-ttu-id="05dab-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="05dab-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05dab-113">Notes</span><span class="sxs-lookup"><span data-stu-id="05dab-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="05dab-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur ppContextNode lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="05dab-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on ppContextNode when you no longer need to use the object.</span></span>

 

<span data-ttu-id="05dab-115">Cette méthode crée un nouveau [**IContextNode**](icontextnode.md) avec un type de CustomRecognizer (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="05dab-115">This method creates a new [**IContextNode**](icontextnode.md) with a type of CustomRecognizer (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="05dab-116">Il ajoute ensuite le nouveau nœud de reconnaissance personnalisé à la collection de sous-nœuds du nœud racine de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez la méthode [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) et [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="05dab-116">It then adds the new custom recognizer node to the subnodes collection of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="05dab-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05dab-117">Requirements</span></span>



| <span data-ttu-id="05dab-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05dab-118">Requirement</span></span> | <span data-ttu-id="05dab-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="05dab-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05dab-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05dab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="05dab-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05dab-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="05dab-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05dab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="05dab-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="05dab-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="05dab-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="05dab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="05dab-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="05dab-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="05dab-126">DLL</span><span class="sxs-lookup"><span data-stu-id="05dab-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05dab-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05dab-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="05dab-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05dab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05dab-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="05dab-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="05dab-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="05dab-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="05dab-131">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="05dab-131">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="05dab-132">**IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode**</span><span class="sxs-lookup"><span data-stu-id="05dab-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="05dab-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="05dab-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

