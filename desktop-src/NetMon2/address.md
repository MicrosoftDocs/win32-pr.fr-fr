---
description: Est obsolète et ne doit pas être utilisé.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Structure d’adresse (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 899d68cb4d041c032ce17ac82866488dfd443071e5368d4ba87950de66a32ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796531"
---
# <a name="address-structure"></a>Structure d’adresse

La structure d' **adresse** est obsolète et ne doit pas être utilisée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Type d'adresse. Il peut s'agir de l'une des valeurs suivantes :

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**MACAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse MAC brute.

</dd> <dt>

**IPAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse IP brute.

</dd> <dt>

**IPXRawAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse IPX brute.

</dd> <dt>

**IPXAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une valeur d’adresse IPX décodée.

</dd> <dt>

**VinesIPRawAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse IP de vignes brutes.

</dd> <dt>

**VinesIPAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse IP décodée Vines.

</dd> <dt>

**EthernetSrcAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse source Ethernet.

</dd> <dt>

**EthernetDstAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse de destination Ethernet.

</dd> <dt>

**TokenringSrcAddress**
</dt> <dd>

Vue des données sous la forme d’une adresse source Token Ring.

</dd> <dt>

**TokenringDstAddress**
</dt> <dd>

Vue des données sous la forme d’une adresse de destination Token Ring.

</dd> <dt>

**FddiSrcAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse source FDDI.

</dd> <dt>

**FddiDstAddress**
</dt> <dd>

Vue des données exprimées sous la forme d’une adresse de destination FDDI.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Ensemble d’indicateurs qui modifient les propriétés d’adresse.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




