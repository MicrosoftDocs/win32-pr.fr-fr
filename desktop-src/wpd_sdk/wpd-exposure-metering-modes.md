---
description: Le \_ \_ \_ type d’énumération des modes d’exposition wpd permet de décrire le mode de contrôle à utiliser lors de l’estimation de l’exposition pour la capture d’image continue par un appareil.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Énumération WPD_EXPOSURE_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195820"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>\_ \_ Énumération des modes de contrôle d’exposition wpd \_

Le type d’énumération des **\_ \_ \_ modes d’exposition wpd** permet de décrire le mode de contrôle à utiliser lors de l’estimation de l’exposition pour la capture d’image continue par un appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**\_mode de contrôle d’exposition wpd \_ \_ \_ non défini**
</dt> <dd>

Le mode de contrôle n’est pas défini.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_moyenne du \_ mode de contrôle d’exposition wpd \_ \_**
</dt> <dd>

Utilisez l’exposition moyenne sur l’intégralité de l’image.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**Centre du mode de contrôle d’exposition WPD- \_ \_ \_ \_ \_ moyenne pondérée \_**
</dt> <dd>

Utilisez une exposition moyenne, le centre de l’image étant donné un poids plus grand.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**MODE de contrôle d’exposition WPD à \_ \_ \_ \_ plusieurs \_ points**
</dt> <dd>

Utilisez une technique de calcul de la moyenne sur plusieurs points.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**point \_ \_ central du mode de contrôle d’exposition wpd \_ \_ \_**
</dt> <dd>

Utilisez une technique de la moyenne à la place.

</dd> </dl>

## <a name="remarks"></a>Notes

Indique le mode de mesure de l’appareil. Cette énumération est utilisée par la propriété du mode de mesure de l’exposition de l' [ \_ \_ image \_ \_ \_ wpd continue](still-image-properties.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




