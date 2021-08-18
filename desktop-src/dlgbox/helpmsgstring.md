---
title: Message HELPMSGSTRING (COMMDLG. h)
description: Une boîte de dialogue commune envoie le message HELPMSGSTRING Registered à la procédure de fenêtre de sa fenêtre propriétaire quand l’utilisateur clique sur le bouton aide.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Boîtes de dialogue de message HELPMSGSTRING
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8a446164bb7ae51d36d1a89219f6c3b84eff74b9af3a40c2121b3bd205a581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741739"
---
# <a name="helpmsgstring-message"></a>Message HELPMSGSTRING

Une boîte de dialogue commune envoie le message **HELPMSGSTRING** Registered à la procédure de fenêtre de sa fenêtre propriétaire quand l’utilisateur clique sur le bouton **aide** .


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la boîte de dialogue commune.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la structure d’initialisation de la boîte de dialogue commune. Cette structure peut être une structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) ou [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Remarques

Vous devez spécifier la constante **HELPMSGSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.

Lorsque vous créez la boîte de dialogue, utilisez le membre **hwndOwner** de la structure d’initialisation pour identifier la fenêtre de réception des messages **HELPMSGSTRING** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HELPMSGSTRINGW** (Unicode) et **HELPMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CDN \_ AIDE**](cdn-help.md)
</dt> <dt>

[**LES ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

