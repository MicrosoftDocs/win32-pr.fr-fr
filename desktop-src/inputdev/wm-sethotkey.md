---
title: Message WM_SETHOTKEY (winuser. h)
description: Envoyé à une fenêtre pour associer une touche d’accès rapide à la fenêtre. Quand l’utilisateur appuie sur la touche d’accès rapide, le système active la fenêtre.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- WM_SETHOTKEY l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "103761515"
---
# <a name="wm_sethotkey-message"></a>\_Message WM SETHOTKEY

Envoyé à une fenêtre pour associer une touche d’accès rapide à la fenêtre. Quand l’utilisateur appuie sur la touche d’accès rapide, le système active la fenêtre.


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible spécifie le code de la touche virtuelle à associer à la fenêtre.

Le mot de poids fort peut être une ou plusieurs des valeurs suivantes à partir de CommCtrl. h.

Le fait de définir *wParam* sur **null** supprime la touche d’accès rapide associée à une fenêtre.



| Valeur                                                                                                                                                                                                                         | Signification                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt> </dl>             | touche ALT<br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <dt>**HOTKEYF \_ CONTRÔLE**</dt> <dt>0x02</dt> </dl> | Touche CTRL<br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <dt>**HOTKEYF \_**</dt> <dt>0x08</dt> de l’ext. </dl>             | Clé étendue<br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <dt>**HOTKEYF \_ DÉCALAGE**</dt> <dt>0x01</dt> </dl>       | Touche Maj<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’une des suivantes.



| Valeur retournée                                                                  | Description                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>-1</dt> </dl> | La fonction échoue ; la touche d’accès rapide n’est pas valide.<br/>                        |
| <dl> <dt>0</dt> </dl>  | La fonction échoue ; la fenêtre n’est pas valide.<br/>                         |
| <dl> <dt>1</dt> </dl>  | La fonction est réussie et aucune autre fenêtre n’a la même touche d’accès rapide.<br/>        |
| <dl> <dt>2</dt> </dl>  | La fonction réussit, mais une autre fenêtre a déjà la même touche d’accès rapide.<br/> |



 

## <a name="remarks"></a>Notes

Une touche d’accès rapide ne peut pas être associée à une fenêtre enfant.

**VK \_** Les touches d’accès rapide, d' **\_ espace de VK** et de **VK \_** sont des touches d’accès non valides.

Quand l’utilisateur appuie sur la touche d’accès rapide, le système génère un message [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) avec *wParam* égal à **SC \_ Hotkey** et *lParam* égal au handle de la fenêtre. Si ce message est transmis à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), le système affiche la dernière fenêtre active de la fenêtre (si elle existe) ou la fenêtre elle-même (s’il n’y a pas de fenêtre contextuelle) au premier plan.

Une fenêtre ne peut avoir qu’une seule touche d’accès rapide. Si la fenêtre est déjà associée à une touche d’accès rapide, la nouvelle touche d’accès rapide remplace l’ancienne. Si plusieurs fenêtres possèdent la même touche d’accès rapide, la fenêtre qui est activée par la touche d’accès rapide est aléatoire.

Ces touches d’accès rapide ne sont pas liées aux touches d’accès rapide définies par [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**\_GETHOTKEY WM**](wm-gethotkey.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

