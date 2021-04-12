---
title: Structure RAS_PPP_IPCP_RESULT (rassapi. h)
description: La \_ structure du \_ résultat IPCP PPP IPX \_ est utilisée pour signaler le résultat d’une opération de projection IP (Internet Protocol) ppp pour un port.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508642"
---
# <a name="ras_ppp_ipcp_result-structure"></a>\_Structure du \_ résultat IPCP PPP \_ IPX

\[La structure du **\_ \_ \_ résultat IPCP PPP IPX** n’est pas prise en charge à partir de Windows Vista.\]

La structure du **\_ \_ \_ résultat IPCP PPP IPX** est utilisée pour signaler le résultat d’une opération de projection IP (Internet Protocol) ppp pour un port.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwError**
</dt> <dd>

Indique les résultats de l’opération de projection IP. La valeur aucune \_ erreur indique la réussite, auquel cas le membre **wszAddress** est valide. En cas d’échec de l’opération de projection, **dwError** est un code d’erreur de Winerror. h ou Raserror. h.

</dd> <dt>

**wszAddress**
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui spécifie l’adresse IP affectée au client distant. Cette chaîne se présente sous la forme *a ***.** _b_* _._ *_c_*_._ * _d_.

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

 

 





