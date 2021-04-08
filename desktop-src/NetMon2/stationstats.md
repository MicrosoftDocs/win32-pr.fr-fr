---
description: La structure STATIONSTATS fournit des statistiques sur une station spécifique décrite par la capture en cours.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: STATIONSTATS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034322"
---
# <a name="stationstats-structure"></a>STATIONSTATS, structure

La structure **STATIONSTATS** fournit des statistiques sur une [*station*](s.md) spécifique décrite par la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a>Membres

<dl> <dt>

**NextStationStats**
</dt> <dd>

Index de la station suivante enregistrée dans le tableau de structures **STATIONSTATS** .

</dd> <dt>

**SessionPartnerList**
</dt> <dd>

Index de la liste des partenaires de station.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Ce membre est obsolète.

</dd> <dt>

**StationAddress**
</dt> <dd>

Adresse MAC de la station.

</dd> <dt>

**Remplir**
</dt> <dd>

Alignement **DWORD** .

</dd> <dt>

**TotalPacketsReceived**
</dt> <dd>

Nombre total de paquets envoyés à la station.

</dd> <dt>

**TotalDirectedPacketsSent**
</dt> <dd>

Nombre total de paquets dirigés envoyés par la station.

</dd> <dt>

**TotalBroadcastPacketsSent**
</dt> <dd>

Nombre total de paquets dirigés par diffusion (adresse MAC FF FF FF FF FF FF) envoyés par la station.

</dd> <dt>

**TotalMulticastPacketsSent**
</dt> <dd>

Nombre total de paquets de multidiffusion (bit de groupe défini dans l’adresse de destination) envoyés par la station.

</dd> <dt>

**TotalBytesReceived**
</dt> <dd>

Nombre total d’octets envoyés à la station.

</dd> <dt>

**TotalBytesSent**
</dt> <dd>

Nombre total d’octets envoyés par la station.

</dd> </dl>

## <a name="remarks"></a>Notes

Moniteur réseau stocke les informations de session et de station dans deux tableaux associés. dont les éléments sont respectivement des structures [SESSIONSTATS](sessionstats.md) et **STATIONSTATS** . Les membres de ces structures peuvent être utilisés pour naviguer entre eux. Par exemple, pour passer à la station suivante, utilisez **NextStationStats**. Pour accéder à la liste des partenaires de session dans le tableau SESSIONSTATS, utilisez l’index fourni dans **SessionPartnerList**.

> [!Note]  
> Le tableau **STATIONSTATS** contient un élément pour chaque station utilisée pendant la capture actuelle. L’algorithme Moniteur réseau utilise pour ajouter des éléments à ce tableau est basé sur la méthode la plus efficace pour enregistrer des informations lorsque la capture est en cours. Par conséquent, la station suivante n’est pas toujours l’élément suivant dans le tableau.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 




