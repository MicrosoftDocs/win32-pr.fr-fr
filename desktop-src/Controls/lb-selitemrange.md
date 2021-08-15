---
title: Message LB_SELITEMRANGE (winuser. h)
description: Sélectionne ou désélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- LB_SELITEMRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a08019f3d60e6c9bfe841067b48220b8fcfe75891c9bcc8db64bf28d219b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958598"
---
# <a name="lb_selitemrange-message"></a>\_Message SELITEMRANGE lb

Sélectionne ou désélectionne un ou plusieurs éléments consécutifs dans une zone de liste à sélection multiple.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**True** pour sélectionner la plage d’éléments, ou **false** pour la désélectionner.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie l’index de base zéro du premier élément à sélectionner. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie l’index de base zéro du dernier élément à sélectionner.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une erreur se produit, la valeur de retour est LB \_ Err.

## <a name="remarks"></a>Remarques

Utilisez ce message uniquement avec les zones de liste à sélection multiple.

Ce message peut sélectionner une plage uniquement dans les 65 536 premiers éléments.

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

[**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)
</dt> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

