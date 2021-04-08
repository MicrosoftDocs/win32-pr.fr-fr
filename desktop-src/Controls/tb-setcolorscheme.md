---
title: Message TB_SETCOLORSCHEME (commctrl. h)
description: Définit les informations de jeu de couleurs pour le contrôle ToolBar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- TB_SETCOLORSCHEME les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844265"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Notes

Le contrôle ToolBar utilise les informations de jeu de couleurs lors du dessin des éléments 3D dans le contrôle.

Lorsque les styles visuels sont activés, ce message n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





