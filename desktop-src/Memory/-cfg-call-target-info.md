---
description: représente des informations sur les cibles d’appel pour Control Flow Guard (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: Structure CFG_CALL_TARGET_INFO (Ntmmapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: e3bd7d351e890a968f2fa01ddffa6c8e3be16164d78393894055f55660c516bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040279"
---
# <a name="cfg_call_target_info-structure"></a>Structure des informations de la \_ cible de l’appel de cfg \_ \_

représente des informations sur les cibles d’appel pour Control Flow Guard (CFG).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Offset**
</dt> <dd>

Décalage par rapport à une adresse virtuelle (de début) fournie. Ce décalage doit être aligné sur 16 octets.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs décrivant l’opération à effectuer sur l’adresse. Si **la \_ cible d’appel cfg \_ \_ valide** est définie, l’adresse est marquée comme valide pour cfg. Dans le cas contraire, elle sera marquée comme une cible d’appel non valide.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Ntmmapi. h</dt> </dl> |



 

 




