---
description: Récupère une valeur indiquant si le IInkAnalyzer effectue une analyse de l’encre.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'IInkAnalyzer :: IsAnalyzing, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526488"
---
# <a name="iinkanalyzerisanalyzing-method"></a><span data-ttu-id="75d9e-103">IInkAnalyzer :: IsAnalyzing, méthode</span><span class="sxs-lookup"><span data-stu-id="75d9e-103">IInkAnalyzer::IsAnalyzing method</span></span>

<span data-ttu-id="75d9e-104">Récupère une valeur indiquant si le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="75d9e-104">Retrieves a value indicating whether the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d9e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75d9e-105">Syntax</span></span>


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a><span data-ttu-id="75d9e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75d9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d9e-107">*pbAnalyzing* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="75d9e-107">*pbAnalyzing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75d9e-108">**Variante \_ TRUE** si le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse de l’encre ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="75d9e-108">**VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d9e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75d9e-109">Return value</span></span>

<span data-ttu-id="75d9e-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="75d9e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75d9e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="75d9e-111">Remarks</span></span>

<span data-ttu-id="75d9e-112">Cette propriété a **la \_ valeur true** si [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="75d9e-112">This property is **VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing synchronous or asynchronous analysis.</span></span>

## <a name="examples"></a><span data-ttu-id="75d9e-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="75d9e-113">Examples</span></span>

<span data-ttu-id="75d9e-114">L’exemple suivant montre une méthode qui parcourt l’arborescence des résultats [**IContextNode**](icontextnode.md) de l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="75d9e-114">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="75d9e-115">Si ce n’est pas le cas, la méthode effectue les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="75d9e-115">If the ink analyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="75d9e-116">Obtient la chaîne de reconnaissance supérieure.</span><span class="sxs-lookup"><span data-stu-id="75d9e-116">Gets the top recognition string.</span></span>
-   <span data-ttu-id="75d9e-117">Obtient le nœud racine de l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="75d9e-117">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="75d9e-118">Appelle une méthode d’assistance, `ExploreContextNode` , pour examiner le nœud racine et ses nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="75d9e-118">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="75d9e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75d9e-119">Requirements</span></span>



| <span data-ttu-id="75d9e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75d9e-120">Requirement</span></span> | <span data-ttu-id="75d9e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="75d9e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d9e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d9e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="75d9e-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75d9e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75d9e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d9e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="75d9e-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d9e-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="75d9e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="75d9e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d9e-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75d9e-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75d9e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="75d9e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d9e-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d9e-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="75d9e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75d9e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d9e-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="75d9e-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="75d9e-132">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="75d9e-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="75d9e-133">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="75d9e-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="75d9e-134">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="75d9e-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




