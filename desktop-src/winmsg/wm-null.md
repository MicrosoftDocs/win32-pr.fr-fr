---
description: N’effectue aucune opération. Une application envoie le \_ message WM null s’il souhaite poster un message que la fenêtre destinataire ignorera.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Message WM_NULL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202881"
---
# <a name="wm_null-message"></a>\_Message WM null

N’effectue aucune opération. Une application envoie le message **WM \_ null** s’il souhaite poster un message que la fenêtre destinataire ignorera.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NULL                         0x0000
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

Une application retourne la valeur zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Par exemple, si une application a installé un hook **BL \_ GETMESSAGE** et qu’elle souhaite empêcher le traitement d’un message, la fonction de rappel [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) peut modifier le numéro de message en **WM \_ null** afin que le destinataire l’ignore.

Autre exemple : une application peut vérifier si une fenêtre répond aux messages en envoyant le message **WM \_ null** avec la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble de Windows](windows.md)
</dt> </dl>

 

 
