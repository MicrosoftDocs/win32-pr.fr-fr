---
description: Se produit avant que le IInkAnalyzer effectue une analyse dans la région d’un objet IContextNode partiellement rempli.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents ::P événement opulateContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294070"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a>\_IAnalysisProxyEvents ::P événement opulateContextNode

Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse dans la région d’un objet [**IContextNode**](icontextnode.md) partiellement rempli.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalyzer* \[ dans\]
</dt> <dd>

Objet [**IInkAnalyzer**](iinkanalyzer.md) sur lequel exécuter l’analyse.

</dd> <dt>

*pContextNodeToPopulate* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) partiellement rempli.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Lorsque le **IInkAnalyzer** déclenche cet événement, votre application doit remplir le *pContextNodeToPopulate*. Pendant la phase d’analyse, le **IInkAnalyzer** déclenche cet événement pour obtenir des informations sur les zones dans lesquelles il analyse l’encre.

Si le document contient des liens pour le *pContextNodeToPopulate*, votre application doit créer et ajouter ces liens. Ce processus requiert que les nœuds source et de destination, y compris leurs ancêtres, soient entièrement remplis avant que le gestionnaire d’événements de cet événement ne se termine (consultez [**IContextLink :: GetSourceNode**](icontextlink-getsourcenode.md) et [**IContextLink :: GetDestinationNode**](icontextlink-getdestinationnode.md)).

Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

Pendant l’analyse en arrière-plan, le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement après avoir déclenché l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .

## <a name="requirements"></a>Spécifications



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

 

 




