---
title: Structure MPTHREAT_INFOEX_NIS (MpClient. h)
description: Contient des informations spécifiques à NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_INFOEX_NIS
- PMPTHREAT_INFOEX_NIS des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8320070f80000ec5c2b235a815dc075f96f82ddd3c6d56c4022b9d60759c3e44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746898"
---
# <a name="mpthreat_infoex_nis-structure"></a>\_Structure MPTHREAT INFOEX \_ NIS

Contient des informations spécifiques à NIS.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a>Membres

<dl> <dt>

**SourceIP**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd></dd> <dt>

**DestinationIP**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd></dd> <dt>

**dwSourceport**
</dt> <dd>

Type : **DWORD**

</dd> <dd></dd> <dt>

**dwDestinationport**
</dt> <dd>

Type : **DWORD**

</dd> <dd></dd> <dt>

**Protocole**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd></dd> <dt>

**Lien**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





