---
title: Code de notification EN_OLEOPFAILED (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit qu’une action de l’utilisateur sur un objet COM (Component Object Model) a échoué. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0391bfc61ff9350758ac81ff6f54fb1cff61d0dd1ebbcb2b8ef02ada9fe3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436679"
---
# <a name="en_oleopfailed-notification-code"></a>\_Code de notification en OLEOPFAILED

Avertit une fenêtre parente d’un contrôle RichEdit qu’une action de l’utilisateur sur un objet COM (Component Object Model) a échoué. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) qui contient des informations sur l’échec.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce code de notification retourne la valeur zéro.

## <a name="remarks"></a>Remarques

La fenêtre parente reçoit toujours un [**message \_ de notification WM**](wm-notify.md) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).

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

[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





