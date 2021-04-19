---
description: Le \_ \_ \_ type d’énumération des modes de contrôle de focus wpd décrit comment un appareil doit déterminer quelle partie d’un cadre utiliser pour définir le focus.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Énumération WPD_FOCUS_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525284"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>\_ \_ Énumération des modes de contrôle de focus wpd \_

Le type d’énumération des **\_ modes de \_ contrôle \_ de focus wpd** décrit comment un appareil doit déterminer quelle partie d’un cadre utiliser pour définir le focus.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_mode de contrôle de focus wpd \_ \_ \_ non défini**
</dt> <dd>

Indique qu’aucun mode de focus n’a été spécifié.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_point \_ central du mode de contrôle du focus wpd \_ \_ \_**
</dt> <dd>

Se concentre sur le centre de la zone de trame.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**\_mode de contrôle du focus wpd \_ \_ \_ \_ sur plusieurs points**
</dt> <dd>

Déterminez le focus en analysant plusieurs parties de la zone encadrée.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est spécifiée par la propriété du mode de contrôle de focus de l' [ \_ \_ image \_ \_ \_ wpd continue](still-image-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




