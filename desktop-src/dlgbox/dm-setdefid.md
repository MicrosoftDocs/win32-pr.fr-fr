---
title: Message DM_SETDEFID (winuser. h)
description: Modifie l’identificateur du bouton de commande par défaut d’une boîte de dialogue.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- Boîtes de dialogue de DM_SETDEFID message
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192004"
---
# <a name="dm_setdefid-message"></a>\_Message SETDEFID DM

Modifie l’identificateur du bouton de commande par défaut d’une boîte de dialogue.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur d’un contrôle de bouton de commande qui devient la valeur par défaut.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est toujours **true**.

## <a name="remarks"></a>Notes

Ce message est traité par la fonction [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) . Pour définir le bouton de commande par défaut, la fonction peut envoyer des messages [**WM \_ GETDLGCODE**](wm-getdlgcode.md) et [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) au contrôle spécifié et au bouton de commande par défaut actuel.

L’utilisation du message **DM \_ SETDEFID** peut entraîner l’affichage de plusieurs boutons avec l’état de bouton de commande par défaut. Quand le système affiche une boîte de dialogue, il dessine le premier bouton de commande dans le modèle de boîte de dialogue avec la bordure d’État par défaut. L’envoi d’un message **DM \_ SETDEFID** pour modifier le bouton par défaut ne supprimera pas toujours la bordure d’État par défaut du premier bouton de commande. Dans ce cas, l’application doit envoyer un message [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) pour modifier le premier style de bordure du bouton de commande.

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

[**DM \_ GETDEFID**](dm-getdefid.md)
</dt> <dt>

[**\_GETDLGCODE WM**](wm-getdlgcode.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**BM \_ SETSTYLE**](../controls/bm-setstyle.md)
</dt> <dt>

[**\_SETLIMITTEXT em**](../controls/em-setlimittext.md)
</dt> </dl>

 

