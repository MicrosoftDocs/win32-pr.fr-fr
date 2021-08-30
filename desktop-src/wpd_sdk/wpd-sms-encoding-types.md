---
description: Le \_ \_ \_ type d’énumération des types d’encodage SMS wpd décrit le type d’encodage d’un message SMS (Short Message Service).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Énumération WPD_SMS_ENCODING_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 648815f8a82248151b19f5c753bf3e42643d61eb507501d907c5ac54a2b226b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927679"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>\_ \_ Énumération des types d’encodage SMS wpd \_

Le type d’énumération des **\_ \_ \_ types d’encodage SMS wpd** décrit le type d’encodage d’un message SMS (Short Message Service).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**Encodage SMS \_ \_ 7 \_ bits**
</dt> <dd>

Encodage 7 bits.

</dd> <dt>

<span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**Encodage SMS \_ \_ 8 \_ bits**
</dt> <dd>

Encodage 8 bits.

</dd> <dt>

<span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**Encodage SMS \_ \_ UTF \_ 16**
</dt> <dd>

Encodage de 16 bits (UTF).

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est utilisée par la propriété d' [ \_ \_ encodage SMS wpd](sms-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




