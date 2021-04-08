---
description: Se produit après que le IInkAnalyzer a créé un objet IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: '_IAnalysisProxyEvents :: ContextNodeCreated, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103953489"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Événement IAnalysisProxyEvents :: ContextNodeCreated

Se produit après que le [**IInkAnalyzer**](iinkanalyzer.md) a créé un objet [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalyzer* \[ dans\]
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) créant l’objet [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pContextNodeCreated* \[ dans\]
</dt> <dd>

Nouvel objet [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui crée un [**IContextNode**](icontextnode.md).

Lorsque le [**IInkAnalyzer**](iinkanalyzer.md) crée un [**IContextNode**](icontextnode.md), le nouveau **IContextNode** ne contient aucun trait, ne contient pas de liens vers d’autres objets **IContextNode** et peut ne pas avoir toutes ses propriétés définies. En outre, le nouveau **IContextNode** est ajouté à la fin de la collection de sous-nœuds du nœud parent (consultez [**IContextNode :: GetParentNode**](icontextnode-getparentnode.md) et [**IContextNode :: GetSubNodes**](icontextnode-getsubnodes.md)). Après cet événement, **IInkAnalyzer** peut déclencher les événements suivants.

-   L’événement [**\_ IAnalysisProxyEvents :: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) lorsqu’il déplace un trait d’un nœud de contexte à un autre.
-   L’événement [**\_ IAnalysisProxyEvents :: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) lorsqu’il ajoute un [**IContextLink**](icontextlink.md) à un [**IContextNode**](icontextnode.md).
-   L’événement [**\_ IAnalysisProxyEvents :: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) lors de la modification de l’ordre d’un [**IContextNode**](icontextnode.md) dans la collection de sous-nœuds du nœud parent.
-   [**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement [**\_ IAnalysisProxyEvents :: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) une fois qu’il a résolu l’état du [**IContextNode**](icontextnode.md) pour cette phase d’analyse.

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

 

 




