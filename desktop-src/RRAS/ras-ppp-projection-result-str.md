---
title: Structure RAS_PPP_PROJECTION_RESULT (rassapi. h)
description: La \_ structure du \_ résultat de projection PPP RAS \_ est utilisée pour signaler les résultats des différentes opérations de projection PPP pour un port.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce1bb82b34490f8a1f3734225cbde1e761c575a2019a30db7790bfc7fa3c169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789583"
---
# <a name="ras_ppp_projection_result-structure"></a>\_Structure du \_ résultat de projection PPP RAS \_

\[la structure du **\_ \_ \_ résultat de PROJECTION PPP RAS** n’est pas prise en charge à partir de Windows Vista.\]

La structure du **\_ \_ \_ résultat de projection PPP RAS** est utilisée pour signaler les résultats des différentes opérations de projection PPP pour un port.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a>Membres

<dl> <dt>

**nbf**
</dt> <dd>

Structure [**de \_ \_ \_ résultat NBFCP PPP d’accès distant**](ras-ppp-nbfcp-result-str.md) qui signale le résultat d’une opération de projection d’une fréquence d’images NetBEUI PPP (NBF).

</dd> <dt>

**adressesIP**
</dt> <dd>

Structure [**de \_ \_ \_ résultat IPCP PPP IPX**](ras-ppp-ipcp-result-str.md) qui signale le résultat d’une opération de projection IP (Internet Protocol) ppp.

</dd> <dt>

**‡**
</dt> <dd>

structure [**de \_ \_ \_ résultat RAS ppp IPXCP**](ras-ppp-ipxcp-result-str.md) qui signale le résultat d’une opération de projection ppp internetwork Packet Exchange (IPX).

</dd> <dt>

**at**
</dt> <dd>

Structure [**de \_ \_ \_ résultat du protocole ATCP PPP RAS**](ras-ppp-atcp-result-str.md) .

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure signale les résultats de la projection pour les protocoles NetBEUI, TCP/IP et IPX. Chaque structure PPP a un membre **dwError** qui indique si les autres informations de la structure sont valides. Si **dwError** n’est pas une \_ erreur, les autres informations sont valides. Si **dwError** est l’un des codes d’erreur dans Winerror. h ou Raserror. h, les autres informations ne sont pas valides.

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

[**\_résultat du protocole \_ ATCP PPP RAS \_**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**\_résultat du protocole \_ IPCP PPP RAS \_**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**\_résultat RAS PPP \_ IPXCP \_**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**\_résultat de \_ NBFCP \_ PPP RAS**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





