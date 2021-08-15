---
description: Se produit lorsque le IInkAnalyzer déplace un trait d’un objet IContextNode à un autre.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: '_IAnalysisProxyEvents :: StrokeReparented, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e9262eb7b4ce2b323669eeb084abb597b5fe00488df90fc5fde0b2876b7e953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967868"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a>\_Événement IAnalysisProxyEvents :: StrokeReparented

Se produit lorsque le [**IInkAnalyzer**](iinkanalyzer.md) déplace un trait d’un objet [**IContextNode**](icontextnode.md) à un autre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalyzer* \[ dans\]
</dt> <dd>

Objet [**IInkAnalyzer**](iinkanalyzer.md) qui déplace le trait.

</dd> <dt>

*lStrokeIdToMove* \[ dans\]
</dt> <dd>

Identificateur du trait à déplacer.

</dd> <dt>

*pSourceContextNode* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) à partir duquel le trait est déplacé.

</dd> <dt>

*pDestinationContextNode* \[ dans\]
</dt> <dd>

Objet [**IContextNode**](icontextnode.md) vers lequel le trait est déplacé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Utilisez cet événement lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Cet événement se produit pendant la phase de rapprochement de l’analyse de l’encre, ou en réponse à une méthode **IInkAnalyzer** qui déplace les données de trait d’un [**IContextNode**](icontextnode.md) vers un autre.

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

 

 




