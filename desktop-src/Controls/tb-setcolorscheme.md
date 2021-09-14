---
title: Message TB_SETCOLORSCHEME (commctrl. h)
description: Définit les informations de jeu de couleurs pour le contrôle ToolBar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116586"
---
# <a name="tb_setcolorscheme-message"></a>TO \_ SETCOLORSCHEME message

Définit les informations de jeu de couleurs pour le contrôle ToolBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) qui contient les informations sur le modèle de couleurs.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Notes

Le contrôle ToolBar utilise les informations de jeu de couleurs lors du dessin des éléments 3D dans le contrôle.

Lorsque les styles visuels sont activés, ce message n’a aucun effet.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





