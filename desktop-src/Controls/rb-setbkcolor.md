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
ms.openlocfilehash: 8a2fb502558b53603b59cf7f140248a72f1bf3e22366a85a6e8f740066775fb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696599"
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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur d’arrière-plan par défaut précédente.

## <a name="remarks"></a>Remarques

La couleur d’arrière-plan par défaut du contrôle rebar est utilisée pour dessiner l’arrière-plan dans un contrôle rebar et toutes les bandes ajoutées après l’envoi de ce message. La couleur d’arrière-plan par défaut pour une bande particulière peut être remplacée lorsqu’une bande est ajoutée ou modifiée en définissant l' \_ indicateur de couleurs RBBIM dans **fmask** et en définissant **ClrBack** dans la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

Lorsque les styles visuels sont activés, ce message n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETBKCOLOR RB**](rb-getbkcolor.md)
</dt> </dl>

 

