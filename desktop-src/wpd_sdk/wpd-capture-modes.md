---
description: Le \_ \_ type d’énumération des modes de capture wpd décrit le mode de temporisation de capture d’une capture d’image continue.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Énumération WPD_CAPTURE_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522856"
---
# <a name="wpd_capture_modes-enumeration"></a>\_Énumération des modes de capture wpd \_

Le type d’énumération des **\_ \_ modes de capture wpd** décrit le mode de temporisation de capture d’une capture d’image continue.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**\_mode de capture wpd \_ \_ non défini**
</dt> <dd>

Le mode de capture n’a pas été défini.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**\_mode de capture wpd \_ \_ normal**
</dt> <dd>

Aucun mode de délai ou de rafale ne doit être utilisé.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**\_ \_ rafale en mode de capture wpd \_**
</dt> <dd>

Spécifie qu’un nombre défini d’images doit être capturé avec un intervalle défini entre eux. Le nombre d’images à capturer et le délai entre elles sont spécifiés par les propriétés de l’intervalle de [ \_ \_ \_ rafales \_ d’images fixes wpd](still-image-properties.md) et de l' [ \_ \_ \_ \_ intervalle de rafales d’images fixes](still-image-properties.md) .

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_mode de capture wpd \_ \_ TIMELAPSE**
</dt> <dd>

La capture d’images doit utiliser la photographie temporelle. Le nombre d’images et l’intervalle entre eux sont décrits par les propriétés de l' [ \_ image wpd toujours \_ image \_ TIMELAPSE \_ Number](still-image-properties.md) et [wpd \_ Still \_ image \_ TIMELAPSE \_ Interval](still-image-properties.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée par la propriété du [ \_ mode de \_ \_ capture \_ d’image](still-image-properties.md) de l’wpd.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




