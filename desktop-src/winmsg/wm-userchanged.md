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
ms.openlocfilehash: 2bb466e80070fe1be5cd7af7889fc5727c81f8caad89ad60c48c7a105b688fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705699"
---
# <a name="wm_userchanged-message"></a>\_Message WM USERCHANGED

Envoyé à toutes les fenêtres une fois que l’utilisateur s’est connecté ou désactivé. Lorsque l’utilisateur ouvre ou ferme une session, le système met à jour les paramètres spécifiques à l’utilisateur. Le système envoie ce message immédiatement après la mise à jour des paramètres.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> ce message n’est pas pris en charge à partir de Windows Vista.

 


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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Vue](windows.md)
</dt> </dl>

 

 
