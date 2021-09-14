---
description: La \_ structure d’adresse IPX fournit une adresse au niveau du protocole IPX.
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: Structure de IPX_ADDRESS (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119238"
---
# <a name="ipx_address-structure"></a>\_Structure d’adresse IPX

La structure d' **\_ adresse IPX** fournit une adresse au niveau du protocole IPX.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a>Membres

<dl> <dt>

**Sous-réseau**
</dt> <dd>

Identificateur du sous-réseau du réseau.

</dd> <dt>

**Adresse**
</dt> <dd>

Identificateur de la carte réseau du sous-réseau.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




