---
title: Structure RAS_PPP_NBFCP_RESULT (rassapi. h)
description: La \_ \_ \_ structure de résultat RAS PPP NBFCP est utilisée pour signaler le résultat d’une opération de projection d’une fréquence d’accès PPP NetBEUI (NBF) pour un port.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103999"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>\_Structure des résultats RAS PPP \_ NBFCP \_

\[La structure des **\_ \_ \_ résultats ppp ppp NBFCP** n’est pas prise en charge à partir de Windows Vista.\]

La structure de **\_ \_ \_ résultat RAS PPP NBFCP** est utilisée pour signaler le résultat d’une opération de projection d’une fréquence d’accès PPP NetBEUI (NBF) pour un port.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwError**
</dt> <dd>

Indique les résultats de l’opération de projection NBF. La valeur aucune \_ erreur indique la réussite, auquel cas le membre **wszWksta** contient le nom de l’ordinateur distant. En cas d’échec de l’opération de projection, **dwError** est un code d’erreur de Winerror. h ou Raserror. h.

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

Ignorer ce membre sur le serveur ; elle s’applique uniquement au client.

</dd> <dt>

**szName**
</dt> <dd>

Ignorer ce membre sur le serveur ; elle s’applique uniquement au client.

</dd> <dt>

**wszWksta**
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui spécifie le nom NetBIOS de la station de travail cliente RAS.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du service d’accès à distance (RAS)](about-remote-access-service.md)
</dt> <dt>

[Structures d’administration de serveur RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Port RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**résultat de la \_ projection PPP RAS \_ \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





