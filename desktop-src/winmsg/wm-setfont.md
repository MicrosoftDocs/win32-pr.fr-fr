---
description: Définit la police qu’un contrôle doit utiliser pour dessiner du texte.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Message WM_SETFONT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811bee30237a64955197588f87866d4a64af89edc640762ec16333839aee9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199935"
---
# <a name="wm_setfont-message"></a>\_Message WM SetFont

Définit la police qu’un contrôle doit utiliser pour dessiner du texte.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la police (**Hfont**). Si ce paramètre a la **valeur null**, le contrôle utilise la police système par défaut pour dessiner du texte.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible de *lParam* spécifie si le contrôle doit être redessiné immédiatement lors de la définition de la police. Si ce paramètre a la **valeur true**, le contrôle se redessine lui-même.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le message **WM \_ SetFont** s’applique à tous les contrôles, pas seulement à ceux des boîtes de dialogue.

Le meilleur moment pour le propriétaire d’un contrôle de boîte de dialogue de définir la police du contrôle est lorsqu’il reçoit le message [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) . L’application doit appeler la fonction [**SupprimerObjet**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) pour supprimer la police lorsqu’elle n’est plus nécessaire. par exemple, après avoir détruit le contrôle.

La taille du contrôle ne change pas suite à la réception de ce message. Pour éviter le découpage du texte qui ne tient pas dans les limites du contrôle, l’application doit corriger la taille de la fenêtre de contrôle avant de définir la police.

Quand une boîte de dialogue utilise le style [DS \_ SetFont](../dlgbox/about-dialog-boxes.md) pour définir le texte dans ses contrôles, le système envoie le message **WM \_ SetFont** à la procédure de boîte de dialogue avant de créer les contrôles. Une application peut créer une boîte de dialogue qui contient le \_ style DS SetFont en appelant l’une des fonctions suivantes :

-   [**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATE**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**MAKELPARAM**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM \_ GETFONT**](wm-getfont.md)
</dt> <dt>

[**\_INITDIALOG WM**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
