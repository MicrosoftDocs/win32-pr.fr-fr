---
title: Structure RAS_PPP_ATCP_RESULT (rassapi. h)
description: La \_ \_ \_ structure de résultat du protocole ATCP PPP RAS est utilisée pour signaler le résultat d’une opération de projection de protocole AppleTalk pour un port.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa3122026613ba5012f950a98a615dbb8c9ef34133a2a24249fca545eaa2060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789633"
---
# <a name="ras_ppp_atcp_result-structure"></a>\_Structure de résultat du protocole ATCP PPP RAS \_ \_

\[la structure du **\_ résultat du protocole \_ ATCP \_ PPP RAS** n’est pas prise en charge à partir de Windows Vista.\]

La structure de résultat du protocole **\_ \_ ATCP \_ PPP RAS** est utilisée pour signaler le résultat d’une opération de projection de protocole AppleTalk pour un port.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwError**
</dt> <dd>

Spécifie une valeur qui indique les résultats de l’opération de projection AppleTalk. La valeur aucune \_ erreur indique la réussite, auquel cas le membre **wszAddress** est valide. Si l’opération de projection échoue, **dwError** est un code d’erreur de Winerror. h ou Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Spécifie une chaîne Unicode terminée par le caractère null qui spécifie l’adresse IP affectée au client distant.

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

[**résultat de la \_ projection PPP RAS \_ \_**](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





