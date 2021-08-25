---
title: Code de notification EN_REQUESTRESIZE (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que le contenu du contrôle est plus petit ou plus grand que la taille de la fenêtre du contrôle. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE les contrôles de Windows de code de notification
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
ms.openlocfilehash: 9b15c21b180c2843eda7947946f6dc98d42caab1bad90383d6afe4a4f8002739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047579"
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

## <a name="remarks"></a>Remarques

Pour prendre en charge le comportement sans fin d’un contrôle RichEdit, la fenêtre parente doit redimensionner le contrôle lorsqu’il reçoit ce code de notification.

Pour recevoir les \_ codes de notification en REQUESTRESIZE, spécifiez [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

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

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> </dl>

 

 





