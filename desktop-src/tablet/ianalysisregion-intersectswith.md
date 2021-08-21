---
description: Détermine si la zone du IAnalysisRegion entre en intersection avec le rectangle spécifié.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'IAnalysisRegion :: IntersectsWith, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 04613e061929bba04c14be37914b22a51de0377f125b21fa29db9c56fc8dfeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720016"
---
# <a name="ianalysisregionintersectswith-method"></a>IAnalysisRegion :: IntersectsWith, méthode

Détermine si la zone du [**IAnalysisRegion**](ianalysisregion.md) entre en intersection avec le rectangle spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRectangle* \[ dans\]
</dt> <dd>

Pointeur vers le rectangle avec lequel comparer, en coordonnées d’espace manuscrit.

</dd> <dt>

*pfIsIntersecting* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si la zone du [**IAnalysisRegion**](ianalysisregion.md) entre en intersection avec le rectangle spécifié ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

La comparaison est en coordonnées d’espace manuscrit.

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

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




