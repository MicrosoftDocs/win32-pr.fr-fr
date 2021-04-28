---
description: 'IDelaydC :: QueryStatus, méthode-la méthode QueryStatus récupère l’état du NPP.'
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: 'IDelaydC :: QueryStatus, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 13d1e34b57302d263b81ed64df0b136dc01177b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118457"
---
# <a name="idelaydcquerystatus-method"></a>IDelaydC :: QueryStatus, méthode

La méthode **QueryStatus** récupère l’état du NPP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNetworkStatus* \[ à\]
</dt> <dd>

Pointeur vers une structure [NETWORKSTATUS](networkstatus.md) retournée qui indique l’état actuel (capture, pause, arrêtée, etc.) du NPP. Il vous incombe d’allouer et de libérer la mémoire associée à la structure **NETWORKSTATUS** .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est le code d’erreur suivant :



| Code de retour                                                                                              | Description                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_paramètre NMERR non valide \_**</dt> </dl> | Le paramètre *pNetworkStatus* ne pointe pas vers une structure [NETWORKSTATUS](networkstatus.md) valide. Allouez de la mémoire pour cette structure et rappelez la méthode **IDelaydC :: QueryStatus** .<br/> |



 

## <a name="remarks"></a>Notes 

Cette méthode peut être appelée à tout moment après l’appel de [CreateNPPInterface](createnppinterface.md) . Il peut être appelé pour déterminer si le NPP est connecté au réseau, pour déterminer l’état de la capture en cours et pour déterminer si des déclencheurs sont en attente.

Avant d’appeler cette méthode, vous devez allouer la mémoire nécessaire à la structure [NETWORKSTATUS](networkstatus.md) et libérer cette mémoire lorsque la structure n’est plus nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




