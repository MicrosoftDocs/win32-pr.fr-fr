---
title: Message LB_RESETCONTENT (winuser. h)
description: Supprime tous les éléments d’une zone de liste.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- LB_RESETCONTENT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c896263cd4a695583bda299b0feeff552a05ef2c938b9df348da685821c46652
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085369"
---
# <a name="lb_resetcontent-message"></a>\_Message RESETCONTENT lb

Supprime tous les éléments d’une zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , le propriétaire de la zone de liste reçoit un message [**WM \_ DELETEITEM**](wm-deleteitem.md) pour chaque élément de la zone de liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





