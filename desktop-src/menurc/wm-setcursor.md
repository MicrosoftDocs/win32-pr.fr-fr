---
title: Message WM_SETCURSOR (winuser. h)
description: Envoyé à une fenêtre si la souris provoque le déplacement du curseur dans une fenêtre et que l’entrée de la souris n’est pas capturée.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032948"
---
# <a name="wm_setcursor-message"></a>\_Message WM SETCURSOR

Envoyé à une fenêtre si la souris provoque le déplacement du curseur dans une fenêtre et que l’entrée de la souris n’est pas capturée.


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre qui contient le curseur.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible de *lParam* spécifie le résultat du test de positionnement pour la position du curseur. Consultez les valeurs de retour de [WM_NCHITTEST](../inputdev/wm-nchittest.md) pour connaître les valeurs possibles.

Le mot de poids fort de *lParam* spécifie le message de fenêtre de la souris qui a déclenché cet événement, par exemple [WM_MOUSEMOVE](../inputdev/wm-mousemove.md). Quand la fenêtre passe en mode de menu, cette valeur est égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la **valeur true** pour arrêter le traitement ou **false** pour continuer.

## <a name="remarks"></a>Notes

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) transmet le message **WM \_ SETCURSOR** à une fenêtre parente avant le traitement. Si la fenêtre parente retourne la **valeur true**, le traitement supplémentaire est interrompu. Le fait de passer le message à la fenêtre parente d’une fenêtre donne le contrôle de fenêtre parente sur le paramètre du curseur dans une fenêtre enfant. La fonction **DefWindowProc** utilise également ce message pour définir le curseur sur une flèche si elle ne se trouve pas dans la zone cliente ou sur le curseur de classe inscrit s’il se trouve dans la zone cliente. Si le mot de poids faible du paramètre *lParam* est **HTERROR** et que le mot de poids fort de *lParam* spécifie que l’un des boutons de la souris est enfoncé, **DefWindowProc** appelle la fonction [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Curseurs](cursors.md)
</dt> </dl>

 

