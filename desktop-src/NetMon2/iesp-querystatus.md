---
description: Récupère l’État NPP.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'IESP :: QueryStatus, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3435ed832484042bfeb9229e4b46fa34441cb395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202311"
---
# <a name="iespquerystatus-method"></a>IESP :: QueryStatus, méthode

La méthode **QueryStatus** récupère l’État NPP.

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

Pointeur vers une structure [NETWORKSTATUS](networkstatus.md) retournée qui indique l’état actuel (capture, pause, arrêtée, etc.) du NPP. L’utilisateur doit allouer et libérer la mémoire pour la structure NETWORKSTATUS.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est le code d’erreur suivant :



| Code de retour                                                                                              | Description                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_paramètre NMERR non valide \_**</dt> </dl> | Le paramètre *pNetworkStatus* ne pointe pas vers une structure [NETWORKSTATUS](networkstatus.md) valide. Allouez de la mémoire pour cette structure et appelez à nouveau **IESP :: QueryStatus** .<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode peut être appelée à tout moment après l’appel de [CreateNPPInterface](createnppinterface.md) . Vous pouvez appeler cette méthode pour voir si le NPP est connecté au réseau, pour déterminer l’état de la capture en cours et pour déterminer si des déclencheurs sont en attente.

Avant d’appeler cette méthode, allouez la mémoire requise pour la structure [NETWORKSTATUS](networkstatus.md) et libérez cette mémoire lorsque la structure n’est plus nécessaire.

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

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




