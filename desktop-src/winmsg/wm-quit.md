---
description: Indique une demande d’arrêt d’une application et est générée lorsque l’application appelle la fonction PostQuitMessage. Ce message amène la fonction GetMessage à retourner zéro.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: Message WM_QUIT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f6b999ff23d964c1998fe1cc2a9991e11ecfe71760800b1d678e2f71b89273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881519"
---
# <a name="wm_quit-message"></a>\_Message WM Quit

Indique une demande d’arrêt d’une application et est générée lorsque l’application appelle la fonction [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) . Ce message amène la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) à retourner zéro.


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de sortie donné dans la fonction [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Ce message n’a pas de valeur de retour, car il provoque l’arrêt de la boucle de message avant que le message ne soit envoyé à la procédure de fenêtre de l’application.

## <a name="remarks"></a>Remarques

Le message **WM \_ Quit** n’est pas associé à une fenêtre et ne sera donc jamais reçu via la procédure de fenêtre d’une fenêtre. Elle est extraite uniquement par les fonctions [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .

Ne publiez pas le message **WM \_ Quit** à l’aide de la fonction [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ; utilisez [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
