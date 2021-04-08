---
title: Code de notification EN_CLIPFORMAT (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit qu’un collage a été effectué avec un format de presse-papiers particulier. Un contrôle RichEdit sans fenêtre envoie cette notification à l’aide de la méthode ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- Contrôles Windows de code de notification EN_CLIPFORMAT
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941954"
---
# <a name="en_clipformat-notification-code"></a>\_Code de notification en CLIPFORMAT

Avertit une fenêtre parente d’un contrôle RichEdit qu’un collage a été effectué avec un format de presse-papiers particulier. Un contrôle RichEdit sans fenêtre envoie cette notification à l’aide de la méthode [**ITextHost :: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

ID de fenêtre récupéré en appelant la fonction [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) avec la \_ valeur d’ID GWL.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) qui contient des informations sur le format du presse-papiers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Pour recevoir les \_ codes de notification en CLIPFORMAT, spécifiez [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

