---
title: Message d’WM_CHOOSEFONT_SETLOGFONT (COMMDLG. h)
description: Une application envoie le \_ message WM CHOOSEFONT \_ SETLOGFONT à une boîte de dialogue de police pour définir les informations de police logique actuelles.
ms.assetid: ad169eca-a3ae-45bd-90df-821a93a7a764
keywords:
- Boîtes de dialogue de WM_CHOOSEFONT_SETLOGFONT message
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_SETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a588ebff7c8e56bb559a2cc9faa1d6290fbd8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742581"
---
# <a name="wm_choosefont_setlogfont-message"></a>\_ \_ Message SETLOGFONT WM CHOOSEFONT

Une application envoie le message **WM \_ CHOOSEFONT \_ SETLOGFONT** à une boîte de dialogue de **police** pour définir les informations de police logique actuelles.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_SETLOGFONT      (WM_USER + 101)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui contient des informations sur la police logique en cours.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

Quand vous appelez la fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour créer une boîte de dialogue de **police** , vous pouvez utiliser le membre **lpLogFont** de la structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour spécifier une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) contenant les valeurs initiales de la boîte de dialogue. Utilisez le message **WM \_ CHOOSEFONT \_ SETLOGFONT** pour spécifier une structure **LOGFONT** avec des valeurs différentes lorsque la boîte de dialogue **police** est ouverte.

En règle générale, vous envoyez le message **WM \_ CHOOSEFONT \_ SETLOGFONT** à partir d’une procédure de hook [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) . La procédure de hook peut également envoyer les messages [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) et [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) .

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

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**\_CHOOSEFONT WM \_ GETLOGFONT**](wm-choosefont-getlogfont.md)
</dt> <dt>

[**\_CHOOSEFONT WM \_ SETFLAGS**](wm-choosefont-setflags.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

