---
title: Masque du stylet
description: Valeurs qui peuvent apparaître dans le champ penMask de la structure POINTER_PEN_INFO.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bd181b5eafbe1cf6de56c95886deb04e5bd6d2b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519961"
---
# <a name="pen-mask"></a>Masque du stylet

Valeurs qui peuvent apparaître dans le champ **penMask** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Par défaut. Aucun des champs facultatifs n’est valide.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



la **pression** de la structure de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) est valide.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



la **rotation** de la structure de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) est valide.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X** 
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



**tiltX** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) est valide.


</dt> </dl> </dd> <dt>

<span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



l' **inclinaison** de la structure de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) est valide.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





