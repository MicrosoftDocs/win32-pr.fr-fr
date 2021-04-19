---
description: Le \_ \_ type d’énumération types de messages SMS décrit le type de contenu d’un message SMS (Short Message Service).
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Énumération SMS_MESSAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530468"
---
# <a name="sms_message_types-enumeration"></a>\_Énumération des types de messages SMS \_

Le type d’énumération **\_ \_ types de messages SMS** décrit le type de contenu d’un message SMS (Short Message Service).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS \_ SMS \_**
</dt> <dd>

Message texte.

</dd> <dt>

<span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS \_ - \_ message binaire**
</dt> <dd>

Message binaire.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée par la commande [**wpd \_ \_ SMS \_ Send**](wpd-command-sms-send-command.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




