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
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294627"
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

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

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
</dt> </dl>

 

 




