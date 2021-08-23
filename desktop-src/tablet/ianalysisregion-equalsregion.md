---
description: Détermine si le IAnalysisRegion spécifié contient la même valeur que l’objet IAnalysisRegion actuel.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'IAnalysisRegion :: EqualsRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: aecf7bd065c2da0c507c2424c0305526510c9d4f64844dfa229183cf43d5554a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596799"
---
# <a name="ianalysisregionequalsregion-method"></a>IAnalysisRegion :: EqualsRegion, méthode

Détermine si le [**IAnalysisRegion**](ianalysisregion.md) spécifié contient la même valeur que l’objet **IAnalysisRegion** actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pOtherRegion* \[ dans\]
</dt> <dd>

Objet [**IAnalysisRegion**](ianalysisregion.md) à comparer avec le **IAnalysisRegion** actif.

</dd> <dt>

*pfRegionsEqual* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si le [**IAnalysisRegion**](ianalysisregion.md) spécifié contient la même valeur que le IAnalysisRegion en cours ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

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
</dt> </dl>

 

 




