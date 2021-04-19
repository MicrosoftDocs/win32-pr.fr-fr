---
title: Structure MPHEALTH_DATA (MpClient. h)
description: Données de notification d’intégrité.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPHEALTH_DATA
- PMPHEALTH_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106539016"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





