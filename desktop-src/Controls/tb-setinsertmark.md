---
title: Message TB_SETINSERTMARK (commctrl. h)
description: Définit la marque d’insertion actuelle pour la barre d’outils.
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- TB_SETINSERTMARK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19453c2e563d884479b9ca1648127ce997c241f7b7f30fd4bffeef73ec894947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434518"
---
# <a name="tb_setinsertmark-message"></a>TO \_ SETINSERTMARK message

Définit la marque d’insertion actuelle pour la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) qui contient la marque d’insertion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ GETINSERTMARK**](tb-getinsertmark.md)
</dt> </dl>

 

 





