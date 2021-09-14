---
description: Le \_ \_ \_ type d’énumération des valeurs d’état de rognés wpd décrit l’état de rognage d’une image.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Énumération WPD_CROPPED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225681"
---
# <a name="wpd_cropped_status_values-enumeration"></a>\_ \_ Énumération des valeurs d’État rognées de l’API \_

Le type d’énumération des **\_ valeurs d' \_ état \_ de rognés wpd** décrit l’état de rognage d’une image.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_État du rognage wpd \_ \_ non \_ rogné**
</dt> <dd>

L’image n’a pas été rognée.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**\_État du rognage wpd \_ \_ rogné**
</dt> <dd>

L’image a été rognée.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**l' \_ État du rognage wpd ne \_ \_ doit \_ pas \_ être \_ rogné**
</dt> <dd>

L’image n’a pas été découpée et ne doit pas être rognée.

</dd> </dl>

## <a name="remarks"></a>Notes

Indique l’État rogné d’une image. Cette énumération est utilisée par la propriété de l' [ \_ \_ \_ État rogné de l’image wpd](image-properties.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




