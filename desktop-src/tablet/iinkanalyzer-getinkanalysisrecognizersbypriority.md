---
description: Récupère une collection ordonnée d’objets IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc663385006eedaca163f529af1f9f8a2da2eb5d3d41db823ffb53ee91775b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713409"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode

Récupère une collection ordonnée d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppInkAnalysisRecognizers* \[ à\]
</dt> <dd>

Collection ordonnée d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppInkAnalysisRecognizers* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

L’ordre des détecteurs dans cette collection indique l’ordre dans lequel le [**IInkAnalyzer**](iinkanalyzer.md) évalue les regroupements disponibles. Le **IInkAnalyzer** utilise la langue des traits comme critère principal pour l’application d’un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). En tant que critère secondaire, **IInkAnalyzer** compare les informations d’indicateur d’analyse aux fonctionnalités prises en charge d’un objet **IInkAnalysisRecognizer** (consultez [**IInkAnalysisRecognizer :: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)). Pour plus d’informations sur les indicateurs d’analyse, consultez la [**méthode IInkAnalyzer :: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md).

Si plusieurs [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) prennent en charge un identificateur de langue, le [**IInkAnalyzer**](iinkanalyzer.md) utilise un algorithme « ajusté » pour sélectionner le premier **IInkAnalysisRecognizer** pour analyser les traits de cette langue.

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

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer :: SetHighestPriorityInkAnalysisRecognizer, méthode**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

