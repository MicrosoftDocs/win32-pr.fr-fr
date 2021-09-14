---
description: Se produit lorsque l’étape d’analyse finale est terminée.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: '_IAnalysisEvents :: Results, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226689"
---
# <a name="_ianalysiseventsresults-event"></a>\_IAnalysisEvents :: Results, événement

Se produit lorsque l’étape d’analyse finale est terminée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalyzer* \[ dans\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) qui produit les résultats de l’analyse.

</dd> <dt>

*pAnalysisStatus* \[ dans\]
</dt> <dd>

Objet [**IAnalysisStatus**](ianalysisstatus.md) qui représente l’état de l’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement après qu’il a concilié les résultats de l’étape d’analyse finale.

Si votre application appelle la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), cet événement signale que les résultats de l’analyse sont prêts.

Si votre application gère sa propre structure de données, qui est synchronisée avec celle de [**IInkAnalyzer**](iinkanalyzer.md), cet événement indique que le **IInkAnalyzer** a terminé d’apporter des modifications à ses données internes pour cette étape d’analyse.

Verrouillez votre structure de données lorsque [**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement [**\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Les modifications apportées à la structure de vos données au cours de cette phase d’analyse peuvent entraîner des erreurs dans l’analyse et la synchronisation de l’encre. Déverrouillez votre structure de données lorsque **IInkAnalyzer** déclenche l’événement [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou **\_ IAnalysisEvents :: Results** .

Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




