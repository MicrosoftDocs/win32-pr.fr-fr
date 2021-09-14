---
description: La structure d' \_ adresse IP Vines \_ est une adresse IP sur un réseau Vines.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Structure de VINES_IP_ADDRESS (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194496"
---
# <a name="vines_ip_address-structure"></a>Structure d' \_ adresse IP Vines \_

La structure d' **\_ \_ adresse IP Vines** est une adresse IP sur un réseau Vines.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>Membres

<dl> <dt>

**NetID**
</dt> <dd>

Identificateur d’un ordinateur spécifique sur un sous-réseau spécifique.

</dd> <dt>

**SubnetID**
</dt> <dd>

Identificateur d’un sous-réseau spécifique sur l’ensemble du réseau.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




