---
title: Méthode IReferenceClock AdviseTime
description: La méthode AdviseTime demande une notification asynchrone indiquant qu’une heure s’est écoulée.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Méthode AdviseTime format Windows Media
- Méthode AdviseTime format Windows Media, interface IReferenceClock
- Interface IReferenceClock Windows Media format, méthode AdviseTime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523036"
---
# <a name="ireferenceclockadvisetime-method"></a>IReferenceClock :: AdviseTime, méthode

La méthode **AdviseTime** demande une notification asynchrone indiquant qu’une heure s’est écoulée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rtBaseTime* \[ dans\]
</dt> <dd>

Temps de référence de base, en unités de 100 nanosecondes.

</dd> <dt>

*rtStreamTime* \[ dans\]
</dt> <dd>

Temps de décalage du flux, en unités de 100 nanosecondes.

</dd> <dt>

*hEvent* \[ dans\]
</dt> <dd>

Handle vers un événement, créé par l’appelant. Cet événement est signalé lorsque la durée spécifiée est écoulée.

</dd> <dt>

*pdwAdviseCookie* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un identificateur pour la demande. Il est utilisé pour identifier cet appel à **AdviseTime** à l’avenir, par exemple, pour annuler la demande.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                               | Description                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | S_OK<br/>                        |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Le paramètre *pdwAdviseCookie* a la **valeur null**.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>    | Échec non spécifié.<br/>                         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





