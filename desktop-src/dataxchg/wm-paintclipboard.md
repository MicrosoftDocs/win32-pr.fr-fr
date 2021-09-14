---
title: Message WM_PAINTCLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au \_ format CF OWNERDISPLAY et que la zone cliente de la visionneuse du presse-papiers doit être redessinée.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- WM_PAINTCLIPBOARD des données de message Exchange
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008155"
---
# <a name="wm_paintclipboard-message"></a>\_Message WM PAINTCLIPBOARD

Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) et que la zone cliente de la visionneuse du presse-papiers doit être redessinée.


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre de la visionneuse du presse-papiers.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle d’un objet de mémoire global qui contient une structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) . La structure définit la partie de la zone cliente à peindre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Pour déterminer si la totalité de la zone cliente ou seulement une partie de celle-ci doit être redessinée, le propriétaire du presse-papiers doit comparer les dimensions de la zone de dessin donnée dans le membre **rcPaint** de [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) aux dimensions indiquées dans le message [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) le plus récent.

Le propriétaire du presse-papiers doit utiliser la fonction [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) pour verrouiller la mémoire qui contient la structure [**PAINTSTRUCT,**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Avant de retourner, le propriétaire du presse-papiers doit déverrouiller cette mémoire à l’aide de la fonction [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .

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

[**\_SIZECLIPBOARD WM**](wm-sizeclipboard.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

