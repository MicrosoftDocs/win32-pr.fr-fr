---
title: Structure de IP_NETWORK (RTM. h)
description: La \_ structure du réseau IP décrit une adresse réseau IP.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK de la structure RAS
- Point d’accès RAS du pointeur de structure PIP_NETWORK
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742477"
---
# <a name="ip_network-structure"></a>\_Structure de réseau IP

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La structure du **\_ réseau IP** décrit une adresse réseau IP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a>Membres

<dl> <dt>

**N \_ numéro Netnumber**
</dt> <dd>

Spécifie le numéro de réseau IP exprimé comme une adresse IP dans l’ordre des octets de l’ordinateur.

</dd> <dt>

**N \_ masque réseau**
</dt> <dd>

Spécifie le masque de réseau. Appliquez ce masque à l’adresse IP afin d’extraire l’adresse réseau. Le masque de réseau est dans l’ordre des octets de l’ordinateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                        |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence de la version 1 du gestionnaire de tables de routage](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Structures de la version 1 du gestionnaire de tables de routage](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_itinéraire IP \_ RTM**](rtm-ip-route.md)
</dt> </dl>

 

 





