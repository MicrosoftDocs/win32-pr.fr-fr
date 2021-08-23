---
description: Le \_ type d' \_ énumération des modes d’effet wpd décrit différents effets visuels qui peuvent être appliqués à une image.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Énumération WPD_EFFECT_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8ca712a758d23f70d2a1f8760272b821adeec548a1d719c9564cdc8cf17cdeb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657419"
---
# <a name="wpd_effect_modes-enumeration"></a>\_Énumération des modes d’effet wpd \_

Le type d’énumération des **\_ \_ modes d’effet wpd** décrit différents effets visuels qui peuvent être appliqués à une image.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_mode effet wpd non \_ \_ défini**
</dt> <dd>

Aucun effet n’a été spécifié.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_couleur du \_ mode d’effet wpd \_**
</dt> <dd>

L’image doit être de couleur.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_mode d’effet wpd \_ \_ noir \_ et \_ blanc**
</dt> <dd>

L’image doit être en noir et blanc.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**\_mode effet \_ wpd \_ sépia**
</dt> <dd>

L’image doit être sépia.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est utilisée par la propriété du [ \_ mode d' \_ \_ effet \_ d’image toujours wpd](still-image-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




