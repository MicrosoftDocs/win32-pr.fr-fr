---
description: La structure PROPERTYINSTEX définit une instance de propriété étendue et de forme libre.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: PROPERTYINSTEX, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311901"
---
# <a name="propertyinstex-structure"></a>PROPERTYINSTEX, structure

La structure **PROPERTYINSTEX** définit une instance de propriété étendue et de forme libre.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a>Membres

<dl> <dt>

**Durée**
</dt> <dd>

Longueur des données en octets.

</dd> <dt>

**LengthEx**
</dt> <dd>

Longueur des données étendues.

</dd> <dt>

**lpData**
</dt> <dd>

Pointeur vers les données étendues.

</dd> <dt>

**Byte**
</dt> <dd>

Pointeur vers les données d' **octets** .

</dd> <dt>

**Word**
</dt> <dd>

Pointeur vers les données du **mot** .

</dd> <dt>

**Grande**
</dt> <dd>

Pointeur vers les données **DWORD** .

</dd> <dt>

**LargeInt**
</dt> <dd>

Pointeur vers les données **LARGEINT** .

</dd> <dt>

**SysTime**
</dt> <dd>

Pointeur vers les données **SystemTime** .

</dd> <dt>

**TypedString**
</dt> <dd>

Chaîne typée qui peut avoir des données étendues.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




