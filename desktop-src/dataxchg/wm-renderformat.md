---
title: Message WM_RENDERFORMAT (winuser. h)
description: Envoyé au propriétaire du presse-papiers s’il a retardé le rendu d’un format de presse-papiers spécifique et si une application a demandé des données dans ce format.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT l’échange de données de message
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317261"
---
# <a name="wm_renderformat-message"></a>\_Message WM RENDERFORMAT

Envoyé au propriétaire du presse-papiers s’il a retardé le rendu d’un format de presse-papiers spécifique et si une application a demandé des données dans ce format. Le propriétaire du presse-papiers doit restituer les données dans le format spécifié et les placer dans le presse-papiers en appelant la fonction [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[Format du presse-papiers](standard-clipboard-formats.md) à restituer.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Lors de la réponse à un message **WM \_ RENDERFORMAT** , le propriétaire du presse-papiers ne doit pas ouvrir le presse-papiers avant d’appeler [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata). Il n’est pas nécessaire d’ouvrir le presse-papiers avant de placer des données en réponse à **WM \_ RENDERFORMAT**, et toute tentative d’ouvrir le presse-papiers échoue parce que le presse-papiers est actuellement maintenu ouvert par l’application qui a demandé le rendu du format.

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

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**\_RENDERALLFORMATS WM**](wm-renderallformats.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

 





