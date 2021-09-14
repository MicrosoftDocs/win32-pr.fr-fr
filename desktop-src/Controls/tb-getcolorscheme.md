---
title: Message TB_GETCOLORSCHEME (commctrl. h)
description: Récupère les informations de modèle de couleur à partir du contrôle ToolBar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- TB_GETCOLORSCHEME les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116786"
---
# <a name="tb_getcolorscheme-message"></a>TO \_ GETCOLORSCHEME message

Récupère les informations de modèle de couleur à partir du contrôle ToolBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) qui recevra les informations de modèle de couleurs. Vous devez définir le membre **cbSize** de cette structure sur **sizeof**(COLORSCHEME) avant d’envoyer ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ SETCOLORSCHEME**](tb-setcolorscheme.md)
</dt> </dl>

 

 





