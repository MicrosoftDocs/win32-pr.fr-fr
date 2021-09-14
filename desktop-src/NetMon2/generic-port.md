---
description: Contient un numéro de port utilisé pour les protocoles IP ou IPX.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: GENERIC_PORT Union (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121438"
---
# <a name="generic_port-union"></a>\_Union de port générique

La structure du **\_ port générique** contient un numéro de port utilisé pour les protocoles IP ou IPX.

## <a name="syntax"></a>Syntaxe


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a>Membres

<dl> <dt>

**IPPort**
</dt> <dd>

Numéro de port IP rempli.

</dd> <dt>

**ByteSwappedIPXPort**
</dt> <dd>

Numéro de port IPX rempli.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




