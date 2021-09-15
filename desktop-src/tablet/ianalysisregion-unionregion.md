---
description: Développe la zone de ce IAnalysisRegion vers la zone créée par son Union avec le IAnalysisRegion spécifié.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'IAnalysisRegion :: UnionRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530329"
---
# <a name="ianalysisregionunionregion-method"></a>IAnalysisRegion :: UnionRegion, méthode

Développe la zone de ce [**IAnalysisRegion**](ianalysisregion.md) vers la zone créée par son Union avec le **IAnalysisRegion** spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRegionToUnion* \[ dans\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) avec lequel effectuer la combinaison.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Si l’une des zones est infinie, la nouvelle zone est également infinie.

## <a name="requirements"></a>Spécifications



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

[**IAnalysisRegion :: IntersectRegion, méthode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion :: UnionRectangle, méthode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




