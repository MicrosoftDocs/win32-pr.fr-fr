---
title: Code de notification EN_REQUESTRESIZE (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que le contenu du contrôle est plus petit ou plus grand que la taille de la fenêtre du contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- Contrôles Windows de code de notification EN_REQUESTRESIZE
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104497"
---
# <a name="en_requestresize-notification-code"></a>\_Code de notification en REQUESTRESIZE

Avertit une fenêtre parente d’un contrôle RichEdit que le contenu du contrôle est plus petit ou plus grand que la taille de la fenêtre du contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) qui reçoit la taille demandée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce code de notification ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour prendre en charge le comportement sans fin d’un contrôle RichEdit, la fenêtre parente doit redimensionner le contrôle lorsqu’il reçoit ce code de notification.

Pour recevoir les \_ codes de notification en REQUESTRESIZE, spécifiez [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> </dl>

 

 





