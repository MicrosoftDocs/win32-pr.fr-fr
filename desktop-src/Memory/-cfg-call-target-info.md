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
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094234"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Ntmmapi. h</dt> </dl> |



 

 




