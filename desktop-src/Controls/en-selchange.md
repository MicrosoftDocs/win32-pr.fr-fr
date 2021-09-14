---
title: Code de notification EN_SELCHANGE (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit que la sélection actuelle a été modifiée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006309"
---
# <a name="en_selchange-notification-code"></a>\_Code de notification en selChange

Avertit une fenêtre parente d’un contrôle RichEdit que la sélection actuelle a été modifiée. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) qui reçoit des informations sur la sélection.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce code de notification ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour recevoir les \_ codes de notification en selChange, spécifiez [**ENM \_ selChange**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

Ce code de notification est envoyé lorsque l’emplacement du signe insertion change et qu’aucun texte n’est sélectionné (la sélection est vide). La position du signe insertion peut changer lorsque l’utilisateur clique sur la souris, tape ou appuie sur une touche de direction.

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

[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> </dl>

 

 





