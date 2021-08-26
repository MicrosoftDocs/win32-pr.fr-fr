---
description: Déplace le IInkAnalysisRecognizer spécifié à la première position dans la liste de reconnaissance d’encre de l’objet IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'IInkAnalyzer :: SetHighestPriorityInkAnalysisRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8404a2e1e89980ce5e8cadac1a468b3383d37d4952349f3702539975a304ac92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935209"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>IInkAnalyzer :: SetHighestPriorityInkAnalysisRecognizer, méthode

Déplace le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) spécifié à la première position dans la liste de reconnaissance d’encre de l’objet [**IInkAnalyzer**](iinkanalyzer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInkAnalysisRecognizer* \[ dans\]
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à placer à la première position.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Pour récupérer la liste des détecteurs d’encre par ordre de priorité, appelez la [**méthode IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).

Cette méthode n’affecte pas l’ordre des autres objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dans la liste des reconnaissance d’encre de l’objet [**IInkAnalyzer**](iinkanalyzer.md) .

L’ordre des détecteurs d’encre retournés par la [**méthode IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indique l’ordre dans lequel le [**IInkAnalyzer**](iinkanalyzer.md) évalue les objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponibles.

L’utilisation des reconnaissances d’encre est évaluée en fonction de leur ordre dans la liste.

Pendant l’analyse de l’encre, [**IInkAnalyzer**](iinkanalyzer.md) itère au sein des détecteurs d’encre dans sa liste jusqu’à ce qu’il trouve un module de reconnaissance qui prend en charge la langue et d’autres propriétés des traits. Ce module de reconnaissance est utilisé pour la reconnaissance de l’encre pour ces traits.

Si le [**IInkAnalyzer**](iinkanalyzer.md) ne trouve pas de [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) qui prend en charge un ensemble de traits pendant l’analyse, le **IInkAnalyzer** génère un [**IAnalysisWarning**](ianalysiswarning.md) avec un code d’avertissement de **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (consultez [**IAnalysisWarning :: GetWarningCode**](ianalysiswarning-getwarningcode.md)).

## <a name="requirements"></a>Configuration requise



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

[**IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




