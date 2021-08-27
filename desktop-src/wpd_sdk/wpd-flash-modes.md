---
description: Le \_ \_ type d’énumération des modes flash wpd décrit un mode flash à utiliser lors de la capture d’images avec un appareil.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Énumération WPD_FLASH_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72e9b6cb2b52f1d90c584b6f425711769b25ea0c5d44065b5aa377d2811592e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005919"
---
# <a name="wpd_flash_modes-enumeration"></a>\_ \_ Énumération des modes flash wpd

Le type d’énumération des **\_ \_ modes flash wpd** décrit un mode flash à utiliser lors de la capture d’images avec un appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_mode flash \_ wpd \_ non défini**
</dt> <dd>

Aucun mode flash n’a été spécifié.

</dd> <dt>

<span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**\_mode flash \_ wpd \_ automatique**
</dt> <dd>

Spécifie que le flash doit être utilisé en mode automatique, comme spécifié par l’appareil.

</dd> <dt>

<span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_mode flash \_ wpd \_ désactivé**
</dt> <dd>

Spécifie qu’aucun flash ne doit être utilisé.

</dd> <dt>

<span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_remplissage du \_ mode \_ Flash wpd**
</dt> <dd>

Spécifie un flash de type de remplissage.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**\_mode flash wpd- \_ \_ \_ yeux rouges \_ auto**
</dt> <dd>

Spécifie que le flash de réduction des yeux rouges doit être utilisé.

</dd> <dt>

<span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_ \_ couleur rouge du mode flash \_ \_ wpd \_**
</dt> <dd>

Spécifie que le flash de remplissage des yeux rouges doit être utilisé.

</dd> <dt>

<span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ synchronisation externe en mode flash \_ wpd \_**
</dt> <dd>

Spécifie que le flash doit être synchronisé avec d’autres périphériques flash externes.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est utilisée par la propriété du [ \_ \_ \_ \_ mode flash de l’image wpd](still-image-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




