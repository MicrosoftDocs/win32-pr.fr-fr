---
description: 'Applique les résultats d’une opération d’analyse d’encre en arrière-plan à l’arborescence du nœud de contexte pour les parties de l’arborescence qui n’ont pas été modifiées par l’application depuis l’appel à la méthode IInkAnalyzer :: BackgroundAnalyze.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'IInkAnalyzer :: Reconcile, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514444"
---
# <a name="iinkanalyzerreconcile-method"></a>IInkAnalyzer :: Reconcile, méthode

Applique les résultats d’une opération d’analyse d’encre en arrière-plan à l’arborescence du nœud de contexte pour les parties de l’arborescence qui n’ont pas été modifiées par l’application depuis l’appel à la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Par défaut, le [**IInkAnalyzer**](iinkanalyzer.md) exécute une phase de réconciliation automatique immédiatement avant de déclencher les événements [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) et [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .

Pour désactiver le rapprochement automatique, désactivez l’indicateur **AnalysisModes \_ AutomaticReconciliation** des modes d’analyse de l’analyseur d’encre (voir [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) et [**AnalysisModes**](analysismodes.md)). La méthode [**IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) retourne une erreur lorsque le rapprochement automatique est désactivé et que votre application ne gère pas l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) . Votre application doit appeler la méthode **IInkAnalyzer :: réconcilie** pour que le [**IInkAnalyzer**](iinkanalyzer.md) puisse continuer à traiter les résultats ou continuer l’analyse pour l’étape d’analyse correspondante.

Votre application peut apporter des modifications, telles que l’ajout ou la suppression de traits et la modification des données de trait, dans l’arborescence du nœud de contexte de l’objet [**IInkAnalyzer**](iinkanalyzer.md) lors de l’analyse en arrière-plan. Ces modifications peuvent invalider certaines parties des résultats de l’analyse en arrière-plan. Cette méthode applique uniquement les résultats d’analyse à l’arborescence du nœud de contexte de l’analyseur pour les parties de l’arborescence que votre application n’a pas modifiées. Cette méthode ajoute également des régions contenant des résultats d’analyse non valides à la région de modification de l’objet **IInkAnalyzer** (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Pour plus d’informations sur l’utilisation du pour analyser l’encre, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre. [**AnalysisModes**](analysismodes.md)

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

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




