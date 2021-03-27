---
description: Envoyé à la fenêtre parente d’un contrôle ou d’un menu owner-drawn lorsqu’un aspect visuel du contrôle ou du menu a changé.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Message DFM_WM_DRAWITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972006"
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

## <a name="remarks"></a>Notes

Le membre **itemAction** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) spécifie l’opération de dessin qu’une application doit effectuer.

Avant de revenir au traitement de ce message, une application doit s’assurer que le contexte de périphérique identifié par le membre **HDC** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) est dans l’État par défaut.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
