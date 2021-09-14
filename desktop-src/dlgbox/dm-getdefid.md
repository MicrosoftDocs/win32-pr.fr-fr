---
title: Message DM_GETDEFID (winuser. h)
description: Récupère l’identificateur du contrôle de bouton de commande par défaut d’une boîte de dialogue.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- Boîtes de dialogue de DM_GETDEFID message
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192012"
---
# <a name="dm_getdefid-message"></a>\_Message GETDEFID DM

Récupère l’identificateur du contrôle de bouton de commande par défaut d’une boîte de dialogue.


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si un bouton de commande par défaut existe, le mot de poids fort de la valeur de retour contient la valeur **DC \_ HASDEFID** et le mot de poids faible contient l’identificateur de contrôle. Sinon, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

La fonction [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) traite ce message.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ SETDEFID**](dm-setdefid.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> </dl>

 

 





