---
description: Limite la zone du IAnalysisRegion à la partie de sa zone qui ne croise pas le rectangle spécifié.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'IAnalysisRegion :: ExcludeRectangle, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514197"
---
# <a name="ianalysisregionexcluderectangle-method"></a>IAnalysisRegion :: ExcludeRectangle, méthode

Limite la zone du [**IAnalysisRegion**](ianalysisregion.md) à la partie de sa zone qui ne croise pas le rectangle spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pExcludingRectangle* \[ dans\]
</dt> <dd>

Rectangle à exclure de ce [**IAnalysisRegion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Les coordonnées du rectangle sont exprimées en unités HIMETRIC.

Si les deux zones ne se croisent pas, le [**IAnalysisRegion**](ianalysisregion.md) est inchangé.

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

[**IAnalysisRegion :: ExcludeRegion, méthode**](ianalysisregion-excluderegion.md)
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

 

 




