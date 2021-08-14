---
description: Envoyé à la fenêtre parente d’un contrôle ou d’un menu owner-drawn lorsqu’un aspect visuel du contrôle ou du menu a changé.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Message DFM_WM_DRAWITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7190d445490b581967c8dda67e170eb5db5665dfa59302313d7af736b275944d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969468"
---
# <a name="dfm_wm_drawitem-message"></a>\_Message DFM WM \_ DRAWITEM

Envoyé à la fenêtre parente d’un contrôle ou d’un menu owner-drawn lorsqu’un aspect visuel du contrôle ou du menu a changé.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Identificateur du contrôle qui a envoyé le message **DFM \_ WM \_ DRAWITEM** . Si le message a été envoyé par un menu, ce paramètre est égal à zéro.

</dd> <dt>

*lpDrawItem* \[ à\]
</dt> <dd>

Pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenant des informations sur l’élément à dessiner et le type de dessin requis.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la **valeur true**.

## <a name="remarks"></a>Remarques

Le membre **itemAction** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) spécifie l’opération de dessin qu’une application doit effectuer.

Avant de revenir au traitement de ce message, une application doit s’assurer que le contexte de périphérique identifié par le membre **HDC** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) est dans l’État par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
