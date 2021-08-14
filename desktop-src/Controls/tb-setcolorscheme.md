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
ms.openlocfilehash: 58c6a07c186fd3f5a521719ba0f75f8e468c3868d8ebfaa0595679d48b45089f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167499"
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

## <a name="remarks"></a>Remarques

Le contrôle ToolBar utilise les informations de jeu de couleurs lors du dessin des éléments 3D dans le contrôle.

Lorsque les styles visuels sont activés, ce message n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ GETCOLORSCHEME**](tb-getcolorscheme.md)
</dt> </dl>

 

 





