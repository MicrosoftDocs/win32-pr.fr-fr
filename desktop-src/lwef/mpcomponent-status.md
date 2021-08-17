---
title: Structure MPCOMPONENT_STATUS (MpClient. h)
description: Informations sur l’état du composant.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPCOMPONENT_STATUS
- PMPCOMPONENT_STATUS des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb12a0358cf4d0112ca1cb8dfedc90c7c3aec504578685e78291dbe5e006cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747797"
---
# <a name="mpcomponent_status-structure"></a>\_Structure d’État MPCOMPONENT

Informations sur l’état du composant.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a>Membres

<dl> <dt>

**fEnable**
</dt> <dd>

Type : **bool**

</dd> <dd>

État du composant.

</dd> <dt>

**Signé**
</dt> <dd>

Type : **HRESULT**

</dd> <dd>

Code de réussite ou d’échec associé à l’État.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





