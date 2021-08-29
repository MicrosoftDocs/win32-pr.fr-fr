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
ms.openlocfilehash: 353faa17a505742f9e5b31feeb1c0108add7895f8039f12905c399d515bb2bb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910869"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




