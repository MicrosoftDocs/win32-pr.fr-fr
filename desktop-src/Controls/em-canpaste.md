---
title: Message EM_CANPASTE (RichEdit. h)
description: Détermine si un contrôle RichEdit peut coller un format de presse-papiers spécifié.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- EM_CANPASTE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195684"
---
# <a name="em_canpaste-message"></a>\_Message de CANPASTE em

Détermine si un contrôle RichEdit peut coller un format de presse-papiers spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie les [formats du presse-papiers](/windows/desktop/dataxchg/clipboard-formats) à essayer. Pour essayer un format qui se trouve actuellement dans le presse-papiers, définissez ce paramètre sur zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le format du presse-papiers peut être collé, la valeur de retour est une valeur différente de zéro.

Si le format du presse-papiers ne peut pas être collé, la valeur de retour est zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

