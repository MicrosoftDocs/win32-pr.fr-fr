---
title: Message d’WM_CHOOSEFONT_SETFLAGS (COMMDLG. h)
description: Une application envoie le \_ message WM CHOOSEFONT \_ SETFLAGS à une boîte de dialogue de police pour définir les options d’affichage de la boîte de dialogue.
ms.assetid: 945ebc07-440d-4466-8255-ad344bdc568a
keywords:
- Boîtes de dialogue de WM_CHOOSEFONT_SETFLAGS message
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETFLAGS
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7abf436311f8a3868b1471c2a10a7ee2e4a3b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523897"
---
# <a name="wm_choosefont_setflags-message"></a>\_ \_ Message SETFLAGS WM CHOOSEFONT

Une application envoie le message **WM \_ CHOOSEFONT \_ SETFLAGS** à une boîte de dialogue de **police** pour définir les options d’affichage de la boîte de dialogue.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETFLAGS        (WM_USER + 102)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) qui contient de nouveaux paramètres dans le membre **Flags** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

La fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crée une boîte de dialogue de **police** et utilise une structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour spécifier les valeurs initiales du membre **Flags** . Utilisez le **message \_ \_ SETFLAGS WM CHOOSEFONT** pour spécifier des valeurs différentes pour le membre **Flags** lorsque la boîte de dialogue **police** est ouverte.

En règle générale, vous devez envoyer le message **WM \_ CHOOSEFONT \_ SETFLAGS** à partir d’une procédure de hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

