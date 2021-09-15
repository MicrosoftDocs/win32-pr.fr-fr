---
description: Obtient une valeur qui indique le niveau de confiance de l’IInkAnalyzer dans la précision du IAnalysisAlternate.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'IAnalysisAlternate :: GetRecognitionConfidence, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523312"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a>IAnalysisAlternate :: GetRecognitionConfidence, méthode

Obtient une valeur qui indique le niveau de confiance de l' [**IInkAnalyzer**](iinkanalyzer.md) dans la précision du [**IAnalysisAlternate**](ianalysisalternate.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pConfidence* \[ à\]
</dt> <dd>

Pointeur vers une [**énumération InkRecognitionConfidence**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) qui indique le niveau de confiance que le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) a dans la précision de l’alternative de reconnaissance.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**RecognitionConfidence**](recognitionconfidence.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




