---
title: Code de notification EN_MSGFILTER (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle d’édition enrichi d’un événement de clavier ou de souris dans le contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006325"
---
# <a name="en_msgfilter-notification-code"></a>\_Code de notification en msgfilter

Avertit une fenêtre parente d’un contrôle d’édition enrichi d’un événement de clavier ou de souris dans le contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) contenant des informations sur le clavier ou le message de la souris. Si la fenêtre parente modifie cette structure et retourne une valeur différente de zéro, le message modifié est traité à la place de celui d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne zéro si le contrôle doit traiter l’événement de clavier ou de souris.

Retourne une valeur différente de zéro si le contrôle doit ignorer l’événement du clavier ou de la souris.

## <a name="remarks"></a>Notes

Pour recevoir les \_ codes de notification en msgfilter pour les événements, spécifiez un ou plusieurs des indicateurs suivants dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .



| Indicateur                                                                             | Signification                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**\_événements ENM**](rich-edit-control-event-mask-flags.md)       | Pour recevoir des codes de notification pour les événements de clavier.     |
| [**ENM \_ MOUSEEVENTS**](rich-edit-control-event-mask-flags.md)   | Pour recevoir des codes de notification pour les événements de souris.        |
| [**ENM \_ SCROLLEVENTS**](rich-edit-control-event-mask-flags.md) | Pour recevoir des codes de notification pour un événement de roulette de la souris. |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> </dl>

 

 





