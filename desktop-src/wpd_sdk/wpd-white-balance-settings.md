---
description: Le \_ \_ \_ type d’énumération des paramètres de l’équilibre blanc wpd indique comment un appareil vidéo ou d’image poids des canaux de couleur pour obtenir une balance des blancs appropriée.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Énumération WPD_WHITE_BALANCE_SETTINGS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1b596dd6d8fbcc2b2a875b70d80e8eb4040c966590642a004c551ec159c9f5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842046"
---
# <a name="wpd_white_balance_settings-enumeration"></a>\_ \_ Énumération des paramètres de l’équilibre blanc wpd \_

Le type d’énumération des paramètres de l' **\_ \_ équilibre \_ blanc wpd** indique comment un appareil vidéo ou d’image poids des canaux de couleur pour obtenir une balance des blancs appropriée.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_équilibre blanc \_ wpd \_ non défini**
</dt> <dd>

Cette valeur n’a pas été définie.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_Manuel d' \_ équilibre des blancs wpd \_**
</dt> <dd>

L’équilibre des blancs est défini explicitement à l’aide de la propriété d' [ \_ obtention d’image wpd continue \_ image \_ RGB \_ ](still-image-properties.md) et ne change pas par lui-même.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_équilibrer les blancs wpd \_ \_ automatique**
</dt> <dd>

L’appareil définit l’équilibre des blancs.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**\_équilibrer les blancs wpd sur \_ \_ un \_ Push \_ automatique**
</dt> <dd>

L’appareil définit l’équilibre des blancs, mais uniquement lorsque l’utilisateur pousse le bouton de capture de l’appareil tout en le recherchant dans un champ blanc.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**heure d’été de l' \_ équilibre blanc wpd \_ \_**
</dt> <dd>

L’appareil utilise les nombres d’équilibres blancs appropriés pour une utilisation dans la plupart des paramètres d’heure d’été.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**espace blanc de l’WPD \_ \_ \_**
</dt> <dd>

L’appareil utilise des chiffres de balance blancs appropriés pour une utilisation dans la plupart des paramètres d’éclairage lumineux.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**\_Flash d' \_ équilibre des blancs wpd \_**
</dt> <dd>

L’appareil utilise des nombres d’équilibres blancs appropriés pour une utilisation avec un flash.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est utilisée par la propriété de l' [ \_ \_ \_ \_ équilibreur d’image de l’image wpd](still-image-properties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




