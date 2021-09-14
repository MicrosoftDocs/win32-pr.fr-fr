---
description: Le \_ \_ type d’énumération de modes de focus wpd décrit le mode Focus utilisé par un appareil de capture d’image continue.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Énumération WPD_FOCUS_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219332"
---
# <a name="wpd_focus_modes-enumeration"></a>\_Énumération des modes de focus wpd \_

Le type d’énumération de **\_ \_ modes de focus wpd** décrit le mode Focus utilisé par un appareil de capture d’image continue.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**\_focus wpd \_ non défini**
</dt> <dd>

Le mode focus n’a pas été spécifié.

</dd> <dt>

<span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**\_Manuel de focus wpd \_**
</dt> <dd>

Spécifie le focus manuel.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**\_focus wpd \_ automatique**
</dt> <dd>

Spécifie le focus automatique, contrôlé par l’appareil.

</dd> <dt>

<span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_ \_ macro automatique Focus \_ wpd**
</dt> <dd>

Spécifie que l’appareil doit basculer automatiquement entre la macro et le focus normal, selon les besoins.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée par la propriété de [ \_ \_ \_ \_ mode focus d’image toujours wpd](still-image-properties.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




