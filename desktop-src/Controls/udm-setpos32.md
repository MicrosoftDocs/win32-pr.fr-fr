---
title: Message UDM_SETPOS32 (commctrl. h)
description: Définit la position d’un contrôle up-up avec une précision de 32 bits.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- UDM_SETPOS32 les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d8dee48c580df72a32bb2072b00cc2dfbdf38b386825d686e8bc8510ba47e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088419"
---
# <a name="udm_setpos32-message"></a>\_Message SETPOS32 UDM

Définit la position d’un contrôle up-up avec une précision de 32 bits.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Variable de type entier qui spécifie la nouvelle position pour le contrôle up-up. Si le paramètre est en dehors de la plage spécifiée du contrôle, *lParam* prend la valeur valide la plus proche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la position précédente.

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

[**\_GETPOS UDM**](udm-getpos.md)
</dt> <dt>

[**\_SetPos UDM**](udm-setpos.md)
</dt> <dt>

[**\_GETPOS32 UDM**](udm-getpos32.md)
</dt> </dl>

 

 





