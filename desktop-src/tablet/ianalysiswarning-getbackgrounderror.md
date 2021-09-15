---
description: Récupère le code d’erreur de l’opération d’analyse de l’encre en arrière-plan si une erreur s’est produite.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'IAnalysisWarning :: GetBackgroundError, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523296"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>IAnalysisWarning :: GetBackgroundError, méthode

Récupère le code d’erreur de l’opération d’analyse de l’encre en arrière-plan si une erreur s’est produite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Si une erreur se produit dans une opération d’analyse en arrière-plan, le [**IInkAnalyzer**](iinkanalyzer.md) ne peut pas retourner le code d’erreur, car il se produit dans un thread différent. Au lieu de cela, le gestionnaire d’événements [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) reçoit un [**IAnalysisStatus**](ianalysisstatus.md) qui contient un [**IAnalysisWarning**](ianalysiswarning.md) avec [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **AnalysisWarningCode \_ BackgroundException**. Ce **IAnalysisWarning** contient le code d’erreur de l’opération d’analyse en arrière-plan. En général, votre gestionnaire d’événements **\_ IAnalysisEvents :: Results** retourne ce code d’erreur afin qu’il puisse être géré ailleurs dans votre application.

## <a name="requirements"></a>Spécifications



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

[**IInkAnalyzer :: BackgroundAnalyze, méthode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents :: Results**](-ianalysisevents-results.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

