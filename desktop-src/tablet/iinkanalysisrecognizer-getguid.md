---
description: Récupère l’identificateur global unique (GUID) du module de reconnaissance.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'IInkAnalysisRecognizer :: GetGuid, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b5fbf2b07b2a63f2fdb088c38a5e03e4182c4e38528208c039f927b282755344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596739"
---
# <a name="iinkanalysisrecognizergetguid-method"></a>IInkAnalysisRecognizer :: GetGuid, méthode

Récupère l’identificateur global unique (GUID) du module de reconnaissance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PID* \[ à\]
</dt> <dd>

GUID qui identifie ce [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

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

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




