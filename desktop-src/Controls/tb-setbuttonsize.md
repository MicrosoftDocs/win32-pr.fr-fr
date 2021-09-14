---
title: Message TB_SETBUTTONSIZE (commctrl. h)
description: Définit la taille des boutons sur une barre d’outils.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116598"
---
# <a name="tb_setbuttonsize-message"></a>TO \_ SETBUTTONSIZE message

Définit la taille des boutons sur une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la largeur, en pixels, des boutons. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la hauteur, en pixels, des boutons.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

**To \_ SETBUTTONSIZE** doit généralement être appelé après l’ajout de boutons.

Utilisez [**to \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) pour définir les largeurs maximales et minimales autorisées pour les boutons avant leur ajout. Utilisez **to \_ SETBUTTONSIZE** pour définir la taille réelle des boutons.

## <a name="examples"></a>Exemples

L’exemple de code suivant définit la largeur des boutons sur 80 pixels et la hauteur sur 30 pixels.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

