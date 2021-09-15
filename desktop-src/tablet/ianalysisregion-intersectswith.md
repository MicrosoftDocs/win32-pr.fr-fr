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
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521261"
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

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

La comparaison est en coordonnées d’espace manuscrit.

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

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




