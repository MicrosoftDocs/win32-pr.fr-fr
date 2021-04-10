---
title: Code de notification EN_CHANGE (Rich Edit) (winuser. h)
description: Avertit la fenêtre hôte d’un contrôle Rich Edit sans fenêtre qu’une modification s’est produite. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- Contrôles Windows de code de notification EN_CHANGE (modification enrichie)
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941957"
---
# <a name="en_change-rich-edit-notification-code"></a>\_Code de notification en modification (RichEdit)

Avertit la fenêtre hôte d’un contrôle Rich Edit sans fenêtre qu’une modification s’est produite. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) spécifiant la modification apportée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce code de notification ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour recevoir les \_ codes de notification de modification, spécifiez [**ENM \_ change**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





