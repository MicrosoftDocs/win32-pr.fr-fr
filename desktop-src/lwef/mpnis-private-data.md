---
title: Structure MPNIS_PRIVATE_DATA (MpClient. h)
description: Notifications NIS privées.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPNIS_PRIVATE_DATA
- PMPNIS_PRIVATE_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740140"
---
# <a name="mpnis_private_data-structure"></a>\_Structure de \_ données privées MPNIS

Notifications NIS privées.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Type de notification.

</dd> <dt>

**cbDataSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille des données réservées, en octets.

</dd> <dt>

**pbData**
</dt> <dd>

Type : **Byte \***

</dd> <dd>

Pointeur vers les données réservées.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





