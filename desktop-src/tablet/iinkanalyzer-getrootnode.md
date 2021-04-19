---
description: Obtient le IContextNode racine de l’arborescence de contexte de l’objet IInkAnalyzer.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'IInkAnalyzer :: GetRootNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 280c1907558372d247f25a0f760990d7c3c53a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544678"
---
# <a name="iinkanalyzergetrootnode-method"></a><span data-ttu-id="fcbc2-103">IInkAnalyzer :: GetRootNode, méthode</span><span class="sxs-lookup"><span data-stu-id="fcbc2-103">IInkAnalyzer::GetRootNode method</span></span>

<span data-ttu-id="fcbc2-104">Obtient le [**IContextNode**](icontextnode.md) racine de l’arborescence de contexte de l’objet [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="fcbc2-104">Gets the root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbc2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcbc2-105">Syntax</span></span>


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a><span data-ttu-id="fcbc2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcbc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbc2-107">*ppRootNode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fcbc2-107">*ppRootNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbc2-108">[**IContextNode**](icontextnode.md) racine de l’arborescence de contexte de l’objet [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="fcbc2-108">The root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbc2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcbc2-109">Return value</span></span>

<span data-ttu-id="fcbc2-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fcbc2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fcbc2-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fcbc2-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppRootNode* lorsque vous n’avez plus besoin d’utiliser le nœud racine.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppRootNode* when you no longer need to use the root node.</span></span>

 

<span data-ttu-id="fcbc2-113">Le [**IInkAnalyzer**](iinkanalyzer.md) gère une arborescence d’objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="fcbc2-113">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a tree of [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="fcbc2-114">Ces objets contiennent à la fois l’entrée pour l’analyse et les résultats de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-114">These objects contain both input for analysis and the results of analysis.</span></span> <span data-ttu-id="fcbc2-115">Lorsque des traits sont ajoutés initialement à **IInkAnalyzer**, **IInkAnalyzer** les assigne à un **IContextNode** de type UnclassifiedInk (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et types de [nœuds de contexte](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="fcbc2-115">When strokes are initially added to the **IInkAnalyzer**, the **IInkAnalyzer** assigns them to a **IContextNode** of type UnclassifiedInk (See [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="fcbc2-116">Une fois les traits analysés, le **IInkAnalyzer** les affecte aux objets **IContextNode** appropriés dans l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-116">After the strokes are analyzed, the **IInkAnalyzer** assigns them to appropriate **IContextNode** objects in the tree.</span></span> <span data-ttu-id="fcbc2-117">Pour plus d’informations sur l’utilisation de **IInkAnalyzer** pour analyser l’encre, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-117">For more information about using the **IInkAnalyzer** to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fcbc2-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="fcbc2-118">Examples</span></span>

<span data-ttu-id="fcbc2-119">L’exemple suivant montre une méthode qui parcourt l’arborescence des résultats [**IContextNode**](icontextnode.md) de l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-119">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="fcbc2-120">Si le IInkAnlyzer n’effectue pas actuellement une analyse de l’encre, la méthode effectue les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-120">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="fcbc2-121">Obtient la chaîne de reconnaissance supérieure.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-121">Gets the top recognition string.</span></span>
-   <span data-ttu-id="fcbc2-122">Obtient le nœud racine de l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-122">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="fcbc2-123">Appelle une méthode d’assistance, `ExploreContextNode` , pour examiner le nœud racine et ses nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="fcbc2-123">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="fcbc2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcbc2-124">Requirements</span></span>



| <span data-ttu-id="fcbc2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcbc2-125">Requirement</span></span> | <span data-ttu-id="fcbc2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcbc2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbc2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcbc2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fcbc2-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fcbc2-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fcbc2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcbc2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fcbc2-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fcbc2-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fcbc2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcbc2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcbc2-132"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fcbc2-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fcbc2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fcbc2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcbc2-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcbc2-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fcbc2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcbc2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbc2-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fcbc2-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fcbc2-137">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="fcbc2-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fcbc2-138">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="fcbc2-138">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="fcbc2-139">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="fcbc2-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

