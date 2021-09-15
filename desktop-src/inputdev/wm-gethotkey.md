---
title: Message WM_GETHOTKEY (winuser. h)
description: Envoyé pour déterminer la touche d’accès rapide associée à une fenêtre.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- WM_GETHOTKEY l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413120"
---
# <a name="wm_gethotkey-message"></a>\_Message WM GETHOTKEY

Envoyé pour déterminer la touche d’accès rapide associée à une fenêtre.


```C++
#define WM_GETHOTKEY                    0x0033
```



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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est le code de touche virtuelle et les modificateurs de la touche d’accès rapide, ou **null** si aucune touche d’accès rapide n’est associée à la fenêtre. Le code de la touche virtuelle se trouve dans l’octet de poids faible de la valeur de retour et les modificateurs se trouvent dans l’octet de poids fort. Les modificateurs peuvent être une combinaison des indicateurs suivants à partir de CommCtrl. h.



| Code/valeur de retour                                                                                                                                         | Description             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt> </dl>     | touche ALT<br/>      |
| <dl> <dt>**HOTKEYF \_ CONTRÔLE**</dt> <dt>0x02</dt> </dl> | Touche CTRL<br/>     |
| <dl> <dt>**HOTKEYF \_**</dt> <dt>0x08</dt> de l’ext. </dl>     | Clé étendue<br/> |
| <dl> <dt>**HOTKEYF \_ DÉCALAGE**</dt> <dt>0x01</dt> </dl>   | Touche Maj<br/>    |



 

## <a name="remarks"></a>Notes

Ces touches d’accès rapide ne sont pas liées aux touches d’accès rapide définies par la fonction [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**\_SETHOTKEY WM**](wm-sethotkey.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

