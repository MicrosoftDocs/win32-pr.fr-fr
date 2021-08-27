---
description: Limite la zone du IAnalysisRegion à la zone créée par son intersection avec le IAnalysisRegion spécifié.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'IAnalysisRegion :: IntersectRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0db58dcc7fc1c1e7458cf804eb82af236de8f1997ddcc658391da19641d1cfdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058079"
---
# <a name="ianalysisregionintersectregion-method"></a>IAnalysisRegion :: IntersectRegion, méthode

Limite la zone du [**IAnalysisRegion**](ianalysisregion.md) à la zone créée par son intersection avec le **IAnalysisRegion** spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRegionToIntersect* \[ dans\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) avec lequel effectuer l’intersection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Si les deux zones ne se croisent pas, la nouvelle zone est vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**IAnalysisRegion :: ExcludeRegion, méthode**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion :: IntersectRectangle, méthode**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion :: UnionRectangle, méthode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion :: UnionRegion, méthode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




