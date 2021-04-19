---
description: Le \_ type d' \_ énumération des sources d’alimentation wpd décrit la source d’alimentation utilisée par un appareil.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Énumération WPD_POWER_SOURCES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542260"
---
# <a name="wpd_power_sources-enumeration"></a>\_Énumération des sources d’alimentation wpd \_

Le type d’énumération des **\_ \_ sources d’alimentation wpd** décrit la source d’alimentation utilisée par un appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_batterie de \_ source d’alimentation wpd \_**
</dt> <dd>

La source d’alimentation de l’appareil est une batterie.

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**\_source d’alimentation wpd \_ \_ externe**
</dt> <dd>

L’appareil utilise une source d’alimentation externe.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée par la propriété de la [ \_ \_ \_ source d’alimentation de l’appareil wpd](device-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




