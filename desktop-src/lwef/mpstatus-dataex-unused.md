---
title: Structure MPSTATUS_DATAEX_UNUSED (MpClient. h)
description: Structure factice pour non-SRP.
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSTATUS_DATAEX_UNUSED
- PMPSTATUS_DATAEX_UNUSED des fonctionnalités d’environnement Windows héritées du pointeur de structure
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
ms.openlocfilehash: bfcbc987a97a8cc47501a24e633c5da2d776a42d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106294"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





