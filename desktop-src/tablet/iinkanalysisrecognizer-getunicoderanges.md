---
description: Récupère un tableau de plages de caractères qui représentent les plages de caractères Unicode prises en charge.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'IInkAnalysisRecognizer :: GetUnicodeRanges, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862706"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>IInkAnalysisRecognizer :: GetUnicodeRanges, méthode

Récupère un tableau de plages de caractères qui représentent les plages de caractères Unicode prises en charge.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulNumberOfRanges* \[ in, out\]
</dt> <dd>

Nombre de plages de caractères pointées par *ppulLowUnicode*.

</dd> <dt>

*ppulLowUnicode* \[ à\]
</dt> <dd>

Pointeur vers un tableau de plages de caractères représentant les plages de caractères Unicode prises en charge.

</dd> <dt>

*ppusUnicodeRangeLength* \[ à\]
</dt> <dd>

Pointeur vers un tableau de valeurs indiquant la longueur de chaque tableau vers par *ppulLowUnicode*.

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

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




