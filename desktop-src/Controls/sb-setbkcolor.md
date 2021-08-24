---
title: Message SB_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan dans une barre d’État.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR les contrôles de Windows de message
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
ms.openlocfilehash: b97893d49d475789b07c28e17e88097aa4df4336154d6b4e0f9c4fa081e52635
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637079"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

