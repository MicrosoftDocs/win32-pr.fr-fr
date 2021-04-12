---
description: Effectue une analyse d’encre asynchrone.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'IInkAnalyzer :: BackgroundAnalyze, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526505"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a>IInkAnalyzer :: BackgroundAnalyze, méthode

Effectue une analyse d’encre asynchrone.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Lorsque cette méthode est appelée, le [**IInkAnalyzer**](iinkanalyzer.md) effectue l’analyse de l’encre sur un thread d’arrière-plan.

Cette méthode retourne **S \_ false** et ne démarre pas une nouvelle opération d’analyse en arrière-plan dans les circonstances suivantes.

-   [**IInkAnalyzer**](iinkanalyzer.md) effectue actuellement une analyse en arrière-plan.
-   la région modifiée (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) représente une zone vide.

Le [**IInkAnalyzer**](iinkanalyzer.md) analyse l’encre au sein de sa région modifiée pendant un appel à la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou à la **méthode IInkAnalyzer :: BackgroundAnalyze**. Toutefois, le **IInkAnalyzer** peut développer l’opération d’analyse pour inclure les régions voisines.

Cette méthode définit la région de modification sur une zone vide.

Si les données de trait ont été ajoutées au [**IInkAnalyzer**](iinkanalyzer.md) après l’appel de la **méthode IInkAnalyzer :: BackgroundAnalyze**, le **IInkAnalyzer** peut mettre à jour la région modifiée pendant la phase de rapprochement de l’analyse de l’encre.

Le paramètre des modes d’analyse (consultez la [**méthode IInkAnalyzer :: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)) spécifie la manière dont le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse en arrière-plan. Pour plus d’informations sur l’analyse des encres, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.

Cette méthode retourne un code d’erreur dans les circonstances suivantes.

-   Votre application a défini la valeur [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ IntermediateResults** dans le [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) et ne gère pas l’événement [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) .
-   Votre application a effacé la valeur [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ AutomaticReconciliation** dans le [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) et ne gère pas l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .
-   Votre application ne gère pas l’événement [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .
-   Votre application ne gère pas l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .

## <a name="examples"></a>Exemples

L’exemple suivant vérifie la région de modification de l’analyseur d’encre, puis lance l’analyse de l’encre en arrière-plan si la région modifiée n’est pas vide.


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
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

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: GetAnalysisModes, méthode**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer :: SetAnalysisModes, méthode**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer :: GetDirtyRegion, méthode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer :: SetDirtyRegion, méthode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer :: GetRootNode, méthode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




