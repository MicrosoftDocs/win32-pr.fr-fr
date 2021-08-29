---
description: 'IESP :: GetControlState, méthode-la méthode GetControlState récupère l’état de la capture, qui indique si la capture est en cours d’exécution ou en pause.'
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: 'IESP :: GetControlState, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8ef791d4d892713c9bd07a693b9aa57651e2e7cf75635a1c8642ceb4a45b0776
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779199"
---
# <a name="iespgetcontrolstate-method"></a>IESP :: GetControlState, méthode

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



| Code de retour                                                                                          | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl> | Le NPP n’est pas connecté au réseau. appelez [IESP :: Connecter](iesp-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>       | le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connecter](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Remarques

Cette méthode peut être appelée chaque fois que le NPP est connecté au réseau. Vous pouvez utiliser cette méthode pour déterminer si une capture est en cours d’exécution, si la capture est suspendue ou si la capture a été arrêtée alors que le NPP est toujours connecté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP :: Connecter](iesp-connect.md)
</dt> <dt>

[IESP ::P ause](iesp-pause.md)
</dt> <dt>

[IESP :: Start](iesp-start.md)
</dt> <dt>

[IESP :: Stop](iesp-stop.md)
</dt> </dl>

 

 




