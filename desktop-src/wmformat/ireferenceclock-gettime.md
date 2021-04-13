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
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380977"
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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                               | Description                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | S_OK<br/>              |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Le paramètre *pTime* a la **valeur null**.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





