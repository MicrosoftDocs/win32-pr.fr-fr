---
title: Message STM_SETICON (winuser. h)
description: Une application envoie le \_ message STM SETICON pour associer une icône à un contrôle Icon.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff1cbaa6a1083751b3619392fbb0d3b60695e829907c2dfe27fdb41170e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281419"
---
# <a name="stm_seticon-message"></a>\_Message SETICON STM

Une application envoie le message **STM \_ SETICON** pour associer une icône à un contrôle Icon.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de l’icône à associer au contrôle Icon.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un handle de l’icône précédemment associée au contrôle Icon, ou zéro si une erreur se produit.

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

[**\_GETICON STM**](stm-geticon.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**LoadIcon**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

