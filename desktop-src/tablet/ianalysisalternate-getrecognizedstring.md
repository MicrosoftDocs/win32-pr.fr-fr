---
description: Obtient la valeur de chaîne reconnue de l’objet IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'IAnalysisAlternate :: GetRecognizedString, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79d0967d2653a68145a9a50c34134d176d78674c5ea5729230035edd65a5e6b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008489"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a>IAnalysisAlternate :: GetRecognizedString, méthode

Obtient la valeur de chaîne reconnue de l’objet [**IAnalysisAlternate**](ianalysisalternate.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbstrRecognizedString* \[ à\]
</dt> <dd>

Pointeur vers le **BSTR** qui a pour valeur la valeur de chaîne reconnue.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer :: GetRecognizedString, méthode**](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




