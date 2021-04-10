---
title: Message SBM_SETRANGEREDRAW (winuser. h)
description: Une application envoie le \_ message SBM SETRANGEREDRAW à un contrôle de barre de défilement pour définir les valeurs de position minimale et maximale et pour redessiner le contrôle.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- SBM_SETRANGEREDRAW les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032342"
---
# <a name="sbm_setrangeredraw-message"></a>\_Message SBM SETRANGEREDRAW

Une application envoie le message **SBM \_ SETRANGEREDRAW** à un contrôle de barre de défilement pour définir les valeurs de position minimale et maximale et pour redessiner le contrôle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie la position de défilement minimale.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie la position de défilement maximale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**ComCtl32.dll version 5,0**: si la position de la case de défilement a changé, la valeur de retour est la position précédente de la case de défilement ; dans le cas contraire, il est égal à zéro.

**ComCtl32.dll version 6,0**: position actuelle de la case de défilement, qu’elle ait été modifiée ou non.

## <a name="remarks"></a>Notes

Les valeurs par défaut de la position minimale et maximale sont égales à zéro. La différence entre les valeurs spécifiées par les paramètres *wParam* et *lParam* ne doit pas être supérieure à MAXLONG.

Si les valeurs de position minimale et maximale sont égales, le contrôle de barre de défilement est masqué et, en fait, désactivé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETPOS SBM**](sbm-getpos.md)
</dt> <dt>

[**\_GETRANGE SBM**](sbm-getrange.md)
</dt> <dt>

[**\_SetPos SBM**](sbm-setpos.md)
</dt> <dt>

[**\_DÉtrange SBM**](sbm-setrange.md)
</dt> </dl>

 

 





