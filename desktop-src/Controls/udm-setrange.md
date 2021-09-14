---
title: Message UDM_SETRANGE (commctrl. h)
description: Définit les positions minimale et maximale (plage) pour un contrôle up-up.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115418"
---
# <a name="udm_setrange-message"></a>\_Message UDM SEtrange

Définit les positions minimale et maximale (plage) pour un contrôle up-up.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **short** qui spécifie la position maximale pour le contrôle up-UpDown, et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est un **short** qui spécifie la position minimale. Aucune position ne peut être supérieure à la \_ valeur ud MAXVAL ou inférieure à la \_ valeur ud MINVAL. En outre, la différence entre les deux positions ne peut pas dépasser UD \_ MAXVAL.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

La position maximale peut être inférieure à la position minimale. Le fait de cliquer sur le bouton fléché vers le haut déplace la position actuelle plus près de la position maximale, et le fait de cliquer sur le bouton fléché vers le bas se déplace vers la position minimale.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**e \_ trange UDM**](udm-setrange.md)
</dt> </dl>

 

