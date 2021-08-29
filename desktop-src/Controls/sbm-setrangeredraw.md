---
title: Message SBM_SETRANGEREDRAW (winuser. h)
description: Une application envoie le \_ message SBM SETRANGEREDRAW à un contrôle de barre de défilement pour définir les valeurs de position minimale et maximale et pour redessiner le contrôle.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- SBM_SETRANGEREDRAW les contrôles de Windows de message
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
ms.openlocfilehash: 70da860ac52e34a32ca72ae5c3cff36fe4a23feb7b0c78bdeac0294ff7d20df3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078513"
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

## <a name="remarks"></a>Remarques

Les valeurs par défaut de la position minimale et maximale sont égales à zéro. La différence entre les valeurs spécifiées par les paramètres *wParam* et *lParam* ne doit pas être supérieure à MAXLONG.

Si les valeurs de position minimale et maximale sont égales, le contrôle de barre de défilement est masqué et, en fait, désactivé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
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

 

 





