---
title: Message RB_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan par défaut d’un contrôle rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- RB_SETBKCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117234"
---
# <a name="rb_setbkcolor-message"></a>\_Message SETBKCOLOR RB

Définit la couleur d’arrière-plan par défaut d’un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la nouvelle couleur d’arrière-plan par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan par défaut précédente.

## <a name="remarks"></a>Notes

La couleur d’arrière-plan par défaut du contrôle rebar est utilisée pour dessiner l’arrière-plan dans un contrôle rebar et toutes les bandes ajoutées après l’envoi de ce message. La couleur d’arrière-plan par défaut pour une bande particulière peut être remplacée lorsqu’une bande est ajoutée ou modifiée en définissant l' \_ indicateur de couleurs RBBIM dans **fmask** et en définissant **ClrBack** dans la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

Lorsque les styles visuels sont activés, ce message n’a aucun effet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETBKCOLOR RB**](rb-getbkcolor.md)
</dt> </dl>

 

