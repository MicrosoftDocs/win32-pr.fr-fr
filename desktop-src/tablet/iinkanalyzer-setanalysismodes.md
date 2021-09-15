---
description: Modifie les indicateurs qui contrôlent la manière dont le IInkAnalyzer effectue l’analyse de l’encre.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'IInkAnalyzer :: SetAnalysisModes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 826d31fd5b61db2332ef953d55b2cf6c6331995b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521252"
---
# <a name="iinkanalyzersetanalysismodes-method"></a>IInkAnalyzer :: SetAnalysisModes, méthode

Modifie les indicateurs qui contrôlent la manière dont le [**IInkAnalyzer**](iinkanalyzer.md) effectue l’analyse de l’encre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*analysisMode* \[ dans\]
</dt> <dd>

Combinaison d’opérations de bits des valeurs d’énumération [**AnalysisModes**](analysismodes.md) .

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

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer :: GetAnalysisModes, méthode**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




