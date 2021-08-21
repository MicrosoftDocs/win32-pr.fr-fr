---
description: Effectue une analyse de l’encre synchrone.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'IInkAnalyzer :: Analyze, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 34548eed6611b8b0e867edc7ef23e1a7c7e20a796738e2750718ec91b1e5a5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044219"
---
# <a name="iinkanalyzeranalyze-method"></a>IInkAnalyzer :: Analyze, méthode

Effectue une analyse de l’encre synchrone.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppStatus* \[ à\]
</dt> <dd>

Pointeur vers un [**IAnalysisStatus**](ianalysisstatus.md) qui décrit l’état de l’opération d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppStatus* lorsque vous n’avez plus besoin d’utiliser l’état d’analyse.

 

Cette méthode démarre une opération d’analyse d’encre synchrone. L’analyse de l’encre comprend l’analyse de la disposition, l’écriture et la classification des dessins et la reconnaissance de l’écriture. Cette méthode est retournée une fois l’opération d’analyse terminée.

Cette méthode retourne **le \_ pointeur E** si *PpStatus* a la **valeur null**.

Pendant un appel à la méthode **IInkAnalyzer :: Analyze** ou à la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), le [**IInkAnalyzer**](iinkanalyzer.md) analyse l’encre au sein de sa région modifiée (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)). Toutefois, le **IInkAnalyzer** peut développer l’opération d’analyse pour inclure les régions voisines.

Cette méthode définit la région de modification de l’objet [**IInkAnalyzer**](iinkanalyzer.md) sur une zone vide. Si un autre thread a ajouté des données de trait qui n’ont pas été analysées, le **IInkAnalyzer** ajoute le cadre englobant des traits non analysés à sa région modifiée pendant la phase de rapprochement de l’analyse.

Cette méthode retourne une erreur si votre application ne gère pas l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .

[**IInkAnalyzer**](iinkanalyzer.md) ne déclenche pas les événements [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) et [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) en réponse à cette méthode.

Pour modifier la façon dont l’analyse de l’encre est effectuée, utilisez la [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).

Pour plus d’informations sur l’analyse des encres, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre.

## <a name="examples"></a>Exemples

L’exemple suivant effectue une analyse de l’encre de premier plan.


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a>Conditions requises



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

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer :: GetDirtyRegion, méthode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer :: SetDirtyRegion, méthode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer :: GetRootNode, méthode**](iinkanalyzer-getrootnode.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

