---
description: Une application envoie le \_ message WM FONTCHANGE à toutes les fenêtres de niveau supérieur dans le système après la modification du pool de ressources de police.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Message WM_FONTCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118281"
---
# <a name="wm_fontchange-message"></a>\_Message WM FONTCHANGE

Une application envoie le message **WM \_ FONTCHANGE** à toutes les fenêtres de niveau supérieur dans le système après la modification du pool de ressources de police.

Pour envoyer ce message, appelez la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec les paramètres suivants.


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
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

## <a name="remarks"></a>Notes

Une application qui ajoute ou supprime des polices du système (par exemple, à l’aide de la fonction [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) ou [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ) doit envoyer ce message à toutes les fenêtres de niveau supérieur.

Pour envoyer le message **WM \_ FONTCHANGE** à toutes les fenêtres de niveau supérieur, une application peut appeler la fonction **SendMessage** avec le paramètre *HWND* défini sur \_ Broadcast HWND.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des polices et du texte](fonts-and-text.md)
</dt> <dt>

[Polices et messages texte](font-and-text-messages.md)
</dt> <dt>

[**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
