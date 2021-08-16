---
description: Se produit avant que le IInkAnalyzer déplace un objet IContextNode vers une nouvelle position dans la collection de sous-nœuds du nœud parent.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: '_IAnalysisProxyEvents :: ContextNodeMovingToPosition, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4cd814e45692d90c77bad8c46fea5dfd8534bd769a07a9d0bc1648ecafc7b2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857148"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_Événement IAnalysisProxyEvents :: ContextNodeMovingToPosition

Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) déplace un objet [**IContextNode**](icontextnode.md) vers une nouvelle position dans la collection de sous-nœuds du nœud parent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalyzer* \[ dans\]
</dt> <dd>

Objet [**IInkAnalyzer**](iinkanalyzer.md) qui déplace l’objet [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pISubNodeToMove* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) à déplacer.

</dd> <dt>

*pParentContextNode* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) parent de *pISubNodeToMove*.

</dd> <dt>

*ulNewIndex* \[ dans\]
</dt> <dd>

Nouvel emplacement de *pISubNodeToMove* dans la collection de sous-nœuds du nœud parent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui déplace un [**IContextNode**](icontextnode.md) dans la collection de sous-nœuds du nœud parent (voir [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)).

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

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




