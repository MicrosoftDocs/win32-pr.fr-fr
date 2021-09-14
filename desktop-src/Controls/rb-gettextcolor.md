---
title: Message RB_GETTEXTCOLOR (commctrl. h)
description: Récupère la couleur de texte par défaut d’un contrôle rebar.
ms.assetid: fc9c731d-c606-4845-a119-737267301b29
keywords:
- RB_GETTEXTCOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082079808aa553aaada5322cff16742dafa0b994
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117289"
---
# <a name="rb_gettextcolor-message"></a>\_Message GETTEXTCOLOR RB

Récupère la couleur de texte par défaut d’un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur de texte par défaut actuelle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTEXTCOLOR RB**](rb-settextcolor.md)
</dt> </dl>

 

