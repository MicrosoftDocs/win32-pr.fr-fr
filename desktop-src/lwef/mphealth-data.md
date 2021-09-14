---
title: Structure MPHEALTH_DATA (MpClient. h)
description: Données de notification d’intégrité.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPHEALTH_DATA
- PMPHEALTH_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294175"
---
# <a name="mphealth_data-structure"></a>\_Structure de données MPHEALTH

Données de notification d’intégrité.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Type de notification.

</dd> <dt>

**dwNotificationFlag**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Inutilisé.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





