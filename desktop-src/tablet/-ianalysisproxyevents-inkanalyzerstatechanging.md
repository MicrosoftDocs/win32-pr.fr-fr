---
description: Se produit avant que le IInkAnalyzer ne rapproche les résultats de l’analyse afin qu’une application puisse synchroniser les données avec le IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: '_IAnalysisProxyEvents :: InkAnalyzerStateChanging, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d4e32685e25e4c942b3c723df2152b1064bed59599fda54fcac00e22aab04206
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884079"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_Événement IAnalysisProxyEvents :: InkAnalyzerStateChanging

Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) ne rapproche les résultats de l’analyse afin qu’une application puisse synchroniser les données avec le **IInkAnalyzer**.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalyzer* \[ dans\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) qui va rapprocher ses résultats d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Lorsque le **IInkAnalyzer** déclenche cet événement, votre application doit remplir les sous-nœuds du nœud racine de l’analyseur d’encre (consultez la méthode [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md) et [**IInkAnalyzer :: GetRootNode**](iinkanalyzer-getrootnode.md)).

Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement après qu’il a déclenché l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) . Il déclenche cet événement uniquement lors de l’analyse en arrière-plan.

Verrouillez votre structure de données lorsque [**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement **\_ IAnalysisProxyEvents :: InkAnalyzerStateChanging** . Les modifications apportées à la structure de vos données au cours de cette phase d’analyse peuvent entraîner des erreurs dans l’analyse et la synchronisation de l’encre. Déverrouillez votre structure de données lorsque **IInkAnalyzer** déclenche l’événement [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .

Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




