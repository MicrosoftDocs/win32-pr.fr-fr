---
title: IReferenceClock méthode GetTime
description: La méthode GetTime récupère le temps de référence actuel.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Méthode GetTime format Windows Media
- Méthode GetTime Windows Media format, interface IReferenceClock
- Interface IReferenceClock Windows Media format, GetTime, méthode
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7756240e8987199e1f1b5d79e3f0b676d4808520781fbac18dfa18dd75e88d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055439"
---
# <a name="ireferenceclockgettime-method"></a>IReferenceClock :: GetTime, méthode

La méthode **getTime** récupère le temps de référence actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTime* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure actuelle, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                               | Description                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | S_OK<br/>              |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Le paramètre *pTime* a la **valeur null**.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





