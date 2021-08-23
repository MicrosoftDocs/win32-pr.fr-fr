---
title: Message RB_SETTEXTCOLOR (commctrl. h)
description: Définit la couleur de texte par défaut d’un contrôle rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88458f5a131250dbb261040bf26689356c1ba5446db854839ded05ff287a14ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078613"
---
# <a name="rb_settextcolor-message"></a>\_Message SETTEXTCOLOR RB

Définit la couleur de texte par défaut d’un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la nouvelle couleur de texte par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur de texte par défaut précédente.

## <a name="remarks"></a>Remarques

La couleur de texte par défaut du contrôle rebar est utilisée pour dessiner le texte dans un contrôle rebar et toutes les bandes ajoutées après l’envoi de ce message. La couleur de texte par défaut pour une bande particulière peut être remplacée lorsqu’une bande est ajoutée ou modifiée en définissant l' \_ indicateur de couleurs RBBIM dans **fmask** et en définissant **ClrBack** dans la structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTEXTCOLOR RB**](rb-gettextcolor.md)
</dt> </dl>

 

