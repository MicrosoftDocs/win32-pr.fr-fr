---
description: Se produit avant que le IInkAnalyzer supprime un objet IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: '_IAnalysisProxyEvents :: ContextNodeDeleting, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106543009"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_Événement IAnalysisProxyEvents :: ContextNodeDeleting

Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) supprime un objet [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalyzer* \[ dans\]
</dt> <dd>

Objet [**IInkAnalyzer**](iinkanalyzer.md) qui supprime l’objet [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pContextNodeToBeDeleted* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui supprime un [**IContextNode**](icontextnode.md).

Avant que [**IInkAnalyzer**](iinkanalyzer.md) ne supprime un [**IContextNode**](icontextnode.md), le **IInkAnalyzer** supprime tous les traits du nœud de contexte et supprime tous les liens vers d’autres nœuds de contexte. Avant de supprimer le nœud de contexte, **IInkAnalyzer** peut déclencher les événements suivants.

-   L’événement [**\_ IAnalysisProxyEvents :: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) lorsqu’il déplace un trait du [**IContextNode**](icontextnode.md).
-   L’événement [**\_ IAnalysisProxyEvents :: ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) avant de supprimer un [**IContextLink**](icontextlink.md) du [**IContextNode**](icontextnode.md).
-   L’événement **\_ IAnalysisProxyEvents :: ContextNodeDeleting** avant de supprimer un nœud de contexte parent qui n’a plus de nœuds enfants.

Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
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

 

 




