---
description: Récupère une valeur indiquant si le IAnalysisRegion représente une région infinie.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'IAnalysisRegion :: IsInfinite, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201519"
---
# <a name="ianalysisregionisinfinite-method"></a>IAnalysisRegion :: IsInfinite, méthode

Récupère une valeur indiquant si le [**IAnalysisRegion**](ianalysisregion.md) représente une région infinie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfIsInfinite* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si la zone représentée est infinie ; Sinon, **Variant \_ false**.

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

[**IAnalysisRegion :: IsEmpty, méthode**](ianalysisregion-isempty.md)
</dt> <dt>

[**IAnalysisRegion :: MakeEmpty, méthode**](ianalysisregion-makeempty.md)
</dt> <dt>

[**IAnalysisRegion :: MakeInfinite, méthode**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




