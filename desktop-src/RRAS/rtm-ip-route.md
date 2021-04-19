---
title: Structure de RTM_IP_ROUTE (RTM. h)
description: La structure de l' \_ itinéraire IP RTM \_ contient des informations qui décrivent un itinéraire appartenant à la famille de protocoles IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE de la structure RAS
- Point d’accès RAS du pointeur de structure PRTM_IP_ROUTE
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516502"
---
# <a name="rtm_ip_route-structure"></a>Structure de l' \_ itinéraire IP RTM \_

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La structure de l' **\_ \_ itinéraire IP RTM** contient des informations qui décrivent un itinéraire appartenant à la famille de protocoles IP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Horodateur du RR \_**
</dt> <dd>

Spécifie l’heure à laquelle l’entrée d’itinéraire a été créée ou mise à jour pour la dernière fois. Ce membre est défini par le gestionnaire de tables de routage. L’heure est exprimée sous la forme d’une structure FILETIME.

</dd> <dt>

**\_ROUTINGPROTOCOL RR**
</dt> <dd>

Spécifie le protocole de routage qui a ajouté l’itinéraire.

</dd> <dt>

**RR \_ InterfaceId**
</dt> <dd>

Spécifie l’interface par le biais de laquelle l’itinéraire a été obtenu.

</dd> <dt>

**\_PROTOCOLSPECIFICDATA RR**
</dt> <dd>

Spécifie une structure de [**\_ \_ données spécifique au protocole**](protocol-specific-data.md) qui contient la mémoire réservée pour les données spécifiques au protocole de routage.

</dd> <dt>

**Réseau de RR \_**
</dt> <dd>

Spécifie une structure de [**\_ réseau IP**](ip-network.md) qui contient une adresse réseau IP.

</dd> <dt>

**\_NEXTHOPADDRESS RR**
</dt> <dd>

Spécifie une structure d' [**adresse IP de \_ \_ saut \_ suivant**](ip-next-hop-address.md) qui contient l’adresse du routeur de tronçon suivant.

</dd> <dt>

**\_FAMILYSPECIFICDATA RR**
</dt> <dd>

Spécifie une structure de [**\_ \_ données spécifique à l’adresse IP**](ip-specific-data.md) qui contient des données spécifiques à la famille de protocoles IP.

</dd> </dl>

## <a name="remarks"></a>Notes

Les membres de la structure d' **\_ \_ itinéraires IP RTM** sont tous alignés sur le **DWORD** .

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

[**\_réseau IP**](ip-network.md)
</dt> <dt>

[**adresse IP du \_ \_ tronçon suivant \_**](ip-next-hop-address.md)
</dt> <dt>

[**\_données IP spécifiques \_**](ip-specific-data.md)
</dt> </dl>

 

 





