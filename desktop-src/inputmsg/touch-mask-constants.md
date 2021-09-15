---
title: Masque tactile
description: Valeurs qui peuvent apparaître dans le champ touchMask de la structure POINTER_TOUCH_INFO.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519937"
---
# <a name="touch-mask"></a>Masque tactile

Valeurs qui peuvent apparaître dans le champ **touchMask** de la structure [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .

<dl> <dt>

<span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE** 
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Par défaut. Aucun des champs facultatifs n’est valide.


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



**rcContact** de la structure [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) est valide.


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



l' **orientation** de la structure de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) est valide.


</dt> </dl> </dd> <dt>

<span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



la **pression** de la structure de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) est valide.


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

 

 





