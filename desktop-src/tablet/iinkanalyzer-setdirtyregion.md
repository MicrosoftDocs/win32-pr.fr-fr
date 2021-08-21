---
description: Modifie la zone qui a été modifiée depuis la dernière opération d’analyse.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'IInkAnalyzer :: SetDirtyRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a39fc420b368911788efcb9462c9c4be5b4828c82906ef2c94bb5be99ca17568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091469"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>IInkAnalyzer :: SetDirtyRegion, méthode

Modifie la zone qui a été modifiée depuis la dernière opération d’analyse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDirtyRegion* \[ dans\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) qui décrit la zone qui a été modifiée depuis la dernière opération d’analyse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Cette méthode identifie les zones qui doivent être analysées ou réanalysées. Toutes les méthodes [**IInkAnalyzer**](iinkanalyzer.md) qui ajoutent, mettent à jour ou suppriment des données de trait mettent à jour la région modifiée. Pour marquer manuellement une zone pour la réanalyse :

1.  Récupérez la région modifiée à l’aide de la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).
2.  Utilisez la méthode [**IAnalysisRegion :: UnionRegion**](ianalysisregion-unionregion.md) ou [**IAnalysisRegion :: UnionRectangle**](ianalysisregion-unionrectangle.md) pour ajouter la zone à la région à partir de l’étape 1.
3.  Utilisez la **méthode IInkAnalyzer :: SetDirtyRegion** pour mettre à jour la région modifiée.

Le [**IInkAnalyzer**](iinkanalyzer.md) analyse l’encre au sein de sa région modifiée pendant un appel à la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou à la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md). Toutefois, le **IInkAnalyzer** peut développer l’opération d’analyse pour inclure les régions voisines.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer :: AddStroke, méthode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokeForLanguage, méthode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokes, méthode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer :: AddStrokesForLanguage, méthode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStroke, méthode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer :: RemoveStrokes, méthode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer :: UpdateStrokesData, méthode**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




