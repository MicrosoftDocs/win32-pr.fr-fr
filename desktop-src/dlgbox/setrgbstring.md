---
title: Message SETRGBSTRING (COMMDLG. h)
description: La procédure de raccordement d’une boîte de dialogue de couleur, CCHookProc, peut envoyer le message SETRGBSTRING Registered à la boîte de dialogue pour définir la sélection de couleur actuelle.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Boîtes de dialogue de message SETRGBSTRING
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8322bb07300ce188684f5097232563e80721fadf0f614c24ac5f7b2d034c1fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985309"
---
# <a name="setrgbstring-message"></a>Message SETRGBSTRING

La procédure de raccordement d’une boîte de dialogue de **couleur** , [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), peut envoyer le message **SETRGBSTRING** Registered à la boîte de dialogue pour définir la sélection de couleur actuelle.


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur RVB de la couleur à sélectionner dans la boîte de dialogue **couleur** . Vous pouvez utiliser la macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) pour spécifier les intensités rouge, verte et bleue d’une valeur de couleur RVB.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Remarques

Si *lParam* correspond à l’une des couleurs de base ou à l’une des 16 couleurs personnalisées, la procédure de la boîte de dialogue sélectionne cette couleur. La procédure de boîte de dialogue met également à jour tous les contrôles dans l’extension de couleur personnalisée de la boîte de dialogue **couleur** , s’il est ouvert.

Si *lParam* ne correspond pas à une couleur de base ou personnalisée, la procédure de boîte de dialogue ne change pas la sélection de couleur actuelle, mais elle met à jour les contrôles de couleur personnalisés, s’ils sont visibles.

## <a name="examples"></a>Exemples

L’exemple de code suivant obtient l’identificateur de message **SETRGBSTRING** , puis définit la sélection de couleur sur bleu.


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **SETRGBSTRINGW** (Unicode) et **SETRGBSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

