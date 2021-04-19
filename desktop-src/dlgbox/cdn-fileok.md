---
title: CDN_FILEOK le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur lorsque l’utilisateur spécifie un nom de fichier et clique sur le bouton OK.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- Boîtes de dialogue CDN_FILEOK code de notification
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511390"
---
# <a name="cdn_fileok-notification-code"></a>\_Code de notification CDN FILEOK

Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur lorsque l’utilisateur spécifie un nom de fichier et clique sur le bouton **OK** .

Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) .

La structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ FILEOK** .

La structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) contient également un pointeur vers une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) dont le membre **lpstrFile** spécifie l’adresse du nom de fichier sélectionné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la procédure de raccordement retourne la valeur zéro, la boîte de dialogue accepte le nom de fichier spécifié et se ferme.

Pour rejeter le nom de fichier spécifié et forcer la boîte de dialogue à rester ouverte, retournez une valeur différente de zéro à partir de la procédure de raccordement et appelez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour définir une valeur **\_ MSGRESULT DWL** différente de zéro.

## <a name="remarks"></a>Notes

Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**\_notification WM**](../controls/wm-notify.md)
</dt> </dl>

 

