---
description: Se produit après que le IInkAnalyzer a mis à jour une ou plusieurs propriétés d’un objet IContextNode.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: '_IAnalysisProxyEvents :: ContextNodePropertiesUpdated, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531260"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a>\_Événement IAnalysisProxyEvents :: ContextNodePropertiesUpdated

Se produit après que le [**IInkAnalyzer**](iinkanalyzer.md) a mis à jour une ou plusieurs propriétés d’un objet [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalyzer* \[ dans\]
</dt> <dd>

Objet [**IInkAnalyzer**](iinkanalyzer.md) qui met à jour les propriétés.

</dd> <dt>

*pContextNodeUpdated* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) dont les propriétés sont mises à jour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode d’analyseur d’encre qui modifie les propriétés d’un [**IContextNode**](icontextnode.md) (consultez [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md)).

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

[Propriétés du nœud de contexte](context-node-properties.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




