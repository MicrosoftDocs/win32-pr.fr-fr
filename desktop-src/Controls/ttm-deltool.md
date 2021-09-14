---
title: Message TTM_DELTOOL (commctrl. h)
description: Supprime un outil d’un contrôle ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- TTM_DELTOOL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115886"
---
# <a name="ttm_deltool-message"></a>\_Message atténuation DELTOOL

Supprime un outil d’un contrôle ToolTip.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Les membres **HWND** et **UID** identifient l’outil à supprimer, tandis que le membre **cbSize** doit spécifier la taille de la structure. Tous les autres membres sont ignorés.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ DELTOOLW** (Unicode) et **atténuation \_ DELTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**ATTÉNUATION \_ ADDTOOL**](ttm-addtool.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[À propos des contrôles ToolTip](tooltip-controls.md)
</dt> </dl>

 

 





