---
description: Indique le niveau de confiance que le IInkAnalyzer a dans la précision du résultat de la reconnaissance.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Énumération RecognitionConfidence (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b5943b303c01a681b1df9d6d919df1822a5f2345c85fb5c52e3ab865ee58dd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596629"
---
# <a name="recognitionconfidence-enumeration"></a>Énumération RecognitionConfidence

Indique le niveau de confiance que le [**IInkAnalyzer**](iinkanalyzer.md) a dans la précision du résultat de la reconnaissance.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ Strong**
</dt> <dd>

Confiance forte dans le résultat ou l’autre.

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ intermédiaire**
</dt> <dd>

Confiance intermédiaire dans le résultat ou l’autre.

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ médiocre**
</dt> <dd>

Confiance faible dans le résultat ou l’autre.

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ inconnu**
</dt> <dd>

Le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) qui a généré le texte reconnu ne prend pas en charge les niveaux de confiance.

</dd> </dl>

## <a name="remarks"></a>Remarques

[**IInkAnalyzer**](iinkanalyzer.md) utilise un ou plusieurs objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pour convertir l’écriture manuscrite en texte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisAlternate :: GetRecognitionConfidence, méthode**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Propriétés du nœud de contexte](context-node-properties.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




