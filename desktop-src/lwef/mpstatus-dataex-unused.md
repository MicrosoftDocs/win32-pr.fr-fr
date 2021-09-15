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
ms.openlocfilehash: bfcbc987a97a8cc47501a24e633c5da2d776a42d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413083"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





