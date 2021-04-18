---
description: Récupère une valeur indiquant si le IAnalysisRegion représente une zone vide.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'IAnalysisRegion :: IsEmpty, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533604"
---
# <a name="ianalysisregionisempty-method"></a>IAnalysisRegion :: IsEmpty, méthode

Récupère une valeur indiquant si le [**IAnalysisRegion**](ianalysisregion.md) représente une zone vide.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfIsEmpty* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si la région représentée est vide ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

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

[**IAnalysisRegion :: IsInfinite, méthode**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**IAnalysisRegion :: MakeEmpty, méthode**](ianalysisregion-makeempty.md)
</dt> <dt>

[**IAnalysisRegion :: MakeInfinite, méthode**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




