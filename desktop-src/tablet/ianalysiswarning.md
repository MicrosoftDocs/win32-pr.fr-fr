---
description: Représente un avertissement ou une erreur qui se produit pendant une opération d’analyse d’encre.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interface IAnalysisWarning (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113399"
---
# <a name="ianalysiswarning-interface"></a>Interface IAnalysisWarning

Représente un avertissement ou une erreur qui se produit pendant une opération d’analyse d’encre.

## <a name="members"></a>Membres

L’interface **IAnalysisWarning** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisWarning** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAnalysisWarning** possède ces méthodes.



| Méthode                                                            | Description                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBackgroundError**](ianalysiswarning-getbackgrounderror.md) | Récupère le code d’erreur de l’opération d’analyse de l’encre en arrière-plan si une erreur s’est produite.<br/>                                    |
| [**GetHint**](ianalysiswarning-gethint.md)                       | Récupère l’indicateur d’analyse à l’origine de cet avertissement<br/>                                                                        |
| [**GetNodeIds**](ianalysiswarning-getnodeids.md)                 | Récupère les identificateurs de tous les nœuds de contexte appropriés associés à cet avertissement.<br/>                              |
| [**GetWarningCode**](ianalysiswarning-getwarningcode.md)         | Récupère le type d’avertissement qui s’est produit à l’aide de l’énumération [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .<br/> |



 

## <a name="remarks"></a>Notes

Les types d’avertissements qui peuvent se produire sont décrits par l’énumération [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) . Souvent, les avertissements se produisent lorsque vous essayez d’utiliser une fonctionnalité qui n’est pas prise en charge par le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) utilisé par le [**IInkAnalyzer**](iinkanalyzer.md) .

Certains avertissements indiquent que le [**IInkAnalyzer**](iinkanalyzer.md) n’a pas terminé l’opération d’analyse. Pour plus d’informations, consultez [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).

## <a name="examples"></a>Exemples

L’exemple suivant montre un plan d’un gestionnaire d’événements pour l’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) . Le gestionnaire vérifie [**IAnalysisStatus :: IsSuccessful**](ianalysisstatus-issuccessful.md). Si l’opération d’analyse génère des avertissements, le gestionnaire itère au sein de la collection d’objets **IAnalysisWarning** .


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisWarnings**](ianalysiswarnings.md)
</dt> <dt>

[**AnalysisWarningCode**](analysiswarningcode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

