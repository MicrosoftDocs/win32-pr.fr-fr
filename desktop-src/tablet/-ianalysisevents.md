---
description: Spécifie les événements associés aux étapes d’analyse d’un objet IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Interface _IAnalysisEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2f49455e3e6fb68b2884cda380c304d7655b70d49ff338bcfb7c36904b449019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452164"
---
# <a name="_ianalysisevents-interface"></a>\_Interface IAnalysisEvents

Spécifie les événements associés aux étapes d’analyse d’un objet [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Événements](/windows)

### <a name="events"></a>Événements

L’interface **\_ IAnalysisEvents** contient ces événements.



| Événement                                                               | Description                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Activité**](-ianalysisevents-activity.md)                       | Se produit lors des appels à la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou à la méthode [**IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Se produit lorsque l’étape d’analyse intermédiaire actuelle est terminée.<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | Se produit lorsque le [**IInkAnalyzer**](iinkanalyzer.md) est prêt à rapprocher les résultats de l’analyse en arrière-plan avec son état actuel.<br/>                                                  |
| [**Résultats**](-ianalysisevents-results.md)                         | Se produit lorsque l’étape d’analyse finale est terminée.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) accède aux données de trait.<br/>                                                                                                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

