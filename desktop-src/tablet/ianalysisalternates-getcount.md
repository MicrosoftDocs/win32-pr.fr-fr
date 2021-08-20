---
description: Récupère le nombre d’objets IAnalysisAlternate contenus dans la collection IAnalysisAlternates.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'IAnalysisAlternates :: GetCount, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84ff5941d4db6ca569c8a7a10a622e4b3dcdfc947284064fa009e030adae1493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967488"
---
# <a name="ianalysisalternatesgetcount-method"></a>IAnalysisAlternates :: GetCount, méthode

Récupère le nombre d’objets [**IAnalysisAlternate**](ianalysisalternate.md) contenus dans la collection [**IAnalysisAlternates**](ianalysisalternates.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulCount* \[ à\]
</dt> <dd>

Entier 32 bits non signé qui a pour valeur le nombre d’objets [**IAnalysisAlternate**](ianalysisalternate.md) contenus dans la collection [**IAnalysisAlternates**](ianalysisalternates.md) .

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

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




