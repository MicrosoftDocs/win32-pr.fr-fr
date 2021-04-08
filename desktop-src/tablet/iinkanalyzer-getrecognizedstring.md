---
description: Récupère la chaîne de résultat optimale de l’opération de reconnaissance pour l’ensemble de l’arborescence de nœuds de contexte dans IInkAnalyzer.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'IInkAnalyzer :: GetRecognizedString, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751805"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a><span data-ttu-id="65ea5-103">IInkAnalyzer :: GetRecognizedString, méthode</span><span class="sxs-lookup"><span data-stu-id="65ea5-103">IInkAnalyzer::GetRecognizedString method</span></span>

<span data-ttu-id="65ea5-104">Récupère la chaîne de résultat optimale de l’opération de reconnaissance pour l’ensemble de l’arborescence de nœuds de contexte dans [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="65ea5-104">Retrieves the best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="65ea5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65ea5-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="65ea5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65ea5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ea5-107">*pbstrRecognizedString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65ea5-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65ea5-108">Chaîne de résultat optimale de l’opération de reconnaissance pour l’ensemble de l’arborescence de nœuds de contexte dans [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="65ea5-108">The best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ea5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65ea5-109">Return value</span></span>

<span data-ttu-id="65ea5-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="65ea5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="65ea5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="65ea5-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="65ea5-112">Pour éviter une fuite de mémoire, appelez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour *pbstrRecognizedString* lorsque vous n’avez plus besoin d’utiliser la chaîne.</span><span class="sxs-lookup"><span data-stu-id="65ea5-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) for *pbstrRecognizedString* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="65ea5-113">Cette méthode retourne la même valeur que les données de propriété du nœud racine pour la chaîne reconnue.</span><span class="sxs-lookup"><span data-stu-id="65ea5-113">This method returns the same value as the root node's property data for the recognized string.</span></span> <span data-ttu-id="65ea5-114">(Consultez [**IInkAnalyzer :: GetRootNode, méthode**](iinkanalyzer-getrootnode.md), [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md), et [Propriétés du nœud de contexte](context-node-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="65ea5-114">(See [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md), [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md), and [Context Node Properties](context-node-properties.md).)</span></span>

## <a name="examples"></a><span data-ttu-id="65ea5-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="65ea5-115">Examples</span></span>

<span data-ttu-id="65ea5-116">L’exemple suivant montre une méthode qui parcourt l’arborescence des résultats [**IContextNode**](icontextnode.md) de l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="65ea5-116">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="65ea5-117">Si le IInkAnlyzer n’effectue pas actuellement une analyse de l’encre, la méthode effectue les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="65ea5-117">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="65ea5-118">Obtient la chaîne de reconnaissance supérieure.</span><span class="sxs-lookup"><span data-stu-id="65ea5-118">Gets the top recognition string.</span></span>
-   <span data-ttu-id="65ea5-119">Obtient le nœud racine de l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="65ea5-119">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="65ea5-120">Appelle une méthode d’assistance, `ExploreContextNode` , pour examiner le nœud racine et ses nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="65ea5-120">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="65ea5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65ea5-121">Requirements</span></span>



| <span data-ttu-id="65ea5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65ea5-122">Requirement</span></span> | <span data-ttu-id="65ea5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="65ea5-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ea5-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ea5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="65ea5-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65ea5-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="65ea5-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ea5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="65ea5-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="65ea5-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="65ea5-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="65ea5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ea5-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="65ea5-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="65ea5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="65ea5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65ea5-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65ea5-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="65ea5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65ea5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ea5-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="65ea5-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="65ea5-134">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="65ea5-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

