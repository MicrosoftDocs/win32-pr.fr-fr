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
ms.openlocfilehash: 5ff2181eacd3df1d2815448a0c2d7cafce4d521fa0abbc7b26492d9c078982dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713419"
---
# <a name="iinkanalyzergetrootnode-method"></a>IInkAnalyzer :: GetRootNode, méthode

Obtient le [**IContextNode**](icontextnode.md) racine de l’arborescence de contexte de l’objet [**IInkAnalyzer**](iinkanalyzer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppRootNode* \[ à\]
</dt> <dd>

[**IContextNode**](icontextnode.md) racine de l’arborescence de contexte de l’objet [**IInkAnalyzer**](iinkanalyzer.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppRootNode* lorsque vous n’avez plus besoin d’utiliser le nœud racine.

 

Le [**IInkAnalyzer**](iinkanalyzer.md) gère une arborescence d’objets [**IContextNode**](icontextnode.md) . Ces objets contiennent à la fois l’entrée pour l’analyse et les résultats de l’analyse. Lorsque des traits sont ajoutés initialement à **IInkAnalyzer**, **IInkAnalyzer** les assigne à un **IContextNode** de type UnclassifiedInk (consultez [**IContextNode :: GetType**](icontextnode-gettype.md) et types de [nœuds de contexte](context-node-types.md)). Une fois les traits analysés, le **IInkAnalyzer** les affecte aux objets **IContextNode** appropriés dans l’arborescence. Pour plus d’informations sur l’utilisation de **IInkAnalyzer** pour analyser l’encre, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.

## <a name="examples"></a>Exemples

L’exemple suivant montre une méthode qui parcourt l’arborescence des résultats [**IContextNode**](icontextnode.md) de l’analyseur d’encre. Si le IInkAnlyzer n’effectue pas actuellement une analyse de l’encre, la méthode effectue les opérations suivantes.

-   Obtient la chaîne de reconnaissance supérieure.
-   Obtient le nœud racine de l’analyseur d’encre.
-   Appelle une méthode d’assistance, `ExploreContextNode` , pour examiner le nœud racine et ses nœuds enfants.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

