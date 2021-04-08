---
title: Message LB_RESETCONTENT (winuser. h)
description: Supprime tous les éléments d’une zone de liste.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- LB_RESETCONTENT les contrôles de message Windows
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
ms.openlocfilehash: c0091871df045812dcaa7a159cc456a1350d20f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844121"
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

## <a name="remarks"></a>Notes

Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , le propriétaire de la zone de liste reçoit un message [**WM \_ DELETEITEM**](wm-deleteitem.md) pour chaque élément de la zone de liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





