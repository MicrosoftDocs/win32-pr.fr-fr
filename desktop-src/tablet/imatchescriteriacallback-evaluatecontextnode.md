---
description: En cas de substitution dans une classe dérivée, évalue si un objet IContextNode spécifié répond aux critères.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'IMatchesCriteriaCallBack :: EvaluateContextNode, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5855928e0827632240c8230bdcc57dff836c5287eec61f2911cc62367a8915f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719049"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a>IMatchesCriteriaCallBack :: EvaluateContextNode, méthode

En cas de substitution dans une classe dérivée, évalue si un objet [**IContextNode**](icontextnode.md) spécifié répond aux critères.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContextNodeToEvaluate* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) à évaluer.

</dd> <dt>

*pbResult* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si *pContextNodeToEvaluate* correspond aux critères ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Pour utiliser la méthode [**IInkAnalyzer :: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) ou [**IInkAnalyzer :: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), créez une classe qui implémente [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md). Implémentez **IMatchesCriteriaCallBack :: EvaluateContextNode** pour retourner la **\_ valeur variant true** si l’objet [**IContextNode**](icontextnode.md) correspond à vos critères, et **Variant \_ false** dans le cas contraire. Pour certains critères, vous devrez peut-être fournir un moyen d’initialiser ou de maintenir l’état de votre objet **IMatchesCriteriaCallBack** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesWithCallBack, méthode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




