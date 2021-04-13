---
title: Message RB_GETTEXTCOLOR (commctrl. h)
description: Récupère la couleur de texte par défaut d’un contrôle rebar.
ms.assetid: fc9c731d-c606-4845-a119-737267301b29
keywords:
- RB_GETTEXTCOLOR les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465855"
---
# <a name="rb_gettextcolor-message"></a>\_Message GETTEXTCOLOR RB

Récupère la couleur de texte par défaut d’un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui représente la couleur de texte par défaut actuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTEXTCOLOR RB**](rb-settextcolor.md)
</dt> </dl>

 

