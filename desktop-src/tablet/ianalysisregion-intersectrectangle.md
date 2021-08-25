---
description: Limite la zone de ce IAnalysisRegion à la zone créée par son intersection avec le rectangle spécifié.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'IAnalysisRegion :: IntersectRectangle, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 074e3cee4cd20a35c780ce0c644b24c7688956d85a631f3563dd678c70c82822
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935489"
---
# <a name="ianalysisregionintersectrectangle-method"></a>IAnalysisRegion :: IntersectRectangle, méthode

Limite la zone de ce [**IAnalysisRegion**](ianalysisregion.md) à la zone créée par son intersection avec le rectangle spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIntersectingRectangle* \[ dans\]
</dt> <dd>

Pointeur vers le rectangle avec lequel effectuer l’intersection, en coordonnées d’espace manuscrit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Les coordonnées du rectangle sont exprimées en unités HIMETRIC.

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

[**IAnalysisRegion :: IntersectRegion, méthode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion :: UnionRectangle, méthode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion :: UnionRegion, méthode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




