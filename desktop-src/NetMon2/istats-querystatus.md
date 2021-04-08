---
description: La méthode QueryStatus récupère l’état du NPP.
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: 'IStats :: QueryStatus, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 02e013d87734b61ad26b6563c402db1b8d4cb4f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760839"
---
# <a name="istatsquerystatus-method"></a>IStats :: QueryStatus, méthode

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

Pointeur vers une structure [NETWORKSTATUS](networkstatus.md) retournée qui indique l’état actuel (capture, pause, arrêtée, etc.) du NPP. Il incombe à l’application d’allouer et de libérer la mémoire pour la structure **NETWORKSTATUS** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est le code d’erreur suivant :



| Code de retour                                                                                              | Description                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_paramètre NMERR non valide \_**</dt> </dl> | Le paramètre *pNetworkStatus* ne pointe pas vers une structure [NETWORKSTATUS](networkstatus.md) valide. Allouez de la mémoire pour cette structure et rappelez la méthode **IStats :: QueryStatus** .<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode peut être appelée à tout moment après l’appel de la méthode [CreateNPPInterface](createnppinterface.md) . Il peut être appelé pour déterminer si le NPP est connecté au réseau, pour déterminer l’état de la capture en cours et pour déterminer si des déclencheurs sont en attente. Toutefois, avant d’appeler cette méthode, vous devez allouer la mémoire nécessaire à la structure [NETWORKSTATUS](networkstatus.md) et libérer cette mémoire lorsque la structure n’est plus nécessaire.

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

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




