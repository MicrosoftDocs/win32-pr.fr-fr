---
description: Le \_ \_ type d’énumération des modes de programme d’exposition wpd \_ décrit un mode d’exposition à utiliser lors de la capture d’images avec un appareil.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Énumération WPD_EXPOSURE_PROGRAM_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545514"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>\_ \_ Énumération des modes du programme d’exposition wpd \_

Le type d’énumération des **\_ modes de \_ programme \_ d’exposition wpd** décrit un mode d’exposition à utiliser lors de la capture d’images avec un appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_mode de programme d’exposition wpd \_ \_ \_ non défini**
</dt> <dd>

Le mode d’exposition n’a pas été spécifié.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_Manuel du \_ mode de programme d’exposition wpd \_ \_**
</dt> <dd>

L’application doit spécifier tous les paramètres d’exposition.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_mode de programme d’exposition wpd \_ \_ \_ automatique**
</dt> <dd>

Utilisez un mode d’exposition automatique défini par l’appareil.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**exposition de l' \_ ouverture du mode de programme d’exposition wpd \_ \_ \_ \_**
</dt> <dd>

Mode d’exposition automatisé qui indique que la valeur de l’ouverture de l’objectif doit rester fixe, mais la vitesse d’obturation doit être déterminée par l’appareil.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_priorité d' \_ obturation du mode de programme d’exposition wpd \_ \_ \_**
</dt> <dd>

Mode d’exposition automatisé qui indique que la vitesse d’obturation doit rester fixe, mais que l’ouverture de l’objectif doit être déterminée par l’appareil.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_ \_ \_ élément créatif du mode de programme exposition wpd \_**
</dt> <dd>

Mode d’exposition automatisé qui tente d’optimiser la profondeur du champ.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_action du \_ mode de programme d’exposition wpd \_ \_**
</dt> <dd>

Mode d’exposition automatisé qui tente d’optimiser la vitesse d’obturation.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**\_mode de \_ programme exposition wpd \_ \_ portrait**
</dt> <dd>

Mode d’exposition automatisé qui spécifie une profondeur relativement faible de champ.

</dd> </dl>

## <a name="remarks"></a>Notes

Indique le mode de programme d’exposition de l’appareil. Cette énumération est utilisée par la propriété du [mode de programme d' \_ \_ exposition d’image \_ \_ \_ toujours wpd](still-image-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




