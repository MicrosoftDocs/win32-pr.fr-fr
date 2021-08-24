---
title: Message COLOROKSTRING (COMMDLG. h)
description: Une boîte de dialogue de couleur envoie le message COLOROKSTRING Registered à votre procédure de Hook, CCHookProc, lorsque l’utilisateur sélectionne une couleur et clique sur le bouton OK.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Boîtes de dialogue de message COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd55db4bb935880438290a83cd99c420ebcabf23ca8cb1bb238ea15f39e06247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726279"
---
# <a name="colorokstring-message"></a>Message COLOROKSTRING

Une boîte de dialogue de **couleur** envoie le message **COLOROKSTRING** Registered à votre procédure de Hook, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), lorsque l’utilisateur sélectionne une couleur et clique sur le bouton **OK** . La procédure de raccordement peut accepter la couleur et autoriser la fermeture de la boîte de dialogue, ou refuser la couleur et forcer la boîte de dialogue à rester ouverte.


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**les ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Le membre **rgbResult** de cette structure contient la valeur de couleur RVB de la couleur sélectionnée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la procédure de raccordement retourne la valeur zéro, la boîte de dialogue **couleur** accepte la couleur sélectionnée et se ferme.

Si la procédure de raccordement retourne une valeur différente de zéro, la boîte de dialogue **couleur** rejette la couleur sélectionnée et reste ouverte.

## <a name="remarks"></a>Remarques

La procédure de hook doit spécifier la constante **COLOROKSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **COLOROKSTRINGW** (Unicode) et **COLOROKSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**LES ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

