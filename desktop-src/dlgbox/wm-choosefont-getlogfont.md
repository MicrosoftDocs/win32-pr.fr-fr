---
title: Message d’WM_CHOOSEFONT_GETLOGFONT (COMMDLG. h)
description: Une application envoie le \_ message WM CHOOSEFONT \_ GETLOGFONT à une boîte de dialogue de police pour récupérer des informations sur les sélections de polices d’utilisateur actuelles.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Boîtes de dialogue de WM_CHOOSEFONT_GETLOGFONT message
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fb429c3cd66af28485edf2979d2efbe50b3205a2142e963c8c3bb51ef5713f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280431"
---
# <a name="wm_choosefont_getlogfont-message"></a>\_ \_ Message GETLOGFONT WM CHOOSEFONT

Une application envoie le message **WM \_ CHOOSEFONT \_ GETLOGFONT** à une boîte de dialogue de **police** pour récupérer des informations sur les sélections de polices d’utilisateur actuelles.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) qui reçoit des informations sur les sélections de polices actuelles de l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crée une boîte de dialogue de **police** . Lorsque l’utilisateur ferme la boîte de dialogue **police** , la fonction **ChooseFont** retourne des informations sur les sélections de police de l’utilisateur dans la structure [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) . Le membre **lpLogFont** de la structure **CHOOSEFONT** est un pointeur vers une structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

Utilisez le message **WM \_ CHOOSEFONT \_ GETLOGFONT** pour obtenir des informations sur les sélections de polices d’utilisateur actuelles lorsque la boîte de dialogue **police** est ouverte. Par exemple, si vous activez le bouton **appliquer** dans la boîte de dialogue **police** , envoyez le message pour obtenir les informations de police à appliquer à la sélection de texte actuelle.

En règle générale, vous activez une procédure de hook [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) pour traiter les messages de [**\_ commande WM**](/windows/desktop/menurc/wm-command) pour le bouton **appliquer** . Quand l’utilisateur clique sur le bouton **apply** , la procédure de hook envoie le message **WM \_ CHOOSEFONT \_ GETLOGFONT** à la boîte de dialogue.

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

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

