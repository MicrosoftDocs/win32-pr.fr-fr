---
description: Se produit avant que le IInkAnalyzer accède aux données de trait.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: '_IAnalysisEvents :: UpdateStrokesCache, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a5854c8061a12dc558a2ca20ebd893880f899b2113065abd9b8122c53812aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047371"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a>\_Événement IAnalysisEvents :: UpdateStrokesCache

Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) accède aux données de trait.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulStrokeIdsCount* \[ dans\]
</dt> <dd>

Nombre d’identificateurs de trait dans *plStrokeIds*.

</dd> <dt>

*plStrokeIds* \[ dans\]
</dt> <dd>

Identificateurs des traits dont les données de paquet ont été effacées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement lors de l’analyse de l’encre lorsqu’il accède à un ou plusieurs traits pour lesquels les données du paquet ont été effacées. Pour mettre à jour les données de paquets de trait, utilisez la méthode de [**méthode IInkAnalyzer :: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md) .

[**IInkAnalyzer**](iinkanalyzer.md) ne déclenche pas cet événement lors de l’accès à un nœud de feuille manuscrite partiellement rempli lorsque l’emplacement du nœud n’a pas été défini par le **IInkAnalyzer**.

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

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer :: UpdateStrokesData, méthode**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




