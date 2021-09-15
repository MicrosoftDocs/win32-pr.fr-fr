---
title: Structure MPNIS_PRIVATE_DATA (MpClient. h)
description: Notifications NIS privées.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPNIS_PRIVATE_DATA
- PMPNIS_PRIVATE_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523733"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





