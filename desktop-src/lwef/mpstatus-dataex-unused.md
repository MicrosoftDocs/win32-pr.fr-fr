---
title: Structure MPSTATUS_DATAEX_UNUSED (MpClient. h)
description: Structure factice pour non-SRP.
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPSTATUS_DATAEX_UNUSED
- PMPSTATUS_DATAEX_UNUSED des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245315d12b5fbe76ec2f552e510336aa3974753678e04f87c33546737f180c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961089"
---
# <a name="mpstatus_dataex_unused-structure"></a>MPSTATUS \_ DATAEX, \_ structure inutilisée

Structure factice pour non-SRP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwNone**
</dt> <dd>

Type : **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





