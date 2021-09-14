---
title: Code de notification EN_STOPNOUNDO (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit qu’une action s’est produite pour laquelle le contrôle ne peut pas allouer suffisamment de mémoire pour maintenir l’état d’annulation. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006306"
---
# <a name="en_stopnoundo-notification-code"></a>\_Code de notification en STOPNOUNDO

Avertit une fenêtre parente d’un contrôle RichEdit qu’une action s’est produite pour laquelle le contrôle ne peut pas allouer suffisamment de mémoire pour maintenir l’état d’annulation. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retournez zéro pour poursuivre l’opération d' **annulation** .

Retourne une valeur différente de zéro pour arrêter l’opération d' **annulation** .

## <a name="remarks"></a>Notes

La fenêtre parente reçoit toujours un [**message \_ de notification WM**](wm-notify.md) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).

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

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> </dl>

 

 





