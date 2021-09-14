---
title: Structure RAS_PPP_IPXCP_RESULT (rassapi. h)
description: la \_ structure du résultat d’accès distant ppp ppp \_ \_ est utilisée pour signaler le résultat d’une opération de projection ppp IPX (packet network Exchange) pour un port.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS_PPP_IPXCP_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416640"
---
# <a name="ras_ppp_ipxcp_result-structure"></a>Structure des résultats du protocole d’accès distant \_ PPP \_ IPXCP \_

\[la structure des **\_ \_ \_ résultats IPXCP PPP d’accès distant** n’est pas prise en charge à partir de Windows Vista.\]

la structure du **\_ \_ \_ résultat d’accès distant ppp ppp** est utilisée pour signaler le résultat d’une opération de projection ppp IPX (packet network Exchange) pour un port.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwError**
</dt> <dd>

Indique les résultats de l’opération de projection IPX. La valeur aucune \_ erreur indique la réussite, auquel cas le membre **wszAddress** est valide. En cas d’échec de l’opération de projection, **dwError** est un code d’erreur de Winerror. h ou Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui spécifie l’adresse IPX assignée au client distant. Cette chaîne a le * net ***.** formulaire de _nœud_ .

</dd> </dl>

## <a name="requirements"></a>Spécifications



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

 

 





