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
ms.openlocfilehash: 3defa68f68e0c2e81bdb093005db1e173442b9686ca4c98a4966c755b2fb52dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092247"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a>IInkAnalyzer :: GetRecognizedString, méthode

Récupère la chaîne de résultat optimale de l’opération de reconnaissance pour l’ensemble de l’arborescence de nœuds de contexte dans [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbstrRecognizedString* \[ à\]
</dt> <dd>

Chaîne de résultat optimale de l’opération de reconnaissance pour l’ensemble de l’arborescence de nœuds de contexte dans [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour *pbstrRecognizedString* lorsque vous n’avez plus besoin d’utiliser la chaîne.

 

Cette méthode retourne la même valeur que les données de propriété du nœud racine pour la chaîne reconnue. (Consultez [**IInkAnalyzer :: GetRootNode, méthode**](iinkanalyzer-getrootnode.md), [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md), et [Propriétés du nœud de contexte](context-node-properties.md).)

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

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

