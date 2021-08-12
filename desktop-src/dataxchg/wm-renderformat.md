---
title: Message WM_RENDERFORMAT (winuser. h)
description: Envoyé au propriétaire du presse-papiers s’il a retardé le rendu d’un format de presse-papiers spécifique et si une application a demandé des données dans ce format.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT des données de message Exchange
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
ms.openlocfilehash: 2885e056577656d6cabb8ea78f48a02a19f3c3c40bb3c30b1e5ca25c72cdf39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545308"
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

## <a name="remarks"></a>Remarques

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

 

 





