---
description: le \_ type d' \_ énumération des valeurs de type de stockage WPD \_ décrit les différents types de stockage d’appareil Windows Portable.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Énumération WPD_STORAGE_TYPE_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1aad78833f9e5baa0d3c7da3ab37d39f4159672b85d5c01c54ae8b034c5b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842075"
---
# <a name="wpd_storage_type_values-enumeration"></a>\_ \_ Énumération des valeurs de type de stockage wpd \_

le type d’énumération des **\_ valeurs de \_ type \_ de stockage WPD** décrit les différents types de stockage d’appareil Windows Portable.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**\_type de stockage wpd \_ \_ non défini**
</dt> <dd>

Le stockage est d’un type non défini.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**mémoire \_ \_ fixe du type de stockage wpd \_ \_**
</dt> <dd>

Le stockage est non amovible et en lecture seule.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_type de stockage wpd \_ \_ \_ ROM amovible**
</dt> <dd>

Le stockage est amovible et est en lecture seule.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ RAM fixe de type de stockage wpd \_ \_**
</dt> <dd>

Le stockage est non amovible et prend en charge la lecture/écriture.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_ \_ RAM amovible de type de stockage wpd \_ \_**
</dt> <dd>

Le stockage est amovible et prend en charge la lecture/écriture.

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




