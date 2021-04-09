---
description: Envoyé à toutes les fenêtres une fois que l’utilisateur s’est connecté ou désactivé. Lorsque l’utilisateur ouvre ou ferme une session, le système met à jour les paramètres spécifiques à l’utilisateur. Le système envoie ce message immédiatement après la mise à jour des paramètres.
title: Message WM_USERCHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952904"
---
# <a name="wm_userchanged-message"></a>\_Message WM USERCHANGED

Envoyé à toutes les fenêtres une fois que l’utilisateur s’est connecté ou désactivé. Lorsque l’utilisateur ouvre ou ferme une session, le système met à jour les paramètres spécifiques à l’utilisateur. Le système envoie ce message immédiatement après la mise à jour des paramètres.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Ce message n’est pas pris en charge par Windows Vista.

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner zéro si elle traite ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble de Windows](windows.md)
</dt> </dl>

 

 
