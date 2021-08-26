---
description: Récupère l’indicateur d’analyse à l’origine de cet avertissement.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'IAnalysisWarning :: GetHint, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51eb76839b157c2ac9611ef9be978ea967c8e9b3506513a23b0ca70906dd32b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940509"
---
# <a name="ianalysiswarninggethint-method"></a>IAnalysisWarning :: GetHint, méthode

Récupère l’indicateur d’analyse à l’origine de cet avertissement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAnalysisHint* \[ à\]
</dt> <dd>

Nœud de contexte d’indicateur d’analyse qui a provoqué cet avertissement, ou **null** si un indicateur d’analyse n’a pas provoqué cet avertissement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *pAnalysisHint* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte d’indicateur d’analyse.

 

Un exemple d’indicateur d’analyse qui génère un [**IAnalysisWarning**](ianalysiswarning.md) est un indicateur d’analyse qui contient un Factoid mal orthographié. Dans ce cas, l’analyse des encres retourne un [**IAnalysisStatus**](ianalysisstatus.md) qui contient un **IAnalysisWarning** qui fait référence au nœud de contexte d’indicateur d’analyse avec le Factoid mal orthographié. En outre, dans ce cas, la méthode [**IAnalysisWarning :: GetWarningCode**](ianalysiswarning-getwarningcode.md) de l’avertissement d’analyse retourne une valeur [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ FactoidNotSupported**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IInkAnalyzer :: Analyze, méthode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

