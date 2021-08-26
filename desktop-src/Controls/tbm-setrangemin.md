---
title: Message TBM_SETRANGEMIN (commctrl. h)
description: Définit la position logique minimale du curseur dans un TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35cbb162b42636d886cb5e41eb9ba6de1a2101a8327ff8ddffbc71c57fa6735
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046069"
---
# <a name="tbm_setrangemin-message"></a>\_Message TBM SETRANGEMIN

Définit la position logique minimale du curseur dans un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur de redessin. Si ce paramètre a la **valeur true**, le message redessine le TrackBar une fois la plage définie. Si ce paramètre a la **valeur false**, le message définit la plage mais ne redessine pas le TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Position minimale du curseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Si la position actuelle du curseur est inférieure à la nouvelle valeur minimale, le message **TBM \_ SETRANGEMIN** définit la position du curseur sur la nouvelle valeur minimale.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TBM \_ SEtrange**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





