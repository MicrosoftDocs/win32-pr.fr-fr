---
description: Limite la zone du IAnalysisRegion à la partie de sa zone qui ne croise pas le IAnalysisRegion spécifié.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'IAnalysisRegion :: ExcludeRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530332"
---
# <a name="ianalysisregionexcluderegion-method"></a>IAnalysisRegion :: ExcludeRegion, méthode

Limite la zone du [**IAnalysisRegion**](ianalysisregion.md) à la partie de sa zone qui ne croise pas le **IAnalysisRegion** spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRegionToExclude* \[ dans\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) à exclure de ce **IAnalysisRegion**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Si les deux zones ne se croisent pas, ce [**IAnalysisRegion**](ianalysisregion.md) est inchangé.

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

[**IAnalysisRegion :: IntersectRectangle, méthode**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion :: IntersectRegion, méthode**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion :: UnionRectangle, méthode**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion :: UnionRegion, méthode**](ianalysisregion-unionregion.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




