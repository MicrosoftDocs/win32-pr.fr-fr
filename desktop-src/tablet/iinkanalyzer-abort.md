---
description: Annule l’opération d’analyse en cours.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'IInkAnalyzer :: Abort, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f52b2037210e39533d1247cb338bb22a7785f354dbca6b615c6ada67eff3bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773599"
---
# <a name="iinkanalyzerabort-method"></a>IInkAnalyzer :: Abort, méthode

Annule l’opération d’analyse en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppAbortedRegion* \[ à\]
</dt> <dd>

Pointeur vers un [**IAnalysisRegion**](ianalysisregion.md) qui représente la région modifiée (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) de l’opération d’analyse actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAbortedRegion* lorsque vous n’avez plus besoin d’utiliser l’objet.

Cette méthode annule l’opération d’analyse en cours.

Quand *ppAbortedRegion* a la valeur **null**, cette méthode effectue l’abandon comme normal, car cela indique que l’appelant n’a aucun intérêt dans la valeur de retour.

La **méthode IInkAnalyzer :: Abort** interrompt les événements [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) et [**\_ IAnalysisEvents :: Activity**](-ianalysisevents-activity.md) pour l’opération d’analyse en cours.

La **méthode IInkAnalyzer :: Abort** s’exécute de façon asynchrone jusqu’à ce que l’opération d’analyse en arrière-plan actuelle soit annulée. Étant donné que le processus d’annulation est asynchrone, l’application peut effectuer d’autres tâches pendant que l’analyse vers actuelle est annulée.

Si aucune opération d’analyse n’est en cours, cette méthode retourne une région d’analyse vide.

Si une opération d’analyse est en cours, cette méthode annule l’opération.

Si les opérations d’analyse synchrones et asynchrones sont en cours, cette méthode annule l’opération synchrone.

Si cette méthode est appelée plusieurs fois pour la même opération d’analyse, le premier appel retourne la région modifiée pour l’opération, et les appels suivants retournent une région vide.

Si votre application gère sa propre structure de données qui est synchronisée avec celle de [**IInkAnalyzer**](iinkanalyzer.md), l’appel de la **méthode IInkAnalyzer :: Abort** peut conserver votre document avec des résultats partiels. Pour éviter cela, n’appelez pas la **méthode IInkAnalyzer :: Abort** entre le moment où le **IInkAnalyzer** reçoit l’événement [**\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) et l’heure à laquelle le **IInkAnalyzer** reçoit l’événement [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .

Pour plus d’informations sur la synchronisation de vos données d’application avec l’analyseur d’encre, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer :: GetDirtyRegion, méthode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer :: SetDirtyRegion, méthode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

