---
title: Structure MPCOMPONENT_STATUS (MpClient. h)
description: Informations sur l’état du composant.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPCOMPONENT_STATUS
- PMPCOMPONENT_STATUS des fonctionnalités d’environnement Windows héritées du pointeur de structure
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
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741021"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





