---
description: Développe la zone de ce IAnalysisRegion vers la zone créée par son Union avec le rectangle spécifié.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'IAnalysisRegion :: UnionRectangle, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514635"
---
# <a name="ianalysisregionunionrectangle-method"></a>IAnalysisRegion :: UnionRectangle, méthode

Développe la zone de ce [**IAnalysisRegion**](ianalysisregion.md) vers la zone créée par son Union avec le rectangle spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRectangle* \[ dans\]
</dt> <dd>

Pointeur vers le rectangle avec lequel combiner, en coordonnées d’espace manuscrit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Les coordonnées du rectangle sont exprimées en unités HIMETRIC.

Si l’une des zones est infinie, la nouvelle zone est également infinie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
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

[**IAnalysisRegion :: IntersectRegion, méthode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion :: UnionRegion, méthode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




