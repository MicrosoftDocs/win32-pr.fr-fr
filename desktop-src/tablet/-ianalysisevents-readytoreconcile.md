---
description: Se produit lorsque le IInkAnalyzer est prêt à rapprocher les résultats de l’analyse en arrière-plan avec son état actuel.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: '_IAnalysisEvents :: ReadyToReconcile, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211297"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_Événement IAnalysisEvents :: ReadyToReconcile

Se produit lorsque le [**IInkAnalyzer**](iinkanalyzer.md) est prêt à rapprocher les résultats de l’analyse en arrière-plan avec son état actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Le [**IInkAnalyzer**](iinkanalyzer.md) effectue un rapprochement automatique lorsque l’indicateur **\_ AutomaticReconciliation AnalysisModes** de l’analyseur d’encre est défini (consultez [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)). Lorsque l’indicateur **AnalysisModes \_ AutomaticReconciliation** n’est pas défini, votre application doit rapprocher manuellement les résultats de l’analyse en arrière-plan.

Pour effectuer un rapprochement manuel, procédez comme suit.

1.  Effacez l’indicateur **AnalysisModes \_ AutomaticReconciliation** de l’analyseur d’encre.
2.  Gérez l’événement **\_ IAnalysisEvents :: ReadyToReconcile** .
3.  Pour rapprocher les résultats de l’analyse, appelez la méthode [**IInkAnalyzer :: rapprochee**](iinkanalyzer-reconcile.md) de la méthode à partir du gestionnaire d’événements pour l’événement **\_ IAnalysisEvents :: ReadyToReconcile** . Pour annuler l’opération d’analyse en arrière-plan actuelle, appelez la méthode de [**méthode IInkAnalyzer :: Abort**](iinkanalyzer-abort.md) à partir du gestionnaire d’événements pour l’événement **\_ IAnalysisEvents :: ReadyToReconcile** .

Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement avant de déclencher l’événement [**\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .

Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement lors de l’analyse en arrière-plan.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer :: Reconcile, méthode**](iinkanalyzer-reconcile.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




