---
title: Code de notification EN_PROTECTED (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que l’utilisateur effectue une action qui modifie une plage de texte protégée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d56af51eea8486286dea8905d52dc64fe0a54803c30d6b6c6f4dabd49ea406b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047629"
---
# <a name="en_protected-notification-code"></a>\_Code de notification en code protégé

Avertit une fenêtre parente d’un contrôle RichEdit que l’utilisateur effectue une action qui modifie une plage de texte protégée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**protégée**](/windows/desktop/api/Richedit/ns-richedit-enprotected) contenant des informations sur le message qui a déclenché le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez zéro pour permettre l’opération.

Retournez une valeur différente de zéro pour empêcher l’opération.

## <a name="remarks"></a>Remarques

Si la valeur zéro est retournée et que les membres **MSG**, **wParam** et **lParam** de la structure [**protégée**](/windows/desktop/api/Richedit/ns-richedit-enprotected) sont modifiés, le contrôle traite le message révisé à la place du message d’origine.

Pour recevoir des \_ codes de notification en protection, spécifiez [**ENM \_ protected**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**PROTÉGÉ**](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> </dl>

 

 





