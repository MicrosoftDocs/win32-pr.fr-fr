---
description: 'Se produit lorsque la méthode IInkAnalyzer :: Analyze ou IInkAnalyzer :: BackgroundAnalyze est appelée.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: '_IAnalysisEvents :: Activity, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc0a0fd1ad5434116dc7333899329384eae4b9c6dbf7c386e1e2e048f8431d21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047358"
---
# <a name="_ianalysiseventsactivity-event"></a>\_Événement IAnalysisEvents :: Activity

Se produit lorsque la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) est appelée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Activity();
```



## <a name="parameters"></a>Paramètres

Cet événement n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Cet événement indique que le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse de l’encre. Cet événement n’indique pas la progression de l’opération d’analyse de l’encre.

Pour effectuer l’une des opérations suivantes, implémentez un gestionnaire d’événements **\_ IAnalysisEvents :: Activity** :

-   Indiquer à l’utilisateur que l’analyseur d’encre effectue une analyse de l’encre.
-   Traiter l’entrée d’utilisateur pendant l’analyse synchrone.
-   Recevoir des notifications de requêtes système, telles que le redessin de la fenêtre de l’application, pendant l’analyse de l’encre.

Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement fréquemment pendant la phase d’analyse de la disposition et la phase de classification de l’écriture et du dessin de l’analyse de l’encre. Le **IInkAnalyzer** déclenche cet événement lors de la phase de reconnaissance de l’écriture manuscrite avant et après l’accès à un module de reconnaissance d’encre.

Le nombre d’événements d’activité générés par un [**IInkAnalyzer**](iinkanalyzer.md) est affecté par :

-   Module de reconnaissance de l’encre que le [**IInkAnalyzer**](iinkanalyzer.md) applique à la reconnaissance de l’encre.
-   Nombre et longueur des traits analysés par le [**IInkAnalyzer**](iinkanalyzer.md) .
-   Nombre de traits classés comme écrits.

Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Conditions requises



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

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




