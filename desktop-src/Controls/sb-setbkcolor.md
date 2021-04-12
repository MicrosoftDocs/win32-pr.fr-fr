---
title: Message SB_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan dans une barre d’État.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385064"
---
# <a name="sb_setbkcolor-message"></a>\_Message SB SETBKCOLOR

Définit la couleur d’arrière-plan dans une barre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui spécifie la nouvelle couleur d’arrière-plan. Spécifiez la \_ valeur CLR par défaut pour faire en sorte que la barre d’État utilise sa couleur d’arrière-plan par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la couleur d’arrière-plan précédente ou la \_ valeur CLR par défaut si la couleur d’arrière-plan est la couleur par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

