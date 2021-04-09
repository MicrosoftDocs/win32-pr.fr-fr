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
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862710"
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
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




