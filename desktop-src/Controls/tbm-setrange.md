---
title: Message TBM_SETRANGE (commctrl. h)
description: Définit la plage de positions logiques minimale et maximale pour le curseur dans un TrackBar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032611"
---
# <a name="tbm_setrange-message"></a>\_Message TBM SEtrange

Définit la plage de positions logiques minimale et maximale pour le curseur dans un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur de redessin. Si ce paramètre a la **valeur true**, le TrackBar est redessiné après la définition de la plage. Si ce paramètre a la **valeur false**, le message définit la plage mais ne redessine pas le TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la position minimale du curseur, tandis que le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position maximale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Si la position actuelle du curseur est en dehors de la nouvelle plage, le message **TBM \_ SetRange** définit la position du curseur sur la nouvelle valeur maximale ou minimale.

Étant donné que ce message prend des valeurs entières non signées 2 16 bits, la plage maximale que ce message peut spécifier est comprise entre 0 et 65 535. Pour spécifier des valeurs de plage plus grandes, utilisez les messages [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md) et [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

