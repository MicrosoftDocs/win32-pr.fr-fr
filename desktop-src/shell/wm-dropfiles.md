---
description: Envoyé lorsque l’utilisateur dépose un fichier dans la fenêtre d’une application qui s’est inscrite en tant que destinataire des fichiers supprimés.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Message WM_DROPFILES (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973106"
---
# <a name="wm_dropfiles-message"></a>\_Message WM DROPFILES

Envoyé lorsque l’utilisateur dépose un fichier dans la fenêtre d’une application qui s’est inscrite en tant que destinataire des fichiers supprimés.


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDrop* 
</dt> <dd>

Handle vers une structure interne décrivant les fichiers déplacés. Transmettez ce handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)ou [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) pour récupérer des informations sur les fichiers déplacés.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Le descripteur HDROP est déclaré dans shellapi. h. Vous devez inclure cet en-tête dans votre build pour utiliser **WM \_ DROPFILES**. Pour plus d’informations sur l’utilisation de la fonction glisser-déplacer pour transférer des données de Shell, consultez [transfert de données de Shell à l’aide de la fonction glisser-déplacer ou du presse-papiers](dragdrop.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**DragAcceptFiles**](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
