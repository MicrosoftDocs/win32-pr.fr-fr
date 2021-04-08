---
title: Structure de RTM_IPX_ROUTE (RTM. h)
description: La \_ \_ structure d’itinéraires IPX RTM contient des informations qui décrivent un itinéraire pour la famille de protocoles IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE de la structure RAS
- Point d’accès RAS du pointeur de structure PRTM_IPX_ROUTE
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941903"
---
# <a name="rtm_ipx_route-structure"></a>Structure de l' \_ itinéraire IPX RTM \_

\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]

La structure d' **\_ \_ itinéraires IPX RTM** contient des informations qui décrivent un itinéraire pour la famille de protocoles IPX.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
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

Spécifie une structure de [**\_ \_ données spécifique au protocole**](protocol-specific-data.md) contenant la mémoire réservée pour les données spécifiques aux protocoles de routage.

</dd> <dt>

**Réseau de RR \_**
</dt> <dd>

Spécifie une structure [**\_ réseau IPX**](ipx-network.md) qui contient une adresse réseau IP.

</dd> <dt>

**\_NEXTHOPADDRESS RR**
</dt> <dd>

Spécifie une structure d' [**\_ \_ \_ adresse de tronçon suivant IPX**](ipx-next-hop-address.md) qui contient l’adresse du routeur de tronçon suivant.

</dd> <dt>

**\_FAMILYSPECIFICDATA RR**
</dt> <dd>

Spécifie une structure de [**\_ \_ données spécifique à IPX**](ipx-specific-data.md) qui contient des données spécifiques à la famille de protocoles IPX.

</dd> </dl>

## <a name="remarks"></a>Notes

Les membres de la structure d' **\_ \_ itinéraires IPX RTM** sont tous alignés sur le **DWORD** .

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

[Structures de la version 1 du gestionnaire de tables de routage \_ \_](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_réseau IPX**](ipx-network.md)
</dt> <dt>

[**\_adresse du \_ tronçon \_ suivant IPX**](ipx-next-hop-address.md)
</dt> <dt>

[**\_données spécifiques à IPX \_**](ipx-specific-data.md)
</dt> </dl>

 

 





