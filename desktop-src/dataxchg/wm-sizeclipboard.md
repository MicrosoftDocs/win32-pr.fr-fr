---
title: Message WM_SIZECLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au \_ format CF OWNERDISPLAY et que la zone cliente de la visionneuse du presse-papiers a changé de taille.
ms.assetid: 95991d03-8677-4dde-b72a-082dec4834b3
keywords:
- WM_SIZECLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_SIZECLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235de630b20757a571b1917a975d1425bee06cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741861"
---
# <a name="wm_sizeclipboard-message"></a>\_Message WM SIZECLIPBOARD

Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) et que la zone cliente de la visionneuse du presse-papiers a changé de taille.


```C++
#define WM_SIZECLIPBOARD                0x030B
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre de la visionneuse du presse-papiers.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle d’un objet de mémoire global qui contient une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) . La structure spécifie les nouvelles dimensions de la zone cliente de la visionneuse du presse-papiers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Quand la fenêtre de la visionneuse du presse-papiers est sur le point d’être détruite ou redimensionnée, un message **WM \_ SIZECLIPBOARD** est envoyé avec un rectangle null (0, 0, 0, 0) en tant que nouvelle taille. Cela permet au propriétaire du presse-papiers de libérer ses ressources d’affichage.

Le propriétaire du presse-papiers doit utiliser la fonction [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) pour verrouiller l’objet mémoire qui contient [**Rect**](/previous-versions//dd162897(v=vs.85)). Avant de retourner, le propriétaire du presse-papiers doit déverrouiller l’objet à l’aide de la fonction [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

