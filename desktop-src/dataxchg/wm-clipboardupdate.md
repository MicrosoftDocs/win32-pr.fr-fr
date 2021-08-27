---
title: Message WM_CLIPBOARDUPDATE (winuser. h)
description: Envoyé lorsque le contenu du presse-papiers a changé.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- WM_CLIPBOARDUPDATE des données de message Exchange
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0483ba43b6b0c660daee74637fd9f9ac8d377a16097b5cfd60632c1b691ead7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991219"
---
# <a name="wm_clipboardupdate-message"></a>\_Message WM CLIPBOARDUPDATE

Envoyé lorsque le contenu du presse-papiers a changé.


```C++
#define WM_CLIPBOARDUPDATE              0x031D
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Remarques

Pour inscrire une fenêtre pour recevoir ce message, utilisez la fonction [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 





