---
description: Expose une méthode pour évaluer si un objet IContextNode satisfait ou échoue à un critère spécifié.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interface IMatchesCriteriaCallBack (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc661f47c77d615df95f63e58beccbbf125b93078392a63f86ed50f52cc5636d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718968"
---
# <a name="imatchescriteriacallback-interface"></a>Interface IMatchesCriteriaCallBack

Expose une méthode pour évaluer si un objet [**IContextNode**](icontextnode.md) satisfait ou échoue à un critère spécifié.

## <a name="members"></a>Membres

L’interface **IMatchesCriteriaCallBack** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMatchesCriteriaCallBack** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMatchesCriteriaCallBack** possède ces méthodes.



| Méthode                                                                      | Description                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) | En cas de substitution dans une classe dérivée, évalue si un objet [**IContextNode**](icontextnode.md) spécifié répond aux critères.<br/> |



 

## <a name="remarks"></a>Remarques

Pour utiliser la méthode [**IInkAnalyzer :: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) ou [**IInkAnalyzer :: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), créez une classe qui implémente **IMatchesCriteriaCallBack**. Implémentez [**IMatchesCriteriaCallBack :: EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) pour retourner la **\_ valeur variant true** si l’objet [**IContextNode**](icontextnode.md) correspond à vos critères, et **Variant \_ false** dans le cas contraire. Pour certains critères, vous devrez peut-être fournir un moyen d’initialiser ou de maintenir l’état de votre objet **IMatchesCriteriaCallBack** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer :: FindNodesWithCallBack, méthode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer :: FindNodesWithCallBackInSubTree, méthode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

