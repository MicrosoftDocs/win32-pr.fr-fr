---
description: 'IStats :: GetControlState, méthode-la méthode GetControlState récupère l’état de la capture, qui indique si la capture est en cours d’exécution ou en pause.'
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: 'IStats :: GetControlState, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5dcc0ea5a7278364218bde23fbffdfa720070c9a54dbff0feb20abc1f161d024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063829"
---
# <a name="istatsgetcontrolstate-method"></a>IStats :: GetControlState, méthode

La méthode **GetControlState** récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsRunnning* \[ à\]
</dt> <dd>

Indicateur de l’exécution de la capture en cours, y compris si la capture est suspendue.

</dd> <dt>

*IsPaused* \[ à\]
</dt> <dd>

Indicateur signalant que la capture en cours est suspendue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                            | Description                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>   | Le NPP n’est pas connecté au réseau. appelez [IStats :: Connecter](istats-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl> | le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connecter](istats-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Remarques

Cette méthode peut être appelée chaque fois que le NPP est connecté au réseau. Vous pouvez utiliser cette méthode pour déterminer si une capture est en cours d’exécution, si la capture est suspendue ou si la capture a été arrêtée, mais que le NPP n’est pas déconnecté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats :: Connecter](istats-connect.md)
</dt> <dt>

[IStats ::P ause](istats-pause.md)
</dt> <dt>

[IStatsC :: Start](istats-start.md)
</dt> <dt>

[IStatsC :: Stop](istats-stop.md)
</dt> </dl>

 

 




